# Jelajah Tulungagung — Petualangan Piksel

A cozy top-down pixel adventure that lets you explore **Tulungagung, East Java** — 32 real
researched destinations and foods (beaches, waterfalls, hills, dams, culture, and kuliner),
each with live royalty-safe photos, Google Maps links, traveler info, and a wishlist.

Built as a single self-contained `index.html` (HTML5 canvas + Web Audio). **No build step.**

## Features

- **Trilingual** — Indonesia / English / Basa Jawa (ID/EN/JV toggle, choice persisted).
- **32 spots, all sourced** — 9 beaches, waterfalls & nature, marble/batik/dance culture,
  and 12+ kuliner. Every popup has rating/price, address, facts, and a **Sumber** link.
- **Real photos in-game** — pulled live from Wikimedia Commons with photographer + license
  attribution and a fullscreen lightbox. Falls back to hand-drawn pixel "postcards" offline.
- **Guided & beginner-friendly** — a compass, a step-by-step trail (Step 1/32), a minimap,
  and the "SELAMAT DATANG DI / TULUNGAGUNG" welcome floor text at the spawn square.
- **Original gamelan music** — fully synthesized in Web Audio (slendro-ish colotomic
  structure), 100% royalty-free. Toggle with 🎵.
- **Mobile + desktop** — on-screen joystick + PERIKSA button on touch, WASD/arrows + E on
  keyboard, responsive zoom, and safe-area insets. Progress auto-saves to the device.

## Run locally

It's a static file — just open it, or serve the folder:

```sh
# Python
python -m http.server 8000
# or Node
npx serve .
```

Then visit http://localhost:8000. (A local server is recommended over `file://` so the
in-game Wikimedia photo fetch works; everything else runs offline.)

## Deploy

Drop the folder on any static host — zero config, zero build:

- **Cloudflare Pages** — connect the repo (build command: *none*, output dir: `/`),
  or `npx wrangler pages deploy .`
- **Netlify** — drag-and-drop the folder, or `netlify deploy --dir .`
- **Vercel** — `vercel --prod` (no framework preset needed).
- **GitHub Pages** — push and enable Pages on the branch root.

## Notes

- Photos load on popup open and need internet; offline shows the pixel illustration plus the
  "Buka Maps" button. Wikimedia is used (not re-hosted Google photos) so every image is
  free-licensed and credited.
- Map coordinates are thematic (beaches south, hills north), not GPS-accurate.

## Credit

Designed in [Claude Design](https://claude.ai/design) and implemented from the handoff bundle.
Gamelan audio and pixel art are original. Destination data is linked to its sources in each popup.
