# Nook landing page

Static site for the Nook beta landing + privacy policy.

## Files

- `index.html` — landing page (hero, showcase, download card)
- `privacy.html` — privacy policy
- `styles.css` — shared stylesheet (theme mirrors the app's chrome)
- `icon.png` — app icon (1024×1024)
- `screenshots/` — product shots. Drop PNGs named `home.png`,
  `spaces.png`, `shield.png`, `palette.png`, `split.png`,
  `preview.png`. Landing falls back to broken-image placeholders
  until you drop them in.

## Deploying

### Option 1: Cloudflare Pages / GitHub Pages (free, fast)

1. Push this folder to a GitHub repo (`kuraydev/nook-website`).
2. Cloudflare Pages → Create Project → connect the repo → build
   command empty, output dir `/`.
3. Add your domain — either `nook.coursion.studio` (subdomain of
   your existing `coursion.studio`) via a CNAME, or a freshly-bought
   `.app` / `.com`.

### Option 2: Coursion subdomain (fastest, matches Aistats/Knack)

1. Drop a `CNAME` file in this folder containing `nook.coursion.studio`
2. Deploy to GitHub Pages OR Cloudflare Pages pointing the subdomain
   at the repo.

## Screenshots

Ships with stylized SVG mockups (`home.svg`, `spaces.svg`,
`shield.svg`, `palette.svg`, `split.svg`, `preview.svg`) so the site
deploys with visuals from the start. SVGs scale cleanly and render
crisp at any size.

### Swapping in real captures

1. Open the Nook app and take clean 1780×1160 screenshots of:
   - **home** — fresh tab, Claude or whatever, sidebar open with a
     space pill row at the bottom
   - **spaces** — space menu open (right-click a pill) with the
     theme / color picker visible
   - **shield** — shield popover open on a site with live stats
   - **palette** — ⌘K command palette with fuzzy results
   - **split** — split view with two tabs side-by-side
   - **preview** — hover preview card over a background tab
2. Save as PNG at 1780×1160 (exactly matches the `width`/`height`
   attrs in `index.html`; Retina-crisp at 2× DPR).
3. Replace either the SVG file (keep the name `home.svg` etc.) or
   rename to `.png` and `sed -i '' 's|.svg"|.png"|g' index.html`.
