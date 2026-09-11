# Facility Log — Maintenance & Upkeep Tracker

A single-page, no-install tool for logging and tracking office and warehouse
facility work: routine cleaning, repair requests, and incident reports —
with a dashboard and downloadable CSV reports.

It's one self-contained file (`index.html`) with no backend and no
build step, so it runs straight from GitHub Pages.

**Note on data:** everything is stored in your browser's local storage.
It stays on the device/browser you're using — it is not shared between
people or synced anywhere. Use the "Export CSV" / "Download full report"
buttons regularly to keep a shared copy, or see "Going further" below if
you later need multi-user syncing.

## Run it locally

Just open `index.html` in a browser. No server needed.

## Put it on GitHub

1. Create a new repository on GitHub (e.g. `facility-log`).
2. Add `index.html` (and this `README.md`) to the repo, then commit and push:
   ```
   git init
   git add index.html README.md
   git commit -m "Add facility maintenance tracker"
   git branch -M main
   git remote add origin https://github.com/<your-username>/facility-log.git
   git push -u origin main
   ```
   (Or just drag the files into the GitHub web UI's "Add file → Upload files".)

## Turn on GitHub Pages (to get a shareable link)

1. In the repo, go to **Settings → Pages**.
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Set **Branch** to `main` and folder to `/ (root)`, then **Save**.
4. After a minute, your site will be live at:
   `https://<your-username>.github.io/facility-log/`

## Using it

- **Dashboard** — open counts across all three logs, plus a "Needs attention"
  list of high-priority repairs and serious/critical incidents.
- **Cleaning / Repairs / Incidents tabs** — click "+ Log …" to add an entry.
  Each table lets you filter, change status inline, and delete an entry.
- **Export CSV** on any tab downloads just that log. **Download full report
  (CSV)** on the dashboard downloads everything combined.
- **Print / save as PDF** on the dashboard opens the browser print dialog
  with a clean, form-free layout — choose "Save as PDF" as the destination
  for a PDF report.

## Going further

If down the line you need the whole team to see the same data (not just
one browser), the natural next step is adding a small shared backend —
for example a free-tier database service — behind the same interface.
That's a bigger change than this simple version, so it's left out for now,
but the current data model (three lists of plain records) would carry
over directly.
