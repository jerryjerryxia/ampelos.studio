# Ampelos Studio — ampelos.studio

The official site for **Ampelos Studio**, the independent game studio of Jerrix.

The homepage is dedicated to the studio's debut title, **Endless Summer Syndrome** (无休夏日综合症) — a surreal psychological visual novel, coming soon to Steam.

## Structure

- `index.html` — Endless Summer Syndrome landing page (hero, `#story`, `#features`,
  `#gallery`, `#wishlist`, `#more` "More Games", `#about`).
- `presskit.html` — press kit: fact sheet, description, features, screenshots, logo, credits, streaming permission. Downloadable asset bundle at `assets/games/ess/ess-presskit.zip`.
- `the-faded.html` — *The Adolescence of a Lunatic* project page.
- `once-upon-a-spring.html` — *Once Upon a Spring* project page.
- `css/home.css` — design system + page styles.
- `js/home.js` — language preference, sticky nav, mobile menu, nav dropdowns, scroll
  reveals, scroll-spy, gallery lightbox, ambient story video, ambient background music.
- `assets/games/ess/` — Endless Summer Syndrome web art (optimized from the game build),
  plus the favicons, the `og.jpg` social card, the `polyhedron.webm` ambient video, and the
  downloadable `ess-presskit.zip`.
- `assets/images/` — art for the other two projects.
- `assets/audio/endless_summer_time.mp3` — ambient background music ("Endless Summer Time").
- `favicon.ico` — root fallback favicon.
- `zh/` — Simplified-Chinese mirror of all four pages (`zh/index.html`, `zh/presskit.html`, `zh/the-faded.html`, `zh/once-upon-a-spring.html`). Shares `css/`, `js/`, and `assets/` via `../` — nothing is duplicated except the HTML.

## Localization

- English is the default, served at the root (`/`). Simplified Chinese lives under `/zh/`.
- Each page links to its counterpart via the `EN` / `中文` switcher in the nav
  (`[data-lang-switch]`). Clicking it records the choice in `localStorage`; on a later
  visit, a returning visitor who previously switched is redirected to their language.
  Otherwise the page is served as-is — first-time visitors always get the language they
  landed on.
- Every page cross-declares both languages with `<link rel="alternate" hreflang>` (`en`, `zh-Hans`, `x-default`) for SEO.
- When editing copy, update **both** the English page and its `zh/` counterpart.

## Deployment

Static site, no build step — the repo root is the document root.

Hosted on **Netlify** at the custom domain `www.ampelos.studio`, deployed from `main` in
this repo. Not GitHub Pages.

> This repo was renamed from `jerryjerryxia.github.io` to `ampelos.studio`, so it is no
> longer the account's GitHub Pages user site. Hosting was unaffected — Netlify tracks the
> repo by ID, not by name.

## Notes

- Hero, gallery, and social images are web-optimized exports of the game's key art.
- Jerrix's personal site is a separate repo,
  [`jerryjerryxia/jerrix.studio`](https://github.com/jerryjerryxia/jerrix.studio), sharing
  this site's design system.
