# Praat Mee

Spoken Dutch (A2-B1) for daily life: 309 phrases in 19 situations, 19 short dialogues, FSRS-5 spaced repetition. Single static page, works offline, no accounts, no external APIs. Progress is stored in the browser on your device.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app, phrase data embedded |
| `manifest.webmanifest` | Home-screen install (name, icons, standalone mode) |
| `sw.js` | Offline cache |
| `icon-*.png`, `apple-touch-icon.png` | App icons |
| `.nojekyll` | Tells GitHub Pages to serve files as-is |

## Publish on GitHub Pages

1. Create a public repository, e.g. `praat-mee`.
2. Upload all files from this folder to the repository root (including `.nojekyll`).
3. Settings → Pages → Source: *Deploy from a branch* → Branch `main`, folder `/ (root)` → Save.
4. After about a minute the app is live at `https://<username>.github.io/praat-mee/`.

## Install on the phone

- **iPhone (Safari):** open the link → Share → *Add to Home Screen*.
- **Android (Chrome):** open the link → menu → *Install app* / *Add to Home screen*.
- Open the app once while online; after that it works offline.
- For Dutch audio on iPhone: Settings → Accessibility → Spoken Content → Voices → Dutch → download a voice.

## Updating

1. Replace `index.html` in the repository.
2. In `sw.js` change `VERSION` (e.g. `praat-mee-v4`) so phones fetch the new version.
3. Progress is kept: it lives in the phone's browser storage, not in the repository.
4. If you change icons or the manifest, remove the home-screen icon and add it again (iOS caches icons).

## Backup

Settings → Backup → *Export progress* saves a JSON file. Do this before clearing Safari data or switching phones.
