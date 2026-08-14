# APP_NAME

## About this app

- **Purpose:** APP_DESCRIPTION
- **Audience:**
- **Owner:** APP_OWNER
- **Repo:** APP_REPO
- **Status:** Not yet built

## Getting started

1. **Run locally** — open `index.html` directly in a browser, or serve the folder with a static web server. See [docs/development.md](docs/development.md).
2. **Customize metadata** — replace every `APP_NAME`, `APP_DESCRIPTION`, `APP_OWNER`, and `APP_REPO` (the GitHub repo slug, e.g. `marin-cupa-fees` — used by the Updates section to know which repo's commits to show) placeholder in this file and in `index.html`.
3. **Add app-specific functionality** — build the real workflow into `index.html`, `assets/app.css`, and `assets/app.js`, replacing the starter `#start` section. Leave `#about` and `#updates` in place — see "Standard nav" below.

## Standard nav

Every app built from this template ships with About and Updates in `#app-nav`, and no "Home" tab — a tab shouldn't just point back to what's already showing by default. The app itself must be immediately functional in the default view; move info/how-to/context content into About instead of stacking it above or alongside the tool. `#start`, `#about`, and `#updates` show one at a time, matching the nav — each has `data-tab-section="…"` and `shared/app-shell.js` handles showing/hiding and syncing `aria-current` generically from that, no per-page JavaScript needed. Give any new top-level section the same `data-tab-section` value as `#start` if it belongs in the default view, or a new value (plus a nav link) if it's its own page. `#updates` also needs no JavaScript of its own beyond `data-updates-repo` and `data-app-name` (the latter is what makes the status line read "APP_NAME release notes." once commits load).
4. **Use marin-ui** — prefer existing marin-ui components, tokens, and shell patterns before writing new CSS or JS. See `docs/development.md` for the bundle update process.
5. **Test changes** — keyboard operation, reflow, light/dark contrast, and WAVE accessibility checks. See `docs/development.md`.
6. **Deploy** — document the actual deployment process for this application in `docs/development.md` once it is established.

This project was created from `marin-app-template`, template version `TEMPLATE_VERSION` at time of creation (see `TEMPLATE_VERSION` in this repo). Existing applications do not automatically inherit later template changes — see that repo's `CHANGELOG.md` if you want to selectively adopt something. Shared UI fixes and additions come from `marin-ui` instead, via the sync process in `docs/development.md`.

## Related resources

- [marin-digital-standards](https://github.com/marincountygov/marin-digital-standards) — accessibility, content, brand, and product-design requirements.
- [marin-ui](https://github.com/marincountygov/marin-ui) — the implemented components, tokens, and app shell this project is built on.
- [marin-skills](https://github.com/marincountygov/marin-skills) — AI workflows for building and reviewing Marin applications, including `marin-app-builder`.
