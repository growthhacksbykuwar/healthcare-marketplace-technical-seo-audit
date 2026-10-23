Healthcare Website SEO Audit

**Technical SEO case study · Indian surgical-care marketplace · Next.js · YMYL**

A rendering, indexation and competitive-gap audit for a healthcare marketplace whose most valuable pages were invisible to Google.

📄 **[Read the full audit →](./full-audit.md)**

---

## The problem

The site had ~20 treatment pages and hundreds of doctor profiles targeting high-intent queries like *"piles surgery cost Delhi"*. They were indexed but never ranked, and Google showed footer links as their search snippet.

## What I found

| # | Finding | Severity |
|---|---|---|
| 1 | Treatment and doctor pages render **client-side only**. Googlebot gets an empty "Please wait…" shell with no content, title, canonical or meta | 🔴 Critical |
| 2 | WordPress **staging subdomain indexed**, duplicating content | 🟠 High |
| 3 | No cost, city, review or insurance content compared with competitors | 🟠 High |
| 4 | **E-E-A-T red flags:** placeholder avatars, stock "patient" photos, duplicated cards, conflicting trust stats | 🟠 High |
| 5 | No schema and near-zero backlink authority (vs. a category leader at DR ~61) | 🟡 Medium |

## How I diagnosed it

1. **Raw HTML vs. rendered DOM:** compared server responses across page templates to isolate the CSR failure to dynamic routes.
2. **SERP snippet forensics:** footer text used as the description is a strong sign that Google is indexing the unrendered shell.
3. **Index sweep:** found the staging subdomain competing for branded queries.
4. **Competitor teardown:** benchmarked content types, schema and authority against the top 4–5 ranking platforms.
5. **E-E-A-T review:** audited trust signals, which matter especially on a YMYL medical site.

## Recommendations

- **P0:** Move `/disease/*` and `/doctor/*` to SSR/SSG with unique per-page meta.
- **P1:** De-index the staging site; publish and submit the sitemap.
- **P2:** Cost and city pages, real patient stories, medical-reviewer bylines, consistent stats.
- **P3:** `MedicalProcedure`, `Physician`, `FAQPage` and `BreadcrumbList` schema, plus healthcare digital PR.

Each fix includes a **measurable success check**, e.g. `view-source:` shows real content, or `site:staging.` returns 0 results.

## Skills demonstrated

`Technical SEO` · `JavaScript SEO / Next.js rendering` · `Indexation & crawl hygiene` · `Competitive analysis` · `E-E-A-T for YMYL` · `Schema strategy` · `Prioritized roadmaps`

---

*Client details are anonymized. Findings reflect the site at the time of the audit.*
*Want an audit like this for your site? → [Contact me](https://github.com/growthhacksbykuwar)*
