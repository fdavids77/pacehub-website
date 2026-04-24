# PaceHub Website — Claude Code context

## What this is

Public marketing website for PaceHub — the running club platform.
Lives at https://pacehub.club. Separate from the app repo at
~/projects/pacehub (which is the actual platform for Itheko and
future pilot clubs).

## Purpose

The website exists to:
1. Explain PaceHub to SA running clubs who've never heard of it
2. Socialise the product with committee members at other clubs
3. Be the canonical "here's what we built, here's why" URL that
   Fagmie shares in demos, DMs, and pitches

## Strategic context

The North Star doc for PaceHub's positioning is
~/projects/pacehub/docs/POSITIONING.md. READ IT before making
content changes — it defines the mission statement, competitive
landscape, "where we're ahead" / "where we're behind", and
pricing promises.

Any copy on this site MUST align with POSITIONING.md. If a
proposed change contradicts POSITIONING.md, flag it — do not
silently change the positioning.

## What this site does NOT have

- No Itheko-specific branding (that lives in the app itself)
- No actual login (that's the app)
- No member data (that's the app)
- No backend (pure static HTML, deployed to GitHub Pages)

## Stack

- Plain HTML + embedded CSS (single file, index.html)
- No JS framework, no build step, no npm
- Typography: Google Fonts (DM Serif Display, DM Sans, DM Mono)
- Color palette matches PaceHub app: dark theme, #E53A3C red accent
- Deployed via GitHub Pages with custom domain pacehub.club

## Execution mode

Same as the app repo:
- Auto-accept mode (not plan mode)
- Write directly to disk, NO git commits by Claude Code
- Fagmie commits manually after reviewing in browser preview
- Exception: docs-only edits where Fagmie has approved the diff
  may be committed immediately

## Commit cadence

- At each confirmed-working change: Claude Code prompts
  "Change X is working. Stage and commit?"
- At session end: Claude Code runs git status and asks about
  uncommitted work before ending.

## Repo structure

    pacehub-website/
    ├── README.md           # project readme
    ├── CLAUDE.md           # this file
    ├── CNAME               # GitHub Pages custom domain
    ├── .gitignore
    ├── index.html          # landing page
    └── assets/             # images, favicons (future)

## Commands that matter

    # Preview locally
    python3 -m http.server 8000
    # then open http://localhost:8000

## Deployment

Pushing to main on GitHub auto-deploys via GitHub Pages.
Propagation takes 30s-2min. No manual deploy step.

## Related

- App repo: ~/projects/pacehub
- Positioning doc: ~/projects/pacehub/docs/POSITIONING.md
- Live app (pilot): https://itheko.ddns.net
- Domain registrar: GoDaddy (pacehub.club, pacehub.info)

---

## Project journey

The narrative arc of the whole PaceHub project — origin, pivots, launch, lessons — lives in `~/projects/pacehub/JOURNEY.md`.

Read once for context on why decisions were made the way they were. Refer back at milestones. Update it at major pivots.

## Launch

**This website launched on Friday, 24 April 2026, at ~15:53 SAST.** First verified live via phone on LTE with a valid Let's Encrypt cert issued by GitHub Pages. DNS via GoDaddy (four A records + www CNAME). See the app repo's `JOURNEY.md` for full context.
