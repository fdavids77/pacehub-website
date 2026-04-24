# pacehub-website

Public marketing website for [PaceHub](https://pacehub.club) — a
digital home for South African running clubs.

Live at: **https://pacehub.club**

## What this is

Static HTML landing page. Explains what PaceHub does, who it's
for, what makes it different, and how SA running clubs can get
their club onboarded.

## Local development

    python3 -m http.server 8000
    # open http://localhost:8000

No build step. Edit index.html, save, refresh browser.

## Deployment

Auto-deployed to GitHub Pages from main branch. Push commits,
wait ~60 seconds, live at https://pacehub.club.

DNS: pacehub.club A/ALIAS records point to GitHub Pages IPs.
CNAME file in repo root claims the custom domain.

## Positioning & strategy

The strategic positioning of PaceHub is documented in the app
repository at pacehub/docs/POSITIONING.md. All copy on this
site must align with that document.

## Contact

fagmie@pacehub.club
