# previews

Private design previews for Smoke Turner web clients, served via GitHub Pages at [previews.smoketurner.com](https://previews.smoketurner.com).

## What this is

Each subdirectory is a self-contained, single-file website mockup built as part of a sales outreach package for a prospective client. Previews are shared by direct link only — the root landing page intentionally lists nothing.

## Structure

```
├── index.html          # Landing card (no directory listing)
├── assets/logo.png     # Smoke Turner logo
├── CNAME               # previews.smoketurner.com
├── robots.txt          # Disallow all crawlers
├── .nojekyll
└── <client>/index.html # One mockup per prospect
```

## Current previews

| Path | Business | Niche |
|------|----------|-------|
| `/kupchick/` | Kupchick Heating & Cooling | HVAC |
| `/roofsmart/` | Roof Smart Home Improvement | Roofing |
| `/bruces/` | Bruce's Landscaping Services | Landscaping / excavating |
| `/lt/` | LT Landscaping & Masonry | Landscaping / masonry |
| `/dm/` | D&M Landscaping | Landscape design |

## Conventions

- **Single file per mockup** — inline CSS, no external JS, no external images (inline SVG + CSS gradients only; Google Fonts is the sole external dependency)
- **`noindex, nofollow`** meta on every page + global `robots.txt` disallow — mockups must never appear in search results
- **Real business facts only** — name, address, phone, rating, and services come from public listings; no invented credentials, reviews, or warranties
- **Demo forms** — contact/quote forms are non-functional and labeled as such

## Deployment

Push to `main`; GitHub Pages (legacy build) publishes automatically. HTTPS is enforced. DNS: `previews` CNAME → `smoketurner.github.io` in Route 53.
