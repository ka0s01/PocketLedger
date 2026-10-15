# PocketLedger

A responsive, installable personal expense tracker designed for phone and laptop. Static site; no backend or paid database required.

## Features
- Add, edit, delete and search expenses, with amount, category, date and optional note.
- Month-by-month navigation, monthly total, daily average, transaction count and top category.
- Interactive spending trend and category doughnut chart.
- Category breakdown, largest expense, previous-month comparison and six-month history.
- INR, USD, EUR, GBP, JPY and AED display currencies.
- JSON backup export and restore on another device.
- Responsive mobile layout and PWA install support.
- Offline app shell after first visit (Chart.js and Google Fonts may need internet).
- Data saved in browser `localStorage`; no account, server, or external database.

## Run locally
Open `index.html` in a browser for basic testing. For service worker/PWA behavior, use a local server:
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000`.

## Deploy free on Vercel
1. Unzip the project.
2. Create a GitHub repository and upload the files in this folder to its root.
3. In Vercel, choose **Add New → Project**, import the repository.
4. Framework preset: **Other**. Build command: leave empty. Output directory: `.` (or leave default if detected as static).
5. Deploy. No environment variables or paid services are needed.

Alternatively, install Vercel CLI and run `vercel` from this directory.

## Use on phone and laptop
Open the deployed HTTPS URL on both devices. On mobile, use the browser's **Add to Home Screen / Install app** option. The site is responsive.

**Important data note:** localStorage belongs to a specific browser profile on a specific device. It does not automatically sync between phone and laptop. To move data, use **Export backup** on one device and **Import backup** on the other. Keep regular backups; clearing browser data can erase your entries. If automatic multi-device sync becomes necessary, a free-tier hosted database plus authentication can be added, but that requires a user account and backend configuration.

## Costs and privacy
The app itself is static and needs no paid API or database. Vercel's free tier is suitable for personal experimentation, subject to its current limits/terms. Transactions remain in the browser unless you export a backup. Chart.js and Google Fonts load from third-party CDNs; the core app remains usable without charts/fonts if those services are unavailable.
