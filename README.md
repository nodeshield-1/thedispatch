# The Dispatch

Daily cybersecurity & technology briefing.
Live at: https://thedispatch.io

## Stack
- Hosting: Netlify (free tier)
- DNS/Domain: Cloudflare
- Repo: GitHub (auto-deploy on push)

## Folder Structure
```
/
├── index.html          ← redirects to today's article
├── archive.html        ← all past editions
├── about.html          ← about page (TBD)
├── _redirects          ← Netlify routing rules
└── daily/
    ├── 2026-06-07.html ← Day 001
    ├── 2026-06-08.html ← Day 002
    └── ...
```

## Daily Workflow (3 steps)

1. Generate new article HTML with Claude (ask for "Day 00X, [date]")
2. Save it as `daily/YYYY-MM-DD.html`
3. Update `index.html` redirect URL + add entry to `archive.html`
4. Push:

```bash
git add .
git commit -m "Day 002 — 8 Jun 2026"
git push
```

Netlify auto-deploys in ~10 seconds.

## URL Pattern
- Today:   thedispatch.io  (redirects to latest)
- Archive: thedispatch.io/archive.html
- Past day: thedispatch.io/daily/2026-06-07.html

