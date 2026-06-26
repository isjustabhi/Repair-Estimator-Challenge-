# Spark Homes Repair Estimator

Mobile-first Progressive Web App for on-site property repair cost estimation. Built for the Spark Homes Developer Contest.

## Live Demo

Deploy to GitHub Pages (Settings → Pages → GitHub Actions), then visit:

`https://<your-username>.github.io/Repair-Estimator-Challenge-/`

## Run Locally

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

No build step. No dependencies to install.

## Approach

Single-page vanilla JavaScript app with static assets. Data model centers on:

- **7 sections** — Interior General, Kitchen, Bathroom, Bedroom, Living/Common, Systems & Structure, Exterior
- **19 collapsible trade groups** with "No Action Needed" per group
- **Configurable room instances** — add/remove/rename Bathrooms, Bedrooms, and Living areas
- **Per-project + global price overrides** — inline edit any unit cost; CSV upload for company-wide schedule
- **Custom line items** — add or hide/delete items per project
- **Deal Analyzer** (creative addition) — ARV, purchase price, holding costs → profit & margin on summary screen
- **Serial OCR** — Tesseract.js attempts to read year/serial from HVAC equipment photos

## Libraries (CDN)

- [Tailwind CSS](https://tailwindcss.com) — styling
- [SheetJS (xlsx-js-style)](https://sheetjs.com) — Excel export
- [JSZip](https://stuk.github.io/jszip/) — ZIP bundling with photos
- [Tesseract.js](https://tesseract.projectnaptha.com/) — serial number OCR

## Features Checklist

| Requirement | Status |
|---|---|
| Multiple saved projects | ✅ |
| 75+ line items, 5+ sections | ✅ |
| 19 collapsible groups | ✅ |
| Bathroom / Bedroom / Living room instances | ✅ |
| Running total + progress bar | ✅ |
| Per-project price override | ✅ |
| Global CSV price schedule | ✅ |
| Add / delete line items | ✅ |
| Photos on all checked items | ✅ |
| Excel + ZIP export | ✅ |
| PWA + offline service worker | ✅ |
| Deal Analyzer (creative) | ✅ |

## Files

| File | Purpose |
|---|---|
| `index.html` | Main application |
| `manifest.json` / `sw.js` | PWA install + offline |
| `Pricing List.csv` | Official price template |
| `Spark Group - Logo.png` | Branding |
| `Submission Writeup.pdf` | Contest writeup |
| `Example App.html` | Reference only (not submitted) |
