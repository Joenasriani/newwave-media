# NewWave Media

Discover free-to-access movies and English-language live TV with NewWave Media, a browser-based player for local files, authorized streaming URLs and M3U playlists.

Website: https://newwave-free-movies.vercel.app/

## Features and limitations

NewWave Media is a mobile-first browser media player. Main navigation: Live, Add URL, Open File, Queue. USA channel discovery starts automatically; English-language directory is selectable. Community IPTV-org entries are tested for three seconds of advancing video before being shown as playable; results expire and are rechecked. Playback is not proof of broadcasting authorization or country availability. Local video and audio files stay on the device; playback uses object URLs. Supports direct HTTPS media URLs, M3U channel playlists, native HLS or HLS.js, SRT/VTT captions, queue, shuffle, repeat, resume, speed, picture fit, fullscreen and picture-in-picture where supported. Internet Archive film discovery screens rights metadata; Blender open films have attribution links. NewWave itself requires no account or subscription. External services may require accounts or subscriptions. No hosting of third-party movies, DRM or geographic bypass. Individual external channel rights and live playback in Lebanon and UAE remain unverified.

## Run locally

Serve the repository root with `python3 -m http.server 8080` and open http://localhost:8080. Static HTML/CSS/JS, no backend or build dependencies; HLS.js loaded from a pinned CDN. External playback depends on connectivity and browser support.

## Deployment and design lock

Vercel project: free-movies. Production branch: main. Preserve existing CSS, colors and four primary navigation actions.

## Synchronization

index.html is the functional source of truth. Update README, llms.txt, llms-full.txt, .well-known/newwave-media.json, sitemap, robots, metadata and RELEASE-VALIDATION.md whenever their underlying facts change. No hidden keyword blocks. See [validation evidence](RELEASE-VALIDATION.md).

Live is the default experience: the player remains visible above a compact, searchable USA/English channel selector. NewWave attempts muted autoplay of the first channel that passes a device-local playback check. Tap Sound to enable audio or tap a channel to switch. Playlist import and remote playlist URLs are under Add URL. Movies and other sources are collapsed by default. Browser autoplay policies, network conditions and regional restrictions can prevent startup; no individual channel is guaranteed.
