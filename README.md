# CadetCore Marketing Site

Static marketing/landing page for [cadetcore.app](https://cadetcore.app) — the public-facing site for the CadetCore training platform.

## Structure

```
index.html        — Main landing page
styles.css        — Stylesheet (responsive, navy/sea colour palette)
favicon.png       — Site favicon
sea-cadets.png    — Logo
screenshots/      — Feature screenshots used on the landing page
```

## Deployment

Hosted on Plesk at `/var/www/vhosts/cadetcore.app/httpdocs/`. Served as static HTML — no build step required.

To deploy changes: push to `main`, then on the server:

```bash
cd /var/www/vhosts/cadetcore.app/httpdocs/
git pull
```

## Related

The CadetCore application (Next.js) is in a separate repo: [sea-cadet-planner](https://github.com/matstocks/sea-cadet-planner)
