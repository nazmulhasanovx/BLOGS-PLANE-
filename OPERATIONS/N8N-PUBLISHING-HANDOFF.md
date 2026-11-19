# n8n / CMS Automation Handoff (Proposed)

Automation should orchestrate research and drafts while human editors retain publication approval.

## Suggested pipeline

1. Trigger from an approved CSV queue or editorial database row with a stable NIM-XXX ID.
2. Fetch editorial brief and retrieve latest research from approved first-party sources.
3. Generate research notes, gap analysis, citations and article draft.
4. Flag uncertain facts, unsupported product details, missing screenshots and unverified SEO metrics.
5. Submit a review packet to a human editor; never treat AI-produced claims as verified evidence.
6. After signoff, create an unpublished draft in the CMS using verified slug, metadata, excerpt and images.
7. Run rendered-page QA: links, canonical, schema, hreflang, sitemap rules, mobile readability.
8. Require a distinct publish approval action; then push live and log the canonical URL.
9. Monitor Search Console, feedback and refresh queue, with rate limits and error handling.

## Required state fields

id, branch, article_path, status, assigned_writer, research_date, sources, reviewer, seo_qa_score, approval_timestamp, cms_draft_id, published_url, published_at, refresh_due, error_details.

## Safety controls

- No auto-sending or publishing without signoff.
- No fake Search Console metrics or invented competitor data.
- No duplicated pages or localization stubs.
- No recharging, payment, or cryptocurrency transaction activity in editorial automation.
- No unapproved changes to unrelated repository branches.
