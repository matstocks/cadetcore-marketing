# CadetCore Marketing Site

Static marketing site for [cadetcore.app](https://cadetcore.app) — the public-facing site for the CadetCore training platform.

## Structure

```
index.html        — Home page (hero, feature highlights, how it works, CTA)
features.html     — All 16 features with desktop screenshots
junior.html       — Junior Sea Cadet programme (badges, crest, pennant, RPLE)
mobile.html       — Mobile showcase with phone mockup frames
security.html     — Security, privacy & GDPR compliance
styles.css        — Stylesheet (responsive, navy/sea colour palette)
favicon.png       — Site favicon
sea-cadets.png    — Logo
screenshots/      — Desktop and mobile screenshots (25 total)
```

## Screenshots

Screenshots are generated with Puppeteer against `dev.cadetcore.app` using `generate-marketing-screenshots.mjs` in the [sea-cadet-planner](https://github.com/matstocks/sea-cadet-planner) repo. Names are blurred automatically (except the admin user).

- 18 desktop screenshots (1440x900, 2x DPI)
- 7 mobile screenshots (390x844, 2x DPI)

## Deployment

Hosted on the production server at `/opt/cadetcore/marketing/httpdocs/`. Served as static HTML via nginx — no build step required.

To deploy changes:

```bash
ssh -i cadetcore-ssh-key warsashadmin@172.187.248.79
cd /opt/cadetcore/marketing/httpdocs
sudo git pull
```

Note: CSS is referenced with a `?v=N` cache-busting parameter in the HTML files. Bump the version number when updating `styles.css` to bypass Cloudflare's cache, or purge the cache manually from the Cloudflare dashboard.

## Related

- **CadetCore application** (Next.js): [sea-cadet-planner](https://github.com/matstocks/sea-cadet-planner)
- **CadetCore Hub** (multi-instance management): [cadetcore-hub](https://github.com/matstocks/cadetcore-hub)
