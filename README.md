# Liquid Loaf

Beer is bread that learned to pour.

Happy to sell the domain and the site — [chad@atlascarolina.com](mailto:chad@atlascarolina.com).

## Live

- Preview: [chadakeith.github.io/liquid-loaf](https://chadakeith.github.io/liquid-loaf/)
- Canonical: [liquidloaf.com](https://liquidloaf.com/) once DNS points here

`CNAME` on `main` is `liquidloaf.com`. This token cannot write Pages settings (403). One click: **Settings → Pages → Custom domain → `liquidloaf.com` → Save**. Leave **Enforce HTTPS** on; the cert issues after DNS lands.

### Squarespace Domains records

Replace the current Squarespace parking records (`198.185.159.144/145`, `198.49.23.144/145`, and `www` → `ext-sq.squarespace.com`).

**Apex `@` / `liquidloaf.com` — four A records** (delete the old Squarespace As first):

| Type | Host | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |

Optional IPv6 (recommended with the As):

| Type | Host | Value |
| --- | --- | --- |
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |

**www — one CNAME** (not an A record; must point at the user site, not the repo path):

| Type | Host | Value |
| --- | --- | --- |
| CNAME | `www` | `chadakeith.github.io` |

Do not use a `*.liquidloaf.com` wildcard. Leave nameservers as they are (`ns-cloud-e*.googledomains.com`). After DNS propagates, GitHub issues the HTTPS cert; `www` will redirect to the apex.

## Stack

Static HTML, CSS, and a little JS. GitHub Pages from `main`.

## Photos

Royalty-free beer photography from [Unsplash](https://unsplash.com/license) and [Pexels](https://www.pexels.com/license/), downloaded into `assets/beers/` so nothing depends on a hotlink.
