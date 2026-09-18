# Porter & Co. Plumbing

Single-page marketing site for Porter & Co. Plumbing, Tulsa, OK.

- `index.html` holds the whole site (home, services, about, contact, privacy)
  with no build step and no dependencies beyond Google Fonts.
- `images/` holds photos. See `images/README.md` for the filenames the page
  looks for.
- `.github/workflows/pages.yml` publishes the site to GitHub Pages on every
  push to `main`.

## Going live

1. In the repository settings open **Pages** and set **Source** to
   **GitHub Actions** (one-time step).
2. Merge to `main`. The workflow deploys to
   https://futurexrp.github.io/PorterWebsite/ within a minute or two.

To use a custom domain, add it under **Settings → Pages → Custom domain**
and point the domain's DNS at GitHub Pages.

## Editing

Open `index.html` in any editor. Phone number, hours, address, and license
number appear in a few places each, so search the file when changing them.
