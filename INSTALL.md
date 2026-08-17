# Break — install on iPhone

A single-page web app. Once on your home screen it runs full-screen, works offline,
and keeps your calibration log on the phone.

Apple does not allow sideloading a real .ipa without a developer account, so this
is a PWA. In use it is indistinguishable from a native app: own icon, no Safari
chrome, works with no signal.

## Fastest route — GitHub Pages (about 5 minutes, free, permanent)

1. github.com → New repository → name it `break` → Public → Create.
2. On the repo page: **Add file → Upload files**. Drag in all five files from this
   folder (index.html, manifest.webmanifest, sw.js, and the three .png icons).
   Do not upload the folder itself — upload the files.
3. Commit.
4. **Settings → Pages**. Source: *Deploy from a branch*. Branch: `main`, folder `/ (root)`. Save.
5. Wait ~1 minute. Your URL is `https://YOURNAME.github.io/break/`
6. Open that URL **in Safari on the iPhone** (not Chrome — only Safari can add to
   the home screen).
7. Share button → **Add to Home Screen** → Add.

Done. Tap the icon. Turn on airplane mode to confirm it works offline.

## Alternative — Netlify Drop (about 60 seconds, free account needed)

app.netlify.com/drop → drag this whole folder onto the page → you get an HTTPS URL
immediately. Then steps 6–7 above.

## Without any hosting

Put index.html in iCloud Drive and open it from the Files app. It works, but there
is no home-screen icon and no offline caching.

## Updating later

Replace index.html in the repo and bump `const CACHE = 'break-v2'` in sw.js to v3,
otherwise the old cached version keeps loading.
