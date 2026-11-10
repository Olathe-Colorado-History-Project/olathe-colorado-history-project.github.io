# Olathe Colorado History Project
This repository contains the source and editorial guidance for the Olathe Colorado History Project website at https://olathe-colorado-history-project.github.io/.
## Purpose and identity
The project documents the history of Olathe, Colorado, through accessible accounts of people, places, events, institutions, and changes to the town and its surrounding area. Its purpose is to make historical information understandable, discoverable, and traceable to evidence. It is a historical publication, not an official municipal record or a claim to speak on behalf of the Town of Olathe. Authorship, publishing responsibility, and corrections should be identifiable without overstating the project's institutional status.
The website is a growing reference work, not a promotional landing page. An incomplete but carefully sourced record is preferable to a comprehensive-looking account built on assumptions.
## Architectural principle: dumb pages, smart source code
Keep complexity in source files and build-time transformations, not in visitors' browsers. Use GitHub Pages and Jekyll to produce ordinary static HTML, CSS, images, and linked documents from Markdown, YAML, Liquid templates, and reusable includes.
- Content must remain readable and navigable with JavaScript disabled.
- Use semantic HTML, system fonts, native links, and open formats. Favor speed, reliability, portability, and machine readability.
- Do not introduce a client-side application framework, content management system, database, analytics platform, visitor accounts, or proprietary dependency without a demonstrated need that cannot be met more simply.
- Store original editorial material in human-readable source files and preserve Git history as a public record of changes.
- Avoid duplicating facts across pages: derive repeated indexes and structured metadata from canonical records where practical.
- Prefer a smaller working site over elaborate infrastructure or placeholder features.
## Editorial standards
Write for curious readers rather than for search engines or an academic in-group. Lead with what is known, then explain why it matters. Favor direct sentences, chronological clarity, informative headings, and substantive prose over decorative interface elements.
- Never invent a date, quotation, location, relationship, event, attribution, or source to complete a narrative.
- Separate historical events from the dates they were reported, recorded, published, digitized, and reviewed.
- Identify whether an assertion comes from a contemporary record, later recollection, secondary interpretation, or the project's own inference.
- Do not convert plausible connections, geographic proximity, coincidental names, or community traditions into established facts without evidence.
- Treat conflicting accounts honestly. State material disagreements and the basis for any preferred interpretation.
- Describe unknowns as unknowns. Avoid both unsupported certainty and repetitive hedging where evidence is strong.
- Preserve source limitations and unresolved leads for review; keep ordinary articles readable without concealing qualifications essential to their claims.
- Attribute quotations, transcriptions, images, maps, and documents. Distinguish quoted wording from transcription and editorial modernization.
- Avoid empty pages, fictitious completeness, generic filler, promotional copy, and unnecessary repetition.
### Treatment of claims
**Established:** A relevant source directly supports the assertion. State the fact plainly and cite the supporting record.
**Qualified:** Evidence supports an interpretation but not every detail, or sources disagree. Explain the limitation and cite the pertinent records.
**Unresolved:** Evidence is insufficient to settle the question. Document the open question and research leads; do not publish a guess as fact.
These are editorial treatments, not decorative confidence scores. The public narrative should show important qualifications in ordinary language. The source directory and research notes may carry fuller discussion.
## Sourcing and provenance
Sources are part of the site's content architecture, not an afterthought. Prefer accessible primary records where they exist: historical newspapers, municipal and county records, land and census documents, photographs, maps, oral histories with clear provenance, and original publications. Secondary histories and community memories are valuable but must be identified for what they are.
Maintain a central source catalog in `_data/sources.yml`. Give each source a stable ID so articles, places, biographies, and chronology entries can cite the same record. Useful fields include:
- `id`, `title`, `type`, `creator` or `author`, and issuing or holding `institution`.
- `created_on` or original publication date, where known; a distinct `accessed_on` or `reviewed_on` when useful.
- `url` or local file path; archival collection, identifier, volume, issue, page, and image/frame references when available.
- `description`, `limitations`, transcription notes, and `rights` or reuse conditions.
Do not invent missing fields. A bibliography entry without a working URL is acceptable if it contains enough bibliographic detail to identify the source. Keep archival identifiers and original destinations even when online links fail; repair or replace dead links when verified.
For each substantive article:
- Cite consequential historical claims near the relevant text using stable source IDs.
- Render unobtrusive numbered references linked to a readable reference list; generate numbering at build time wherever practical rather than manually synchronizing multiple lists.
- Link to scans, page-level records, or archival catalogs rather than to general institutional homepages when the specific source is available.
- Record source disagreements, provenance gaps, and research leads in the source catalog or dedicated research records, without burying the public prose in editorial process notes.
- Do not use circular citations. A statement authored by this project is not independent evidence for itself.
Corrections should amend the source record and affected pages together; do not silently discard historical caveats.
## Information architecture
Organize around the subjects of local history and how they can be investigated, not around the functions of a government office. These are conceptual sections rather than a requirement to create seven empty navigation tabs:
1. **Home:** State the project's scope and direct readers to substantive material.
2. **History:** Readable narratives of the town's development, grouped by meaningful subject or period.
3. **People:** Biographical accounts and documented connections among residents, families, and organizations.
4. **Places:** Buildings, streets, businesses, landmarks, surrounding landscapes, and historical geography.
5. **Chronology:** Dated events with concise descriptions, links to fuller entries, and supporting evidence.
6. **Sources & Documents:** Bibliography, original records, archival links, images, transcriptions, and downloadable material.
7. **About & Corrections:** Scope, publisher identity, editorial method, attribution, rights, contribution procedure, and corrections.
Use a short primary navigation that reflects pages containing real material. Add categories only when substantial content exists. Cross-link related people, places, events, and sources in the body of each entry; do not require visitors to understand the underlying data model.
## Content models and reuse
Markdown articles with YAML front matter should be the default for readable narratives. Structured data should power repeated lists and relationships when that improves consistency.
- **Article:** Stable slug, title, summary, subject or period, relevant dates, source IDs, and related entries.
- **Person:** Preferred display name, attested variants, documented dates and relationships, biographical text, and source IDs.
- **Place:** Historical and present names, geographically supported location if known, dated uses or changes, and source IDs.
- **Event:** Date or bounded range, precision or uncertainty, short description, related people and places, and source IDs.
- **Document:** Title, original date, creator, holding institution, persistent locator, format, rights, related article, and source IDs.
These are proposed data models, not an instruction to prematurely create every collection. Keep uncertain dates as qualified text or explicitly modeled ranges; never silently turn an approximate year into a precise calendar date. Location coordinates must refer to documented places and must not imply survey-grade certainty.
Use Jekyll collections, `_data/` records, and `_includes/` only where they reduce duplication. Stable URLs and human-readable source files are more important than an elaborate taxonomy.
## Original materials and imagery
Historical photographs, newspaper pages, maps, plans, inscriptions, and facsimiles may be central evidence, not decoration. Include them when they add verifiable information.
- Supply descriptive alt text, visible captions, dates or approximate dates, creator/holding institution, and a citation or archival identifier.
- Distinguish original artifacts from restorations, crops, colorizations, reconstructions, and illustrations.
- Keep an accessible text account of information conveyed by a map, diagram, or scan. Provide transcriptions where useful and feasible.
- Optimize display copies for bandwidth while retaining attribution and links to originals. Do not silently modify an archival source and present the result as untouched.
- Verify copyright, license, donor permission, and privacy considerations before publishing or redistributing files. Public online availability is not the same as permission to reproduce.
- Do not publish private living-person information, sensitive records, or identifying metadata merely because it exists in an archival or donated file.
## Visual design and accessibility
Use a quiet editorial design whose hierarchy is carried primarily by typography, spacing, and links. The default should be a light reading surface with high-contrast text, comfortable line height, readable article width, generous margins, and restrained accent colors.
- Favor a simple site header, clearly marked navigation, plain text links, an obvious page title, and a compact footer.
- Keep the content column narrower than the full page on large displays; adapt gracefully to small phones without horizontal scrolling.
- Use conventional underlines for prose links, visible keyboard focus states, skip navigation, appropriate landmarks, and correctly nested headings.
- Prefer tables only for genuinely tabular records; ensure they remain readable on narrow screens.
- Do not hide essential historical information in carousels, hover interactions, animations, or scripts.
- Respect reduced-motion settings, text zoom, and assistive technologies. Aim for WCAG 2.2 AA; do not claim a formal audit without conducting one.
- Printable, linkable article pages are more valuable than a visually elaborate interface.
## Documents and bibliography
A source or document should be listed on its relevant subject page and, when appropriate, included automatically in a shared index at build time. Deduplicate by stable ID and retain attribution to the original publisher or holding institution. Do not imply that external historical records were created by this project.
A record's display status is not a privacy mechanism: **anything committed to this public repository can be retrieved directly**, even if unlinked or marked as unpublished. Review permissions and sensitive information before committing binaries or data.
## Metadata, discovery, and long-term maintenance
Generate useful metadata without changing the visible reading experience: descriptive page titles and summaries, canonical URLs, accessible images, `robots.txt`, `sitemap.xml`, and accurate Schema.org JSON-LD.
- Use appropriate `WebSite`, `WebPage`, `Article` or `ScholarlyArticle`, `Person`, `Place`, and `CreativeWork` types only when the page and evidence support them.
- Make the publisher identifiable as the Olathe Colorado History Project. Never imply municipal endorsement or official authority that has not been established.
- Preserve old URLs through redirects when pages move; avoid breaking references needlessly.
- Do not add trackers, advertisements, third-party embeds, or external scripts merely for analytics or appearance.
- Keep source dates and editorial update dates distinct. A revised webpage does not make an old historical document newly published.
## Technical organization
The initial implementation should remain a small, conventional Jekyll repository. A plausible structure, added incrementally, is:
```text
_config.yml
index.md
_data/navigation.yml
_data/sources.yml
_includes/references.html
_layouts/default.html
assets/css/site.css
assets/images/
assets/documents/
history/
people/
places/
chronology/
sources/
about/
legal/
```
Only add directories and templates when there is content to support them. Use a single shared layout and stylesheet until real needs justify more. GitHub Pages should build from `main` using supported Jekyll facilities. Avoid runtime requests for the site's own core content.
## Publication workflow
1. Collect evidence and record enough provenance to relocate it.
2. Draft readable prose, or a structured record when justified, without inventing missing details.
3. Check claim-to-source correspondence, event dates, names, locations, competing accounts, and quotations.
4. Review images, documents, rights, privacy, accessibility, and outgoing links.
5. Build and inspect the site; check narrow and wide screens, keyboard operation, metadata, internal links, and reference targets.
6. Commit the source changes with a descriptive message. Keep corrections traceable in Git history.
7. Verify the public deployment and relevant pages after publishing.
A source change affecting multiple entries should update all dependent material. Build-time checks for duplicate source IDs, broken reference IDs, missing local files, and invalid data are desirable as the catalog grows, but should remain proportionate to the site's complexity.
## Contributions and corrections
Accept corrections and contributed material with enough context to evaluate them: the exact claim or page, the proposed correction, the supporting evidence, and any relevant rights or privacy limitations. Credit contributors with their consent. A recollection can be published as an attributed recollection without being misrepresented as a contemporaneous record.
Keep a public explanation of editorial responsibility and a workable correction channel once one is established. Do not publish a personal email address or claim a contact channel exists before it is approved.
## Initial milestone
Publish a readable homepage, the shared layout and stylesheet, an About & Corrections page, and a small number of well-supported historical entries with functioning references. Expand the source catalog and subject indexes from real material. The measure of progress is not the number of sections or features but the amount of verifiable Olathe history readers can actually use.
