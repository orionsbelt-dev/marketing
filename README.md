# orionsbelt.dev

Marketing site for Orion's Belt, plus the Google Business Profile copy.

## What is here

- `index.html`, `styles.css`, `favicon.svg`: the one-page site. Plain HTML and CSS, no build step and no dependencies.
- `CNAME`: tells GitHub Pages to serve the site at `orionsbelt.dev`.
- `.nojekyll`: tells GitHub Pages to serve the files as they are.
- `google-business-profile.md`: description, categories, services, and the first four posts for the Google Business Profile.

## Stack

Static HTML and CSS hosted on GitHub Pages. It is free, deploys on every push to `main`, and handles the custom domain and HTTPS certificate. To preview locally, open `index.html` in a browser, or run:

```bash
python3 -m http.server 8000
```

## Going live

1. In the repo on GitHub, go to Settings > Pages, choose "Deploy from a branch", branch `main`, folder `/ (root)`.
2. At the domain registrar for `orionsbelt.dev`, add these DNS records:
   - Four `A` records for `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record for `www` pointing to `orionsbelt-dev.github.io`
3. Back in Settings > Pages, wait for the DNS check to pass, then tick "Enforce HTTPS". Every `.dev` domain requires HTTPS in all browsers, so the site will not load until the certificate is issued.
4. Optional: verify the domain under the organization's Settings > Pages so nobody else can claim it on GitHub.

## Placeholders to fill in

- **Booking link:** every "Book a call" button points at `https://cal.com/orionsbelt/intro`. Replace it with the real scheduling link (search `index.html` for `cal.com`).
- **Email:** the contact line uses `hello@orionsbelt.dev`. Set up that address or change it.
- **About Clark:** the about section has a short placeholder bio and a `TODO(Clark)` comment for background and a photo.

## Writing style

No em dashes or en dashes anywhere in the copy. Use "to" for ranges ("$1,500 to $3,000").
