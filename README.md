# Erion's Builds — site source

A static portfolio of the agents and tools I build with Claude. Plain HTML and CSS, no build step.

## Files

- `index.html` — homepage with build cards
- `job-search-agent.html` — Build No. 01 deep-dive
- `styles.css` — shared stylesheet (warm-paper editorial aesthetic)

## Deploying to GitHub Pages

1. Create a new repo on GitHub. Name suggestion: `builds` (so your URL becomes `mexiro.github.io/builds`).
2. Push these three files to the `main` branch.
3. In the repo settings → Pages → Source: select `Deploy from branch` → `main` → `/ (root)`.
4. Wait ~1 minute. Your site will be live at `https://mexiro.github.io/builds/`.

If you want a custom domain later (e.g. `builds.erionmaxhari.com`), add a CNAME file with the domain name and configure DNS — GitHub has docs for this.

## Adding a new build

1. Duplicate `job-search-agent.html` and rename (e.g. `milo-sql-gem.html`).
2. Update the `<title>`, `<meta>`, kicker, h1, standfirst, byline, TOC, and section content. Keep the structural classes — they're styled.
3. In `index.html`, replace one of the `.build.coming` placeholder cards with a real one pointing to the new file. Move the old "latest build" further down the list if you want chronological ordering.
4. Commit and push. GitHub Pages redeploys automatically.

## When to migrate to a framework

You don't need Astro, Jekyll, or anything else until you have ~5 build pages and find yourself copy-pasting headers/footers and getting them out of sync. At that point, the migration is half a day with Astro. Until then, plain HTML wins.

## Design notes

- **Fonts**: Fraunces (display, serif), Inter (body), JetBrains Mono (code/labels) — all loaded from Google Fonts.
- **Palette**: warm paper background `#f6f1e8`, deep ink text, single accent `#2d6a64` (desaturated teal).
- **No JavaScript**: smooth-scroll is CSS-only, animations are CSS keyframes. Total page weight is ~30KB plus fonts.
- **Accessibility**: semantic HTML, sufficient contrast, scales cleanly to mobile.

## Privacy

The Job Search Agent page uses a fictional persona (Alex, junior dev, Neukölln). Nothing in the published rubric is from Marsida's actual setup. Keep it that way for any future builds — pattern public, personal data private.
