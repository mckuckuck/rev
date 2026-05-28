# Page Template & Block Analysis Plan

## Objective
Analyze 350+ URLs across 5 brand websites (lottabody.com, rouxbeauty.com, cutex.com, revlon.com, sinfulcolors.com) to identify recurring page templates, map each URL to its template, and identify custom blocks needed per template.

## Deliverables
1. **`page-template-mapping.csv`** — URL, Brand, Template columns
2. **`template-block-mapping.csv`** — Template, Block Name, Block Description columns

## Identified Templates (Preliminary — based on URL pattern analysis)

| # | Template Name | Description | Brands Using It |
|---|---|---|---|
| 1 | Homepage | Brand landing page with hero, featured products, CTAs | All 5 |
| 2 | Product Detail (PDP) | Individual product page with images, description, specs | All 5 |
| 3 | Product Collection/Category | Product grid/listing page with filters | All 5 |
| 4 | Product Line Landing | Sub-brand or product line overview (e.g., Coconut & Shea) | Lottabody, Roux |
| 5 | Blog Listing | Blog index or blog category page | Revlon, Roux |
| 6 | Blog Article | Individual blog post with content, images, author | Revlon, Roux, Lottabody |
| 7 | Legal/Policy | Privacy, terms, accessibility — text-heavy pages | All 5 |
| 8 | Contact | Contact form page | All 5 |
| 9 | About | Brand story/about page | Roux, Cutex, Sinful Colors |
| 10 | Gallery | User/style image gallery | Lottabody |
| 11 | Where to Buy / Store Locator | Retailer links or store finder | Lottabody, Roux, Revlon |
| 12 | Landing/Promo | Special campaign or promotional pages | Revlon, Sinful Colors, Roux |
| 13 | Product Tag/Filter | Tag-filtered product listing | Cutex, Sinful Colors |
| 14 | Monthly Specials | Monthly promotional content | Roux |
| 15 | Quiz/Interactive | Interactive quiz or try-on pages | Revlon |
| 16 | Retailer Detail | Individual retailer page (e.g., Walgreens, Amazon) | Lottabody |
| 17 | FAQ | FAQ/help pages | Revlon |

## Approach

### Phase 1: Validate Templates via Page Sampling
Sample 2-3 pages per suspected template to confirm structural patterns by fetching and inspecting HTML structure. Priority pages:
- Homepages (all 5 brands)
- Product pages (1 per brand)
- Collection pages (1 per brand)
- Blog articles (Revlon)
- Legal pages (1 sample)
- Gallery, Store Locator, Quiz pages

### Phase 2: Identify Blocks per Template
For each confirmed template, identify the custom EDS blocks needed:
- **Homepage**: Hero, Featured Products Carousel, CTA Banner, Brand Story, Newsletter Signup
- **PDP**: Product Gallery, Product Info, Ingredients, Related Products, Reviews
- **Collection**: Product Grid, Filter/Sort Bar, Category Banner
- **Blog Article**: Article Hero, Content Body, Author Bio, Related Posts, Social Share
- **Legal**: Text Content (default content, no custom blocks)
- etc.

### Phase 3: Generate CSVs
Produce both CSV files based on confirmed analysis.

## Execution Plan

### Step 1 — Fetch & Inspect Sample Pages
Use web fetch or site analysis tools to inspect page structure for ~15-20 representative URLs across templates.

### Step 2 — Finalize Template Definitions
Confirm or adjust the 17 template types based on actual page structures observed.

### Step 3 — Classify All URLs
Map each of the 350+ URLs to its template based on URL patterns and confirmed structures.

### Step 4 — Block Identification
Document custom blocks per template with names and descriptions.

### Step 5 — Generate Output CSVs
Write both CSV files to the project directory.

## Checklist

- [ ] Fetch and inspect sample homepage (1 per brand = 5 pages)
- [ ] Fetch and inspect sample PDP (1 per brand = 5 pages)
- [ ] Fetch and inspect sample collection/category page (3 pages)
- [ ] Fetch and inspect sample blog article (2 pages)
- [ ] Fetch and inspect sample gallery, store locator, quiz pages (3 pages)
- [ ] Confirm/revise template definitions based on observed structures
- [ ] Classify all 350+ URLs to templates
- [ ] Identify custom blocks for each template
- [ ] Generate `page-template-mapping.csv`
- [ ] Generate `template-block-mapping.csv`
- [ ] Review outputs with user

## Notes
- All 5 sites appear to be WordPress/WooCommerce-based (Revlon is Shopify-based)
- URL patterns provide strong signal for classification but page inspection will confirm
- Some pages may be edge cases requiring manual classification
- Execution requires switching out of Plan mode
