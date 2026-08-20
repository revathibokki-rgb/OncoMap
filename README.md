# OncoMap

**Precision Oncology, Simplified.**

OncoMap is a research/learning web app built around a structured 50-biomarker dataset. It connects:

**Cancer → Biomarker → Alteration → Diagnostic testing → Example therapy → Evidence → Clinical trials**

## Included

- 50 structured biomarker records
- Search across biomarker, cancer, alteration, testing and therapy fields
- Filters for biomarker type and evidence level
- Biomarker detail pages
- Biomarker → therapy relationship views
- Diagnostic testing fields
- Local shortlist/favourites using browser localStorage
- Compare up to 4 biomarkers
- Live ClinicalTrials.gov API v2 search
- Clinical trial status filtering
- Learning module + quiz
- Responsive mobile/desktop UI
- PWA manifest and service worker
- GitHub Pages deployment workflow
- Original CSV + JSON dataset included

## Important scope

This is an educational/research prototype, not a diagnostic, treatment-selection or medical-advice tool. The dataset is curated for the project and should not be treated as a substitute for current regulatory labels, guidelines, companion-diagnostic authorisations, or clinical-trial eligibility criteria.

## Run locally

Because this is a static app, a local HTTP server is recommended so the service worker works correctly.

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Deploy with GitHub Pages

1. Create a GitHub repository named `oncomap`.
2. Upload all files in this folder to the repository.
3. Push them to the `main` branch.
4. In **Settings → Pages**, select **GitHub Actions** as the source.
5. The included workflow deploys the static site automatically.

## Deploy with Vercel

Upload this folder or its ZIP to Vercel. No build command is required because the app is static HTML/CSS/JS.

## ClinicalTrials.gov integration

The app uses the public ClinicalTrials.gov API v2 endpoint:
`https://clinicaltrials.gov/api/v2/studies`

The search is read-only. Trial records are opened on ClinicalTrials.gov for the authoritative current record.

## Project structure

- `index.html` — complete application UI and client logic
- `data.json` — structured 50-record dataset
- `data.csv` — original tabular dataset
- `manifest.webmanifest` — installable PWA metadata
- `sw.js` — offline shell caching
- `assets/icon.svg` — app icon
- `.github/workflows/deploy.yml` — GitHub Pages deployment
