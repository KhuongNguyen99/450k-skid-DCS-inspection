# 450k Skid DCS Inspection

Single-page offline-capable inspection application for Siemens ET 200SP / PRONETA Basic.

**Live site (after GitHub Pages is enabled):** https://khuongnguyen99.github.io/450k-skid-DCS-inspection/

## Features

- Work instructions and three checklists on one page: **Modules (15)**, **Valves (13)** and **Sensors (13)**.
- Seven distinct initial skids, with independent test data. Create additional inspections with **+ New checklist**.
- Inspector name, skid name and inspection date for each record.
- Automatic results for valve checks and an inspection progress summary.
- One-click download of the work instruction PDF (embedded; works offline).
- Download current skid results as a multi-page PDF with skid name, header and footer, or as CSV / JSON.
- Export all skids as a JSON backup; restore later.
- **All inspection data stays in the browser's localStorage.** No database, account sign-in, external analytics or network requests are used by the page.

## Usage

Open `index.html` in a browser, or visit the published GitHub Pages URL. Select a skid or create a new checklist, fill the results, and export a backup.

LocalStorage is **specific to each browser profile/device**. Clearing browser site data or using private browsing may erase local inspections; using the site in a different browser or using the downloaded file can create a separate data set. Export the **All skids · JSON backup** file regularly and import it when needed.

## GitHub Pages

This repository includes `.github/workflows/pages.yml`, which deploys the static website on every push to `main`. To enable it initially, open **Settings → Pages → Build and deployment** and choose **GitHub Actions** as the publishing source. The site then deploys on the next workflow run.

## Files

- `index.html`: complete app, all checklist templates and an embedded work instruction PDF
- `.github/workflows/pages.yml`: GitHub Pages workflow

**Safety:** An I/O functional test does not constitute calibration, controller-logic validation, or safety-function validation. Operate pneumatic actuators and Ex circuits only under authorized safe conditions.