# Zoko — Fridge Tracker

A single-page app that tracks food in your fridge/freezer/pantry, reads grocery
receipts, suggests recipes from what's expiring, and charts your grocery spending.
It runs entirely in the browser — no server, no build step. Your data is saved in
the browser's own local storage on the device you use.

## Files

- `index.html` — the whole app.
- `ocr/` — the offline receipt-photo reader (Tesseract engine + English data).
  Needed only for the "read a receipt photo" feature; the rest of the app works
  without it.
- `.nojekyll` — tells GitHub Pages to serve every file as-is.

## Publish it on GitHub Pages

1. Create a new **public** repository on GitHub.
2. Upload every file here, keeping the `ocr/` folder as a folder.
3. In the repo, go to **Settings → Pages**, set **Source** to *Deploy from a
   branch*, choose the `main` branch and the `/ (root)` folder, and save.
4. After a minute your site is live at
   `https://<your-username>.github.io/<your-repo>/`.

## Notes

- The "Export" button from the original Claude artifact stays hidden here — that
  one feature relied on Claude's runtime and isn't available on a plain web host.
  Everything else works.
- Because data lives in the browser, each browser/device keeps its own separate
  inventory.
