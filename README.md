# Nook landing page

Static site for Nook — waitlist + privacy policy.

## Files

- `index.html` — landing page (hero, showcase, waitlist card)
- `privacy.html` — privacy policy
- `styles.css` — shared stylesheet (theme mirrors the app's chrome)
- `icon.png` — app icon (1024×1024)
- `screenshots/` — drop product PNGs here; wire them into `index.html`
  feature rows when ready.

## Waitlist form

The form currently uses a `mailto:` fallback. Swap the `action` URL in
`index.html` for a form endpoint (Formspree, Tally, Getform, Buttondown,
etc.) once you pick one.

## Deploying

GitHub Pages + custom domain (`nookbrowser.app`) via the existing
`CNAME` file. Any push to `main` redeploys via
`.github/workflows/deploy.yml`.
