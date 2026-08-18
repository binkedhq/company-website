# binked.org

Static company website for binked UG (haftungsbeschränkt). Plain HTML/CSS, no build step, no JavaScript, no cookies, no external requests (fonts are system fonts — deliberately, to keep the site GDPR-clean).

## Pages

- `index.html` — landing page (English)
- `impressum.html` — Impressum per § 5 DDG (German)
- `datenschutz.html` — privacy policy incl. GitHub Pages hosting notice (German)
- `404.html` — served automatically by GitHub Pages for unknown URLs

## Deploying to GitHub Pages

1. Push this repository to GitHub.
2. Repository **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)`.
3. Custom domain: the `CNAME` file already contains `binked.org`. In Settings → Pages, enter `binked.org` as the custom domain and enable **Enforce HTTPS** once the certificate is issued.

### DNS records for binked.org

At your DNS provider:

| Type  | Name | Value |
|-------|------|-------|
| A     | `@`  | `185.199.108.153` |
| A     | `@`  | `185.199.109.153` |
| A     | `@`  | `185.199.110.153` |
| A     | `@`  | `185.199.111.153` |
| CNAME | `www` | `binkedhq.github.io` |

With both configured, GitHub redirects `www.binked.org` → `binked.org`.

## Maintenance notes

- **VAT ID (USt-IdNr.):** not yet issued. Once it arrives, uncomment the prepared block in `impressum.html` (search for `Umsatzsteuer-ID`) and fill in the number.
- **Favicon:** `favicon.svg` (Chrome, Edge, Firefox) with `favicon.png` (32×32) as fallback for Safari and older browsers. Optional: render a 180×180 `apple-touch-icon.png` from the SVG for iOS home-screen bookmarks and add `<link rel="apple-touch-icon" href="apple-touch-icon.png">`.
- **Footer year:** static (`© 2026`) — bump it in the four HTML files at year end, or leave the founding year.
