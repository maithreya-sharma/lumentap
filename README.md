# LumenTap

Tap any spot on a photo and the whole image re-exposes so that spot lands at a target brightness, like tap-to-meter on a phone camera. Runs entirely on the device; photos never leave the phone.

## Files

```
index.html             the app
manifest.webmanifest   name, icon, full-screen launch
sw.js                  offline support
icons/                 home screen icons
```

## Put it online with GitHub Pages

1. Create a new public repository on GitHub, named `lumentap`.
2. Upload all the files above, keeping the `icons` folder. (On github.com: Add file → Upload files, then drag the whole unzipped folder's contents in.)
3. Go to Settings → Pages. Under "Build and deployment", set Source to "Deploy from a branch", Branch to `main`, folder `/ (root)`, and save.
4. After a minute the site is live at `https://<your-username>.github.io/lumentap/`.

## Install on iPhone

1. Open that link in **Safari** (other browsers can't add web apps on iOS).
2. Tap Share → **Add to Home Screen** → Add.
3. Open LumenTap from the home screen once while online, so it caches itself for offline use.

## Using it

- **Open photo** picks from your library.
- Tap a spot to meter on it. The **Spot target** slider sets how bright that spot should end up.
- **Hold to compare** shows the original.
- **Save full size** prepares the full-resolution photo, then **Save to Photos** opens the share sheet. Choose **Save Image**.

Exports are capped at about 16 megapixels, which is the canvas limit in iOS Safari. 12 MP iPhone photos save at full size; 24 or 48 MP photos are scaled down slightly. The saved file doesn't keep the original's date and location.

## Updating

After changing any file, bump `VERSION` in `sw.js` (for example to `lumentap-v2`) and push. The installed app picks up the new version the next time it is opened online.
