# Laurel Lane — Project Command PWA

## Files in this folder
- index.html      — Main app
- manifest.json   — PWA manifest
- sw.js           — Service worker (offline support)
- icon-*.png      — App icons (72px through 512px)

## How to install on your home screen

PWAs must be served over HTTPS (or localhost) — a local file:// path will NOT trigger installation.
The easiest zero-cost options:

────────────────────────────────────────
OPTION 1 — Netlify Drop (easiest, 2 min)
────────────────────────────────────────
1. Go to https://app.netlify.com/drop
2. Drag this entire folder onto the page
3. Netlify gives you a free HTTPS URL instantly
4. Open that URL on your iPhone/Android
5. iOS: tap Share → Add to Home Screen
   Android/Chrome: tap the menu → Install App (or banner appears automatically)

────────────────────────────────────────
OPTION 2 — GitHub Pages (free, permanent)
────────────────────────────────────────
1. Create a free GitHub account at github.com
2. Create a new repository (public)
3. Upload all files in this folder
4. Go to Settings → Pages → Branch: main → Save
5. Your app is live at https://yourusername.github.io/yourrepo/
6. Open on phone and install from browser

────────────────────────────────────────
OPTION 3 — Local server (on your Mac/PC)
────────────────────────────────────────
If you just want to test locally:
  npx serve .          (requires Node.js)
  OR: python3 -m http.server 8080
Then open http://localhost:8080 in Chrome
Note: localhost works for PWA testing but won't install on your phone

────────────────────────────────────────
BACKUP YOUR DATA
────────────────────────────────────────
Your data lives in the browser's localStorage for whichever domain you host it on.
Use the BACKUP button inside the app to export a JSON file regularly.
If you ever move to a different URL, use RESTORE to reload your data.

────────────────────────────────────────
UPDATING THE APP
────────────────────────────────────────
If you get a new version of index.html:
1. Replace index.html on your host
2. Open the app and pull to refresh (or close and reopen)
3. The service worker will fetch the new version automatically
