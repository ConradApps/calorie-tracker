# Calorie Tracker

A clean calorie tracking PWA + Android APK, built with the same swipe-pager
architecture as the Lyfts workout tracker.

## Features

- **Today** — Log meals with calories, live ring progress, delete entries
- **Calendar** — Monthly view with colour-coded days (green/amber/red)
- **Settings** — Set daily calorie goal, choose Weight Loss or Weight Gain mode
- Swipe left/right between tabs (same animation as workout tracker)
- 100% local storage — works offline on iPhone (PWA) and Android (APK)

## Repo structure

```
index.html          ← The full app (single file)
manifest.json       ← PWA manifest
sw.js               ← Service worker (offline support)
capacitor.config.json
package.json
.github/workflows/build-apk.yml  ← Auto-builds APK on push to main
www/                ← Capacitor web dir (copy of root files)
```

## iPhone (PWA)

1. Host via GitHub Pages (Settings → Pages → main / root).
2. Open the Pages URL in Safari on iPhone.
3. Share → Add to Home Screen.

## Android APK

1. Push to `main` → GitHub Actions builds `CalorieTracker-debug.apk`.
2. Open the repo **Releases → latest** on your Android phone.
3. Tap the APK to download, then install (allow "Install unknown apps" first time).

## Updating

Edit `index.html`, commit to `main`. The APK rebuilds automatically.
Re-download and install over the existing app (your data is preserved in local storage).

## Identity

- App name: **Calorie Tracker**
- Package ID: **com.calories.app**

Change either in `capacitor.config.json` (delete `android/` if it was committed so it regenerates).
