# Mortigen Landing Site

This folder contains the static landing site for Mortigen. It presents the game,
its lore hook, platform store links, privacy summary, and legal pages for
players.

## Files

- `index.html`: main landing page
- `privacy.html`: privacy policy
- `terms.html`: terms and conditions
- `assets/css/site.css`: shared responsive styling
- `assets/js/home-i18n.js`: language selector and page translations
- `assets/images/`: landing artwork, store badges, icons, and social assets
- `assets/fonts/`: the RetroFont face used by the site

## Localization

The landing site supports the same 13 language choices used by Mortigen:
Bengali, Basque, Chinese, English, French, German, Hindi, Italian, Japanese,
Korean, Portuguese, Russian, and Spanish.

Visible strings are marked in HTML with `data-i18n`, `data-i18n-alt`,
`data-i18n-aria-label`, `data-i18n-href`, or `data-i18n-src`. Their values live
in `assets/js/home-i18n.js`. Keep that file limited to keys that are actually
referenced by `index.html`, `privacy.html`, or `terms.html`.

## Preview

The site has no build step. For a local preview, run a static server from this
folder:

```bash
python3 -m http.server 8765
```

Then open:

```text
http://127.0.0.1:8765/index.html
```

The legal pages are:

```text
http://127.0.0.1:8765/privacy.html
http://127.0.0.1:8765/terms.html
```

## Deployment

Deploy the whole `landing-site` folder to any static host. The site depends only
on relative local assets, so no build command, bundler, or server-side runtime is
required.

Before deployment, check that:

- Store badge links still point to the current iOS and Android listings.
- Social links still point to official Mortigen accounts.
- `privacy.html` and `terms.html` match the current app behavior.
- All referenced files under `assets/` are included in the deployed folder.

## Asset Rights

All image assets in `assets/images/` are original artwork for Mortigen. All
rights reserved. They may not be reproduced, distributed, or used outside this
project without prior written permission.
