# KNUSTrack

**Net-Zero Emissions Platform — KNUST College of Engineering**
Net-Zero Carbon Emission Lab (NCEL) · Kwame Nkrumah University of Science and Technology

KNUSTrack turns the College of Engineering's activity data — procurement spend,
metered electricity, fuel and refrigerant records, and a campus commuting survey — into
a complete, auditable greenhouse-gas inventory across **Scopes 1, 2 and 3**, and presents
it as an interactive dashboard with a costed pathway to **net zero by 2040**.

Baseline: **1,927 tCO₂e** in 2025 · Scope 1 495 · Scope 2 536 · Scope 3 896 · 2023–2025 study.

---

## What's in this folder

| File | Purpose |
|------|---------|
| `index.html` | Landing page — the home of the platform |
| `dashboard.html` | The full interactive dashboard (Executive Summary, Scopes 1–3, Trends, Departments, Commuting, Buildings, Net-Zero Pathway) |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is (**do not delete**) |
| `src/` | The original dashboard file, kept for reference |

Both pages are **self-contained** and run in any modern browser. The only things loaded
from the internet are Google Fonts, Chart.js (from a public CDN) and the KNUST CoE logo,
so an internet connection is needed for charts, fonts and the logo to appear.

---

## Run it locally

**Double-click `index.html`** — it opens in your browser. Click **Open the dashboard** to
enter the platform; the logo and **Home** button in the dashboard bring you back.

> If your browser blocks something when opened directly from disk, run a tiny local server
> instead: open a terminal in this folder and run `python3 -m http.server 8000`, then visit
> `http://localhost:8000`.

---

## Host it on GitHub Pages (free public link)

This gives you a shareable URL like `https://YOUR-USERNAME.github.io/knustrack/`.

### Step 1 — Create a GitHub account
Sign up at <https://github.com> if you don't have one (free).

### Step 2 — Create a new repository
1. Click **+** (top-right) → **New repository**.
2. **Repository name:** `knustrack` (lowercase, no spaces).
3. Set it to **Public**.
4. Leave "Add a README" **unchecked**.
5. Click **Create repository**.

### Step 3 — Upload the files
On the new empty repository page:
1. Click **uploading an existing file**.
2. Drag in **the contents of this folder** — `index.html`, `dashboard.html`, `.nojekyll`,
   `README.md`, and the `src` folder. *(Drag the files themselves, not the enclosing
   `KNUSTrack` folder — GitHub should list `index.html` and `dashboard.html` at the
   top level of the repo.)*
3. Scroll down and click **Commit changes**.

> **Important:** make sure **both** `index.html` **and** `dashboard.html` appear in the
> repository file list before continuing. Large files are sometimes dropped during
> drag-and-drop — if `dashboard.html` is missing, upload it again on its own.

### Step 4 — Turn on GitHub Pages
1. In the repository, go to **Settings** → **Pages** (left sidebar).
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Under **Branch**, select **`main`** and folder **`/ (root)`**, then **Save**.

### Step 5 — Get your link
Wait about a minute, refresh the **Pages** settings screen, and it will show:

> Your site is live at `https://YOUR-USERNAME.github.io/knustrack/`

That opens the landing page. The dashboard is reachable from the buttons, or directly at
`https://YOUR-USERNAME.github.io/knustrack/dashboard.html`.

### If only the homepage opens
This almost always means `dashboard.html` didn't get committed, or Jekyll is interfering:
1. Open `https://github.com/YOUR-USERNAME/knustrack` and confirm `dashboard.html`
   is in the file list next to `index.html`. If not, re-upload it.
2. Confirm the `.nojekyll` file is present (hidden files are often skipped in drag-and-drop).
   If missing: **Add file → Create new file**, name it exactly `.nojekyll`, leave it empty,
   and **Commit**.
3. Test the dashboard URL directly (…/dashboard.html) and hard-refresh (Ctrl/Cmd+Shift+R).

---

## Optional — publish from the command line

```bash
# from inside this folder
git init
git add .
git commit -m "KNUSTrack"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/knustrack.git
git push -u origin main
```
Then enable Pages as in **Step 4**.

---

## The numbers at a glance

- **Total 2025:** 1,927 tCO₂e (Scope 1 495.4 · Scope 2 535.9 · Scope 3 896.1).
- **Largest share:** Scope 3 at 46.5% — commuting (≈797 tCO₂e) plus supply chain (≈91 tCO₂e).
- **Coverage:** 11 buildings (device-level audit), 1,115 students surveyed, 2023–2025 trend.
- **Target:** net zero by 2040 (≈128 tCO₂e/yr), with residual offsets via Enhanced Rock
  Weathering (KREW) under an NCEL MRV framework.

---

© 2026 Net-Zero Carbon Emission Lab (NCEL), KNUST College of Engineering.
Principal Investigator: Dr. Yen Adams Sokama-Neuyam · asokama@knust.edu.gh · +233 24 593 7358
