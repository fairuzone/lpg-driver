# LPG Driver App (PWA) for LaundryBar

Mobile-first Progressive Web App for LPG delivery drivers.

## Features
- Select driver (persisted)
- List today's jobs from Google Apps Script
- Scan branch QR to confirm arrival
- Scan cylinder QRs (deliver/collect/load/return)
- Capture timestamped photo + short video
- GPS check
- Offline queue via IndexedDB
- Installable PWA (Add to Home Screen)

## Setup
1. Edit `config.js` with your Apps Script URL and key.
2. Host the folder on GitHub Pages (or any HTTPS host).
3. Open `index.html` on the phone (HTTPS required for camera/GPS).
4. Add to Home Screen for app-like experience.

## Files
- `index.html` – main app
- `config.js` – backend URL + key
- `manifest.json` – PWA manifest
- `sw.js` – service worker (caching)
- `lb-logo.jpg` – header logo

## Notes
- POST uses `Content-Type: text/plain;charset=utf-8` to avoid CORS preflight.
- Branch codes generated as STATE_INITIALS (e.g. SL_TBB).
- Queue badge shows pending offline uploads.
- Permissions requested on first use (camera + location).

Test with the demo driver if backend is not ready.
