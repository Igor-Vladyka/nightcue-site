# nightcue-site

Static site for [Nightcue](https://play.google.com/store/apps/details?id=app.nightcue), a paced ear-prompter for Android — a candle for your ear.

Hosts the **privacy policy** required by Google Play, and will house the landing page when v1 ships.

## Live URLs

| Page | URL |
|---|---|
| Privacy policy | https://igor-vladyka.github.io/nightcue-site/privacy.html |
| Landing page | https://igor-vladyka.github.io/nightcue-site/ *(placeholder; landing page comes after v1 launch)* |

## Repo layout

```
nightcue-site/
├── README.md        — this file
├── index.html       — landing page placeholder (links to privacy)
├── privacy.html     — Google Play–compliant privacy policy
└── CNAME            — present only if a custom domain is wired (see below)
```

Everything is **plain static HTML** with inline CSS — no Jekyll, no build step, no dependencies. GitHub Pages serves the files directly. The whole site loads zero third-party resources (no font CDN, no analytics, no trackers) so the privacy-policy claims it makes about the app stay literally true of the page itself.

## How GitHub Pages is configured

- **Source:** Deploy from a branch
- **Branch:** `main` / root (`/`)
- **Custom domain:** none yet — uses the default `*.github.io` URL

To wire a custom domain later:

1. Buy a domain (e.g. `nightcue.io`, `getnightcue.com`, etc. — `nightcue.app` is taken).
2. Add a `CNAME` file at the repo root containing only the domain name (e.g. `nightcue.io`).
3. At the DNS registrar, point an `A` record at GitHub Pages' IPs (185.199.108.153 / 109.153 / 110.153 / 111.153) **or** a `CNAME` record to `<your-github-username>.github.io`.
4. In repo Settings → Pages, set the custom domain and enable "Enforce HTTPS" once propagation finishes.

## Updating the privacy policy

The "Last updated" date at the top of `privacy.html` and the timestamp in the footer should be bumped whenever the policy changes materially — and Google Play wants you to keep it current.

A *material* change is anything that affects what data the app collects, stores, or shares. A typo fix is not material; bumping the date for a typo is fine but not required.

When updating:

1. Edit `privacy.html`.
2. Update the "Last updated" line near the top.
3. Commit with a descriptive message (`privacy: disclose X SDK added in v1.5`).
4. Push to `main` — Pages redeploys in ~1 minute.
5. If the change is material, also update the Data Safety form in Play Console to match.

## License

Content here (the privacy policy text, the eventual landing-page copy) is **All Rights Reserved** by the Nightcue project — feel free to reference the structure and disclosures as a template, but don't copy the body wholesale. No reuse license is granted.
