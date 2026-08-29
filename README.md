# foxup — Card Payments, Recharge & Bill Pay

Marketing site for **foxup**, a card payment terminal that also sells mobile
recharge (local & international), UAE bill payments, and gaming/entertainment
vouchers for merchants across Dubai and the UAE.

## Structure

```
Home.html            The entire site — single self-contained page (markup + CSS + JS inline)
logo.png              Wordmark logo
POS-Terminal.png      Hero product photo
favicon.ico           Multi-size favicon
site.webmanifest      PWA manifest
robots.txt            Crawler directives (points to sitemap.xml)
sitemap.xml           XML sitemap for search engines
icons/                Favicons (16/32/48/180/192/512px) + Open Graph share image
logos/                Carrier, biller, and voucher-brand logos used across the coverage sections
```

## Deploying

`Home.html` must be served at the domain root (`/`). Either rename it to
`index.html` for your host's default document convention, or configure the
server to serve `Home.html` as the index — every canonical URL, Open Graph
tag, and the sitemap all assume `https://foxuppay.com/` resolves to this file.

## SEO

The `<head>` of `Home.html` carries the full on-page SEO layer: title/meta
description, canonical URL, Open Graph + Twitter Card tags, geo tags, and an
`Organization` JSON-LD block. See the SEO growth plan (shared separately) for
the local SEO, content, and off-page roadmap that builds on this foundation.

## Notes

- `icons/mark-square.png` and `uat-artifact.html` are local working files
  (an intermediate favicon source and a saved preview snapshot) — intentionally
  left out of version control since they aren't part of the deployed site.
