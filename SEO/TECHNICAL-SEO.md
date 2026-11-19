# Technical SEO Implementation Plan

The URLs in the topic CSV are **proposals**, not live website paths. Final hostname and CMS are not confirmed.

## Crawl and information architecture

- Blog index /blog/ -> language index (/blog/en/ and /blog/bn/) -> topical hub -> article.
- Use stable, descriptive, human-readable article URLs; one canonical URL per language version.
- Include only published, indexable canonical URLs in XML sitemaps; submit in Search Console.
- Ensure no accidental noindex/robots blocking, redirect loops, 404 internal links or 5xx errors.
- Pages must render primary article content in crawlable HTML; avoid relying on client-only rendering with no accessible fallback.
- Main navigation and HTML contextual links should make every live article discoverable.
- Use breadcrumbs that reflect actual structure, not fake structured data.

## Per-article markup

- Unique relevant title and H1. Descriptive meta description; no claim of Google using it verbatim.
- Correct meta robots and canonical; avoid canonicalizing the distinct Bangla article to an English article.
- Real named author or responsible organization as appropriate; datePublished/dateModified only when true.
- Appropriate Article or BlogPosting JSON-LD fields when they match visible content: headline, image, datePublished, dateModified, author, publisher, mainEntityOfPage.
- Do not label informational how-to pages as Product or Review unless eligible and accurate. Rich-result eligibility is not guaranteed.
- Use descriptive alt text, compressed responsive images, width/height, and appropriate lazy loading.
- Validate responsive typography, interaction and accessible headings.
- Check Core Web Vitals and page experience on actual devices; do not fake lab scores.

## Product claim controls

The blog must not invent NIMORAI live wallets, verified payments, active infrastructure or chain deployments. Product documentation NIM-571–600 stays behind an engineering evidence gate.

## Multilingual behavior

- Human-edited English/Bangla versions get separate URLs and correct html lang.
- When a real translation pair exists, implement reciprocal hreflang (en and bn; x-default only when appropriate).
- Each language page self-canonicalizes; do not point translations to the English canonical.
- If only English exists, do not emit a fictional Bangla hreflang alternate.
- Do not publish empty auto-translated stubs or redirect users automatically based on IP.

## Validation tools and monitoring

- Google Search Console URL inspection and indexing reports.
- Sitemap status, crawl checks and canonical comparisons.
- Rich Results Test and schema validation when relevant.
- PageSpeed Insights and real-user Core Web Vitals.
- Broken-link crawl and Lighthouse accessibility spot checks.
- Keep a deployment change log for redirects and URL migrations.

## First-party references

https://developers.google.com/search/docs/fundamentals/seo-starter-guide
https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap
https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls
https://developers.google.com/search/docs/appearance/structured-data/article
https://developers.google.com/search/docs/specialty/international/localized-versions
