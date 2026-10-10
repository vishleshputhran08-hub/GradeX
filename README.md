# GradeX — Diploma Result & Grade Calculation System

A single-file static web app for Govt. Polytechnic Bantwal that computes diploma
grades/marks, stores records locally, and exports results to CSV/Excel/PDF.

Everything (markup, styles, logic, logo) lives in `index.html` — no build step,
no server, no database. Data is persisted in the browser via `localStorage`.

## Features

- Grade & result calculation for diploma subjects (custom grade scale)
- Student records with photo, search, and history
- Dashboard with stats and visual breakdowns
- Export to CSV and Excel (SheetJS), print-ready report view
- Light/dark theme, responsive layout, animated UI
- All data stays on the user's device (localStorage)

## Run locally

Just open the file:

```bash
index.html
```

Or serve it (recommended, avoids any browser file:// restrictions):

```bash
npx serve .
# or
python -m http.server 8000
```

Then visit http://localhost:8000

## Deploy on GitHub Pages

Deployment is automated by [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml).

1. Push these changes to `main` on GitHub.
2. Open the repo → **Settings → Pages**.
3. Under **Build and deployment → Source**, select **GitHub Actions**.
4. Push to `main` (or run the workflow manually from the **Actions** tab).
5. Your site is published at `https://<username>.github.io/GradeX/`.

Why it previously failed: the app was committed as
`gradex_student_result_system.html`, so GitHub Pages had no `index.html` at the
repository root and returned a 404. It has been renamed to `index.html`.

## Project structure

```
.
├── index.html                  # the entire application
├── .nojekyll                   # skip Jekyll processing on Pages
├── .github/workflows/deploy.yml # GitHub Pages deploy workflow
└── README.md
```
