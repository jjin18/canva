# canva-quotes-web

**Static site only** — `index.html` + JSON. Safe for [Vercel](https://vercel.com): no Python, no build step.

## Deploy on Vercel (new project)

1. Create a **new** empty GitHub repository (e.g. `canva-quotes-web`) and push **this repo only**:
   ```powershell
   cd C:\Users\jiahu\canva-quotes-web
   git init
   git add .
   git commit -m "Initial static site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USER/canva-quotes-web.git
   git push -u origin main
   ```
2. In Vercel: **Add New Project** → Import that repo.
3. Leave **Framework** as default / Other, **Build** empty, **Root** `.` (repository root).
4. Deploy. Vercel serves `index.html` at `/`.

## Update the quotes

Run the scraper from the sibling **`canva-scraper`** repo (see that repo’s README). It writes into this folder. Then commit and push **this** repo to refresh the live site.

## Files

| File | Purpose |
|------|--------|
| `index.html` | Main page |
| `canva_quotes.html` | Same HTML (optional mirror) |
| `canva_quotes.json` | Raw data |
