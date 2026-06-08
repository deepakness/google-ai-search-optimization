# Google AI Search Principles

Use this reference for source-grounded reasoning about Google AI Overviews, AI Mode, and related Search guidance.

## Contents

- Source Map
- Mental Model
- Recommendations
- Content
- AI-Assisted Content
- Technical Foundation
- JavaScript
- Media
- Structured Data
- Ecommerce and Local
- Agentic Experiences
- Myth-Busting

## Source Map

Primary guide:
- Google guide to optimizing for generative AI Search: `https://developers.google.com/search/docs/fundamentals/ai-optimization-guide`

Core Search and SEO sources:
- Search Essentials: `https://developers.google.com/search/docs/essentials`
- Technical requirements: `https://developers.google.com/search/docs/essentials/technical`
- Spam policies: `https://developers.google.com/search/docs/essentials/spam-policies`
- SEO Starter Guide: `https://developers.google.com/search/docs/fundamentals/seo-starter-guide`
- Helpful, reliable, people-first content: `https://developers.google.com/search/docs/fundamentals/creating-helpful-content`
- Guidance on AI-generated content: `https://developers.google.com/search/docs/fundamentals/using-gen-ai-content`
- How Google Search works: `https://developers.google.com/search/docs/fundamentals/how-search-works`
- Developer guide to Search: `https://developers.google.com/search/docs/fundamentals/get-started-developers`
- Maintaining SEO: `https://developers.google.com/search/docs/fundamentals/get-started`

Technical and appearance sources:
- Crawl budget: `https://developers.google.com/crawling/docs/crawl-budget`
- JavaScript SEO: `https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics`
- Page experience: `https://developers.google.com/search/docs/appearance/page-experience`
- Image SEO: `https://developers.google.com/search/docs/appearance/google-images`
- Video SEO: `https://developers.google.com/search/docs/appearance/video`
- Indexable file types: `https://developers.google.com/search/docs/crawling-indexing/indexable-file-types`
- Business details: `https://developers.google.com/search/docs/appearance/establish-business-details`

Commerce, local, and agentic sources:
- Merchant Center product upload methods: `https://support.google.com/merchants/answer/11586438`
- Business Agent overview: `https://support.google.com/brandprofile/answer/16410382`
- Agent-friendly websites: `https://web.dev/articles/ai-agent-site-ux`
- Universal Commerce Protocol: `https://ucp.dev/latest/`

## Mental Model

Google's guidance frames AI Overviews and AI Mode as part of Google Search, not a separate answer engine with separate optimization mechanics. AEO and GEO are common industry labels, but Google's position is that optimizing for generative AI Search is still optimizing for the Search experience.

The practical pipeline is:

1. Google discovers URLs through links, sitemaps, redirects, and prior knowledge.
2. Google crawls accessible resources with Googlebot.
3. Google renders pages when needed, including JavaScript execution.
4. Google indexes text, images, videos, metadata, canonical clusters, language, location, and usability signals.
5. Google's systems serve relevant, high-quality results for user queries.
6. Generative AI features retrieve from the Search index and use AI techniques to generate grounded responses with prominent clickable links to supporting pages when Google shows those sources.

Two AI-specific concepts matter:

- Retrieval-augmented generation: AI responses are grounded by retrieving relevant, fresh pages from Google's Search index.
- Query fan-out: the model can issue related concurrent queries to gather more context than the user's literal wording.

Implication: improve the pages, site, and data Google can already crawl, index, understand, and rank. Do not build a separate AI-only layer unless it also helps users and Search.

Do not over-prescribe SEO. Google's guide explicitly leaves room for content to thrive in Search, including generative AI experiences, without overt SEO. The practical goal is to remove blockers and improve user value, not to complete every possible checklist item on every page.

## Recommendations

### Content

Create content that has a reason to exist beyond summarizing common knowledge. Favor:

- Firsthand experience, testing, examples, photos, data, or analysis.
- Expert or enthusiast authorship that is visible and credible.
- Clear sourcing, author/site background, and trust signals.
- Specific answers that leave the reader feeling satisfied.
- Main headings and titles that accurately describe the page.
- Clear organization with paragraphs, sections, descriptive headings, and useful links.
- Substantial value over competing pages.

Avoid:

- Generic commodity content that could be written by anyone.
- Summaries of other sources without original value.
- Mass AI-generated or templated pages.
- Changing dates to fake freshness.
- Writing to an assumed Google word count.
- Publishing on topics only because they trend.

### AI-Assisted Content

Using generative AI as an assistant is acceptable when the final content is accurate, useful, relevant, and original enough to help users. AI becomes risky when it creates many low-value pages primarily for search ranking manipulation.

Disclose or explain automation when it gives users useful context. For ecommerce, follow Merchant Center requirements for AI-generated product images or product data when applicable.

### Technical Foundation

To be eligible for Google Search and therefore Google AI Search visibility, a page needs:

