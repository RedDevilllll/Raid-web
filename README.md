# RAID — Web playtest

This repository contains only the current compiled Web client for the RAID prototype.
The source code and authoritative game server remain in the private `Raid` repository.

## Stable entry point

Use this URL for every user and tester:

https://reddevilllll.github.io/Raid-web/

Do not share versioned files such as `raid2-mobile-v66.html`; the root loader is the permanent address.

## Current network layout

- GitHub Pages stores the current v66 Web client files and browser-cacheable static assets.
- The root `index.html` forwards to the current hybrid loader.
- The hybrid loader keeps the WebSocket connection on the Tailscale host:
  `wss://home-red.taildfbfaa.ts.net/raid-ws`.
- The Godot host must be running before a player enters the game.
- For local Wi‑Fi testing, use the preview URL from the private source repository:
  `https://<PC-LAN-IP>:8767/raid2-mobile.html?host=<PC-LAN-IP>&port=29032`.

Old v60–v65 deployment files were removed from the active branch. Git history still preserves them if an older build ever needs investigation.

## Important limitation

The current public route is a working prototype route, not a final production hosting architecture.
To let players enter without the home PC/Tailscale host, the next delivery step is a public WebSocket relay/server.
