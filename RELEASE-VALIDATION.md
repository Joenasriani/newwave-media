# NewWave Media — Release validation

Audit: 2026-11-17. Application change: 9b75972599e843e687c19717725a10dba8fc8dcc.

## Evidence obtained

- Committed inline JavaScript parses successfully.
- Extracted playback probe and M3U parser exercised in headless Chromium at desktop 1440×900 and mobile-emulated 390×844. Local synthetic WebM video and WAV audio both advanced playback; corrupt media and pre-aborted probes were rejected; probe elements were cleaned up. Playlist fixture retained two distinct HTTPS entries (one relative URL), rejected duplicate/insecure entries.
- Subtitle parser fixture recognized a valid cue and rejected an inverted time interval.
- These isolated tests are not a complete app or device test, nor a live HLS test.
- External DNS failed in the test environment. No external media URL was certified playable. No matching NewWave Media project was found by name in the connected Vercel project listing.

## Sources and rights

- https://github.com/iptv-org/iptv — community-supplied URLs; individual broadcasting authorization and territorial rights remain unverified. Do not describe these as licensed solely because they play.
- https://studio.blender.org/films/ — official open-film project directory; attribution link included in app. Verify exact versions and applicable license credits.
- Internet Archive film metadata is an initial rights screen, not legal proof.
- https://github.com/video-dev/hls.js — HLS resources require appropriate cross-origin GET access.

## Mandatory live acceptance matrix

For each source, record broadcaster, channel/film, exact source and stream URLs, license/authorization evidence, test timestamp, actual country/network, browser/OS, manifest and media-segment access, CORS outcome, decoding, at least 60 seconds of continuous playback, audible audio where applicable, and status. Redact any signed credentials from evidence.

Test Lebanon and UAE separately using authorized connections in each country. Do not defeat region restrictions. Test real Android Chrome and iPhone Safari, plus desktop Chrome, Edge and Firefox. Exercise full-screen, local media, subtitles, queues, resume, HLS quality changes, errors, filtering, and responsive layout at narrow and wide viewports. Confirm deployed revision matches main.

Statuses: PASS / FAIL / NOT TESTED / RIGHTS UNVERIFIED / TERRITORY RESTRICTED. A successful local playback probe is not a rights or worldwide availability certification. Do not publish unverified curated channels as certified.

Release sign-off: OPEN. External per-stream playback, regional access, CORS, real-device and full application testing are outstanding.

## 2026-11-17 compact player update

Player remains visible on startup; validated channels populate a compact selector. Muted autoplay attempts the first validated channel. The Live screen no longer exposes import tools, long rights statements or expanded movie discovery by default. Syntax, DOM ID references and stylesheet preservation checked. Production deployment status does not certify external live playback or actual mobile interaction.
