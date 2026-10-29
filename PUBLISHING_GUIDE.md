# BRANDSTUDIO daily auto-publishing contract

The scheduled task **BRANDSTUDIO Phone SEO** owns daily phone research and publication. It must follow this contract.

## Source repository and production
- GitHub: `artclass11/BRANDSTUDIO`, default branch `main`.
- Static production project: Vercel project ID `prj_JQbuCW9a7LEyjyVRvCk7hwJ2yoR9`, project name `brandstudio`.
- Public site alias to verify: `https://brandstudio-pi.vercel.app/`.
- Guide archive: `phone-guides/index.html`.
- Sitemap: `sitemap.xml`.
- Live site changes are not complete until the GitHub commit(s) are saved, a production deployment is READY, and the new article URL is checked.

## Budget rotation
Start on 2026-10-30 with under ₹10,000, then rotate each calendar day by this seven-band cycle:
1. Under ₹10,000
2. ₹10,000–₹20,000
3. ₹20,000–₹30,000
4. ₹30,000–₹50,000
5. ₹50,000–₹80,000
6. ₹80,000–₹1,20,000
7. ₹1,20,000–₹2,00,000

Calculate the band from the number of calendar days since 2026-10-30 modulo seven. Candidate brands are Apple, Samsung, Motorola, OnePlus, Xiaomi, Honor, Vivo, Nothing, Nokia/HMD and Realme; this is not a fixed quality ranking. Compare the full market objectively.

## Evidence and writing bar
- Search current sources on every run, with India price and purchase availability checked on the publication date.
- Prefer official manufacturer India pages for specs, warranty/software policy, and reputable independent reviews for performance, thermals, display, sound and sustained quality. Use independent retailer pages only as price evidence. Include 2–4 source links in the article.
- Assess processor/performance and thermal stability, display, sound/speakers, 5G compatibility, battery/charging, cameras, build, software-update policy, reliability evidence and after-sales service.
- Compare three contenders internally but publicly recommend only one model, with a simple short verdict, three grounded strengths, one limitation and who the phone suits.
- Never fabricate exact street price, specifications, benchmarks, warranty, reliability statistics, availability, or future launch details. Date the price checks and note normal price/stock variation.
- Upcoming launches are a separate short note only when officially or strongly confirmed; never recommend an unavailable/released-later device as buyable.
- If nothing clears the minimum quality bar in the target band, do not publish a page, archive card or sitemap entry. Return NO PUBLISH TODAY and the evidence-based reason. Never force a bad recommendation.

## Auto-publishing sequence
1. Check the repo latest state and archive to avoid duplicate article for the same date/budget. A date already published must not be overwritten. If no recommendation clears the quality bar, stop without site changes.
2. Research and write a short static HTML article at `phone-guides/YYYY-MM-DD-<short-seo-slug>.html`. It must be mobile responsive and use the existing minimal graphite/ivory/champagne design, BRANDSTUDIO name, clear H1, date published/price checked, budget, one recommendation, price/range only if verified, concise rationale, one limitation, source links, canonical/description/open-graph tags, Article JSON-LD with datePublished/dateModified (same publication date), and a WhatsApp CTA to `https://wa.me/919921894495`. Do not copy product photos or official review text; no image is required.
3. Create the new article using the GitHub contents connector (create a NEW file; never replace an existing article).
4. Fetch `phone-guides/index.html`, preserve all existing content and replace the contents only between `<!-- AUTO-POST-INDEX:START -->` and `<!-- AUTO-POST-INDEX:END -->` with the newest-first list of cards, each linking to the correct article and displaying publication date, budget and a short accurate summary. Never remove previously published posts from the archive.
5. Fetch `sitemap.xml`; add the article's absolute canonical URL as a new `<url>` entry with current `lastmod`. Keep every existing URL and do not duplicate entries.
6. Use the GitHub update/create file operations sequentially, based on fresh blob SHA values for updates. Commit content only to `main`. Do not modify unrelated files, workflow permissions, secrets, or repository settings.
7. After all GitHub changes succeed, trigger a production deployment via the connected Vercel tool against project `prj_JQbuCW9a7LEyjyVRvCk7hwJ2yoR9`, using GitHub source `artclass11/BRANDSTUDIO` branch `main` (latest commit, no pinned old SHA), production target. Poll the deployment status. Do not report success while building or on ERROR.
8. Verify the deployment is READY and test the homepage, archive and new article page. Report the actual URL, budget/model, price check date and sources. If deployment fails after GitHub files are committed, state that the post is saved but not live, include the error and do not claim auto-publication succeeded.

## Homepage link
The homepage has a Phone guides navigation link and a phone-guides teaser. Do not rewrite the homepage in daily runs.

## Required daily report
Return just a compact status: PUBLISHED (with article URL + one-pick summary + verified price + sources) or NO PUBLISH TODAY (reason), or BLOCKED (exact repository/deployment blocker). Never silently imply a successful live post.
