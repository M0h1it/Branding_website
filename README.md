# Star Halal Meat Shop

Marketing website for **Star Halal Meat Shop**, Gurugram — a fresh halal chicken &
mutton butcher serving the city since 1995. It's a plain static site (HTML, CSS,
JavaScript) with no build step, so it runs anywhere: open it locally with Live
Server or push it straight to GitHub Pages.

## Project structure

```
.
├── index.html          ← the entire page (all sections in one file)
├── style.css           ← all styling
├── script.js           ← behaviour: scroll reveal, sticky nav, mobile menu, FAQ accordion
├── site.webmanifest    ← PWA manifest referenced in <head>
└── (images & logos)    ← see below
```

Everything lives in `index.html` — hero, stats, about, products, quality, bulk
orders, how-to-order, reviews, FAQ, contact/map, and footer are all sections inside
that one file. To edit a part of the page, search for its section comment (for
example `<!-- ── 4. FRESH CUTS / PRODUCTS ── -->`) and edit right there.

## Images this site expects

Place these files in the **root of the project** (next to `index.html`) — that's how
they're referenced:

- `favicon1.png`, `favicon-16x16.png`, `favicon-32x32.png`, `apple-touch-icon.png`
- `logo1.png`
- `star_halal_shop.png`
- `boneless_chicken_breast.jpg`
- `Mutton_Curry_Cut.jpg`
- `qr_code.jpeg`

The remaining product and gallery images load from external Unsplash URLs, so they
need no local files.

## Running it

**Local preview:** right-click `index.html` in VS Code and choose *"Open with Live
Server"* (or just double-click the file to open it in a browser). No Ruby, no build,
no setup.

**Deploy on GitHub Pages:** push these files to your repository, then in
`Settings → Pages` set the source to your branch. The site goes live at
`https://<username>.github.io/<repo>/`.

## Tech

- Semantic HTML5 with Schema.org / JSON-LD structured data (LocalBusiness, FAQ,
  breadcrumbs) for SEO
- Open Graph + Twitter Card meta tags for link previews (WhatsApp, Facebook, etc.)
- Vanilla CSS (custom properties, grid, flexbox) — no framework
- Vanilla JavaScript (IntersectionObserver for reveal animations and active-nav
  highlighting) — no dependencies
- Google Fonts: Cormorant Garamond + DM Sans

## Note before deploying

Two asset paths use a leading slash — `/site.webmanifest` and `/qr_code.jpeg`. These
work in Live Server but will 404 on a GitHub Pages **project** site (one served from
a `/<repo>/` subfolder). If you deploy to a project URL, change them to
`./site.webmanifest` and `./qr_code.jpeg` so they resolve in both places.

---

© 2025 Star Halal Meat Shop, Gurugram. All rights reserved.
