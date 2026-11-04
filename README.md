# SADC Christmas Championship: Affiliate Leaderboard

Static leaderboard for the Weltrade Africa affiliate performance competition. No build step, no backend. Hosted on GitHub Pages.

## What it shows

Each affiliate gets a score out of 100 from four KPIs, each measured against the best affiliate:

| KPI | Weight |
|---|---|
| Active clients | 35% |
| FTDs | 25% |
| SpreadPay | 25% |
| Net deposit | 15% |

KPI points = (your result / best result among all affiliates) x weight. The top 3 scores closest to 100 are selected. Ties go to more FTDs, then higher net deposit.

The page also shows a launch countdown to the competition start (15 November 2026) and a "Standings open soon" message until then.

## Files (all in the root, not in a folder)

- `index.html`: the leaderboard page. It includes sample data, so it works on its own.
- `README.md`: this file.
- `partners-data.js` (optional): the real daily data, exported from the private admin page. When uploaded next to `index.html`, it replaces the sample data.

The file must be named exactly `index.html`, lowercase. Never upload `admin.html`.

## First publication

1. Go to github.com and sign in.
2. Click **New repository**. Name it `SADC-Christmas-Championship` (GitHub does not allow spaces). Set it to **Public**.
3. On the empty repository page, click **uploading an existing file**.
4. Drag in `index.html` and `README.md`.
5. Commit message: `initial leaderboard`. Click **Commit changes**.
6. Go to **Settings > Pages**. Source: **Deploy from a branch**. Branch: `main`. Folder: `/ (root)`. Click **Save**.
7. Wait 2-3 minutes, then refresh. The live URL appears at the top: `https://<user>.github.io/SADC-Christmas-Championship/`
8. Open the URL on a phone before sharing it.

## Daily update

1. Open `admin.html` on your own computer and load the day's CSV (`id, country, net, ftd, active, spread`).
2. Check the panel, untick "sample data", click **Export partners-data.js**.
3. In the repository click **Add file > Upload files**, drag in the new `partners-data.js` and commit. It replaces the old one.
4. The live page refreshes within a minute or two.

## Before sharing

- The sample data in the page is for preview only. Upload a real `partners-data.js` before the competition starts.
- Check that no real FTD, deposit or spread figures appear in the page source. The default export contains percentages only.
- Open the link on a phone and confirm rows stack cleanly.
