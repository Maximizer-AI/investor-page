# Maximizer AI — Investor One-Pager

Static site hosting the investor one-pager PDF at **[invest.maximizer.ai](https://invest.maximizer.ai)**.

Hosted on GitHub Pages. Any push to `main` auto-deploys within ~1 minute.

## How to Update the PDF

1. Replace `maximizer-one-pager.pdf` in the repo root with the new file (keep the same filename)
2. Commit and push to `main`
3. Wait ~1 minute — the new PDF is live at https://invest.maximizer.ai

```bash
# Quick update from terminal:
cp /path/to/new-file.pdf maximizer-one-pager.pdf
git add maximizer-one-pager.pdf
git commit -m "Update investor one-pager"
git push
```

## Initial Setup (one-time)

1. Create the repo `Maximizer-AI/investor-page` on GitHub
2. Push this code to `main`
3. Go to repo **Settings > Pages** — set source to **GitHub Actions**
4. Add DNS CNAME record: `invest.maximizer.ai` → `maximizer-ai.github.io`
5. (Optional) Add CNAME: `investment.maximizer.ai` → `invest.maximizer.ai`
6. In repo **Settings > Pages > Custom domain**, enter `invest.maximizer.ai` and enable **Enforce HTTPS**

## Structure

```
index.html                 # Landing page with embedded PDF viewer
maximizer-one-pager.pdf    # The PDF file (replace this to update)
CNAME                      # Custom domain config
.github/workflows/deploy.yml  # Auto-deploy on push to main
```
