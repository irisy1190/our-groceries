# Our Groceries – the app

A shared grocery list for a household, as a web app you add to the iPhone home screen.
Live at **https://irisy1190.github.io/our-groceries/** (hosted free on GitHub Pages, data in Firebase).
It used to be at our-groceries.netlify.app.

## Files

| File | What it is |
|---|---|
| `index.html` | The page and all the styles |
| `app.js` | Everything the app does: list, categories, history, photos, barcode scanner, prices, households |
| `config.js` | The Firebase project settings (safe to be public – access is controlled by `firestore.rules`) |
| `firestore.rules` | Who may read/write what in Firebase. Paste into Firebase console → Firestore → Rules if you change it |
| `sw.js` | Lets the app open offline. **Bump `CACHE` (e.g. `groceries-v18` → `v19`) whenever you change a file**, so phones pick up the update |
| `manifest.json`, `*.png` | Home-screen name and icons |
| `SETUP-WEB.md`, `UPDATE-ACCOUNTS.md` | Older setup notes |

## Publishing a change

1. Edit the files.
2. Bump `CACHE` in `sw.js`.
3. On github.com/irisy1190/our-groceries choose **Add file → Upload files**, drag the changed files in, and **Commit changes**. GitHub publishes them in about a minute.
4. On the phone, close and reopen the app.

## Store prices

Prices and sales come from the `prices/` folder of this same project (GitHub runs it daily, and the Mac
adds Victory and Super-Pharm). The app reads `https://irisy1190.github.io/groceries-prices/prices.json`,
set in the app under ⋯ → Household & invite → Store prices.
