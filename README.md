# gustrentrodeo-apex-redirect

Apex redirect `gustrentrodeoassociation.com` -> `https://www.gustrentrodeoassociation.com` via GitHub Pages.

The real site is on Cloudflare Pages (project `gustrentrodeo`) at the `www` host.
Wix DNS cannot CNAME/flatten the apex to Cloudflare Pages, so the naked domain
points at GitHub Pages A records, which serve this path-preserving redirect.

DNS at Wix:
  - `CNAME www` -> `gustrentrodeo.pages.dev`
  - apex `A` -> 185.199.108.153 / 185.199.109.153 / 185.199.110.153 / 185.199.111.153

See memory `reference_apestudios_site_cutover`.