- Googlebot access.
- A successful HTTP response.
- Indexable content in a supported format.
- No blocking `noindex` or access controls for pages that should appear.
- Snippet eligibility when inclusion in generative AI features is desired.

Indexing and serving are never guaranteed.

Use crawlable links, sitemaps, canonicalization, redirects, descriptive URLs, accessible resources, and Search Console diagnostics. For large sites, manage URL inventory so crawlers spend time on important unique content.

Use semantic HTML where practical because it helps people, screen readers, agents, and crawlers navigate content. Do not imply perfectly valid or perfectly semantic HTML is required; Google can understand imperfect web pages.

### JavaScript

Google can process JavaScript, but JS sites are easier to break. Ensure important text, links, media, status handling, canonical tags, robots tags, and structured data are visible in rendered HTML. Use URL Inspection or Rich Results Test to inspect rendered output.

Avoid relying on JavaScript to remove an initial `noindex`. If the original HTML says `noindex`, Google may skip rendering.

### Media

Images and videos can appear in Search and generative AI experiences. Use media when it helps the user understand the page.

For images:

- Use standard HTML image elements with `src`.
- Provide descriptive alt text, filenames, nearby text, and captions where useful.
- Provide preferred preview images through page metadata or structured data when relevant.
- Avoid generic or extreme-aspect-ratio preview images.

For video:

- Use dedicated or clear watch pages where appropriate.
- Provide unique titles and descriptions.
- Add VideoObject structured data where useful.
- Provide thumbnails and stable video URLs.
- Allow Google to fetch video bytes for previews and key moments.

### Structured Data

Structured data helps Google understand page meaning and enables eligible rich results. It is not required for generative AI Search and there is no special schema.org markup for AI Overviews or AI Mode.

Use structured data when it accurately represents visible page content and matches a supported Search feature, such as Product, Article, Breadcrumb, Organization, LocalBusiness, VideoObject, or image metadata.

### Ecommerce and Local

Google can include product, merchant, and local business details in Search and AI experiences. Keep these systems accurate:

- Merchant Center product data and feeds.
- Product structured data on product pages.
- Google Business Profile for local businesses.
- Organization, logo, breadcrumb, contact, support, return, shipping, and business details where relevant.
- Business Agent settings for eligible merchants.

### Agentic Experiences

Browser agents may inspect screenshots, DOM, and accessibility trees. Prepare by making the site usable and semantically clear:

- Use real buttons and links for actions.
- If semantic controls are not possible, provide appropriate roles, tabindex, labels, and other accessibility metadata.
- Keep layouts stable.
- Avoid transparent overlays and hidden interactive traps.
- Reflect important action state in the interface.
- Make forms and product flows understandable from the DOM, accessibility tree, and visual rendering.
- Keep required interactive elements visibly large enough to be recognized and make actionability clear with expected visual cues such as pointer cursors.

## Myth-Busting

Unsupported or overhyped tactics:

- `llms.txt` or AI-only machine-readable files for Google AI Search.
- Special Markdown or AI text versions of pages.
- Splitting content into tiny chunks solely for AI.
- Rewriting content in a special AI style.
- Creating pages for every long-tail query or guessed query fan-out.
- Inauthentic mentions, fake citations, or manufactured reputation.
- Treating structured data as an AI-specific visibility lever.

Better framing: if a tactic does not improve users, crawlability, indexability, understanding, trust, or Search feature eligibility, it is probably noise.

### Myth-Check Quick Reference

When a user asks whether one of these tactics helps, answer in the Response Pattern shape: state the verdict, name the closest real Google mechanism, then redirect to the user/Search-centered alternative.

| Claimed tactic | Verdict | Closest real Google mechanism | Do instead |
| --- | --- | --- | --- |
| `llms.txt` or AI-only machine-readable files | Not supported for Google AI Search | Standard crawling and indexing of normal HTML; `robots.txt` and sitemaps for crawl control | Make the human page crawlable, indexable, and snippet-eligible; serve the real content in HTML/rendered DOM |
| Special Markdown or AI text versions of pages | Not supported | One canonical, indexable URL per meaningful page | Keep the primary content on the canonical page; avoid duplicate AI-only variants |
| Splitting content into tiny chunks solely for AI | Overhyped | Passage-level understanding already operates over normal, well-structured pages | Use logical sections, descriptive headings, and stable URLs; consolidate rather than fragment |
| Rewriting content in a special "AI style" | Not supported | Helpful, reliable, people-first content evaluation | Improve clarity, firsthand expertise, and evidence for the human reader |
| Pages for every long-tail or guessed query fan-out | Not supported | Query fan-out runs over the existing Search index, not a per-query page | Map query families to fewer, stronger pages that answer related needs |
| Inauthentic mentions, fake citations, manufactured reputation | Against spam policies | Genuine reputation, links, and E-E-A-T signals | Earn real expertise, sourcing, and citations; never manufacture them |
| Structured data as an AI-specific ranking lever | Overhyped | Structured data for eligible rich results and clearer meaning of visible facts | Add accurate markup that matches visible content; validate with Rich Results Test |
