# foxup — Card Payments, Recharge & Bill Pay

Marketing site for **foxup**, a card payment terminal that also sells mobile
recharge (local & international), UAE bill payments, and gaming/entertainment
vouchers for merchants across Dubai and the UAE.

Hosted on GitHub Pages at **foxuppay.com**.

## Structure

```
index.html            The entire site — single self-contained page (markup + CSS + JS inline)
CNAME                  GitHub Pages custom domain (foxuppay.com)
logo.png               Wordmark logo
POS-Terminal.png       Hero product photo
favicon.ico            Multi-size favicon
site.webmanifest       PWA manifest
robots.txt             Crawler directives (points to sitemap.xml)
sitemap.xml            XML sitemap for search engines
icons/                 Favicons (16/32/48/180/192/512px) + Open Graph share image
logos/                 Carrier, biller, and voucher-brand logos used across the coverage sections
```

## Hosting (GitHub Pages)

This repo is served directly by GitHub Pages from the `main` branch, root
folder. Two pieces make that work together:

1. **Repo settings → Pages** — source set to `main` / `/ (root)`.
2. **`CNAME`** — contains `foxuppay.com`, which is what tells GitHub Pages to
   answer to that custom domain instead of the default
   `sumalvarittakkil.github.io/foxup-website`.

Your domain registrar/DNS still needs to point at GitHub separately — Pages
serving the domain and DNS resolving to Pages are two different steps. At
your DNS provider, add:

- An **A** record for the root (`@`) pointing at each of GitHub Pages' IPs:
  `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- A **CNAME** record for `www` pointing at `sumalvarittakkil.github.io`

DNS propagation can take anywhere from a few minutes to ~24 hours. Once it
resolves, enable "Enforce HTTPS" in repo settings → Pages — GitHub issues the
TLS certificate automatically, but only after it can see the domain
resolving correctly.

## SEO

The `<head>` of `index.html` carries the full on-page SEO layer: title/meta
description, canonical URL, Open Graph + Twitter Card tags, geo tags, and an
`Organization` JSON-LD block. See the SEO growth plan (shared separately) for
the local SEO, content, and off-page roadmap that builds on this foundation.

## Notes

- `icons/mark-square.png` and `uat-artifact.html` are local working files
  (an intermediate favicon source and a saved preview snapshot) — intentionally
  left out of version control since they aren't part of the deployed site.
