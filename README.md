# StoryTeller

A visual story canvas for writers. Plot your scenes on an infinite canvas, branch your timelines, and trace storylines through the structure of your narrative — all in a single HTML file, no server required.

---

## What it does

- **Scene cards** — each card holds a scene number, title, description, in-story date and time, and your own writer notes
- **Branching** — fork any scene into parallel timelines (BSS, SBSS, nested branches) with colour-coded cards and connection lines
- **Storylines** — trace a read path through any sequence of scenes across branches
- **Writer overlay** — click a scene's description to enter a full-screen, distraction-free writing surface
- **Auto-arrange** — lay out all cards into a clean grid automatically
- **Import / Export** — full JSON export and import, so your data is always yours
- **Offline-first** — works with no internet connection after the first load (PWA)
- **Installable** — add to your home screen or desktop like a native app

---

## File structure

```
StoryTeller/
├── index.html       ← the entire app (HTML + CSS + JS, self-contained)
├── manifest.json    ← PWA manifest (name, icons, theme)
├── sw.js            ← service worker (offline caching)
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── README.md
```

> All logic, styling, and behaviour live inside `index.html`. The manifest and service worker are the only external files the app needs.

---

## Setup

### GitHub Pages (recommended)

1. Fork or clone this repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, root folder
4. Your app will be live at `https://yourusername.github.io/StoryTeller/`

### Local use

Just open `index.html` in any modern browser. No build step, no dependencies, no server needed.

> To enable the service worker locally (for offline testing), serve via a local HTTP server:
> ```bash
> python -m http.server 8080
> ```
> Then open `http://localhost:8080`.

---

## PWA install

Once the app is open in Chrome, Edge, or Safari (iOS 16.4+):

- **Desktop:** look for the install icon in the address bar → click → Install
- **Mobile:** browser menu → "Add to Home Screen"

After install, StoryTeller runs as a standalone app with no browser chrome.

---

## Data storage

Your story data is saved to the browser's local storage (`localStorage` / `window.storage`) automatically. Nothing is sent to any server. Your data never leaves your device.

To back up or move your data, use **Export JSON** in the sidebar. To restore, use **Import JSON**.

---

## Icons

The `icons/` folder expects two PNG files:

| File | Size | Use |
|---|---|---|
| `icon-192.png` | 192 × 192 px | Android home screen, PWA splash |
| `icon-512.png` | 512 × 512 px | Desktop install, app stores |

You can generate these from any image using [Favicon.io](https://favicon.io) or [RealFaviconGenerator](https://realfavicongenerator.net).

---

## License

Copyright © 2026 Arshad (Loki). All rights reserved.

This project is licensed under the **GNU General Public License v3.0**.

You may use, study, and modify this software freely. If you distribute it or any derivative work — in any form, modified or unmodified — you must:

- Release the full source code under GPL-3.0
- Credit the original author
- Not restrict others' rights to do the same

See the full license text at [https://www.gnu.org/licenses/gpl-3.0.html](https://www.gnu.org/licenses/gpl-3.0.html).

**In plain language:** you can build on this. You cannot close it.
