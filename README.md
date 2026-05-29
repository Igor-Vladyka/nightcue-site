# nightcue-site

Static site for [Nightcue](https://play.google.com/store/apps/details?id=app.nightcue), a paced ear-prompter for Android — a candle for your ear.

Hosts the privacy policy and landing page.

## Live URLs

| Page | URL |
|---|---|
| Landing page | https://igor-vladyka.github.io/nightcue-site/ |
| Privacy policy | https://igor-vladyka.github.io/nightcue-site/privacy.html |

## Repo layout

```
nightcue-site/
├── README.md
├── index.html       — landing page
└── privacy.html     — Google Play–compliant privacy policy
```

Plain static HTML with inline CSS — no Jekyll, no build step, no dependencies. GitHub Pages serves the files directly. The site loads zero third-party resources (no font CDN, no analytics, no trackers), so the claims the privacy policy makes about the app stay true of the page itself.

## GitHub Pages

- Source: Deploy from a branch
- Branch: `main` / root (`/`)

## Updating the privacy policy

Bump the "Last updated" date in `privacy.html` whenever the policy changes materially. A material change is anything that affects what data the app collects, stores, or shares.

1. Edit `privacy.html`.
2. Update the "Last updated" line near the top.
3. Commit, push to `main` — Pages redeploys in ~1 minute.
4. If the change is material, update the Data Safety form in Play Console to match.

## License

All rights reserved. Reference the structure and disclosures as a template if useful; don't copy the body wholesale.
