# WordPress handoff / Part 3

## Scope and source distinction
The user requested a local static preview before WordPress. Assignment PDFs are requirements to assess, not authorization to sign up for hosting, publish content, contact instructors, or grant administrator access. None of those actions were performed.
Part 2 final content is DOC-20261018-WA0004.pdf. The other two PDFs are assignment briefs. The original Part 1 model is not among these three PDFs. Its previously discussed structure is preserved, and the final content provides concrete field names and relationships.

## Content model
- Destination CPT: 1 Bagdad record, linked to 8 Places.
- Place CPT: 8 records; Category taxonomy is many-to-many.
- Review CPT: 4 test records linked to the corresponding Places; mark as test/draft, never as authentic visitor experiences.
- Category taxonomy: 4 terms, not an independent CPT.
- Media Library: 9 images and attached metadata.
- Reusable site header/footer and consistent global styles.

Destination fields: Name, Slug, Description, Hero image, Getting there, Getting around, Best time to visit, Language & currency, Accommodation, Health and safety, Address / region, Latitude, Longitude, Official tourism website, Tourist information office, Emergency contacts, Featured places.
Place fields: Name, Slug, Description, Main_image, Gallery, Category, Opening_hours, Entry_fee, Accessibility, Address, Place reference, Review reference.
Review fields: Visitor_name, Rating, Comment, Review_date, Place.
Category fields: Name, Slug, Description, Image, Icon.
Media metadata: File, Source website, Source_url, Copyright_holder, Photographer, License / usage rights, Attribution required, Attribution, Alt_text, Caption.

## ACF implementation
Use text for names/slugs/addresses and short metadata, textarea or WYSIWYG for long prose, image and gallery fields for Media Library attachments, relationship fields for featured/related Places and review links, a taxonomy field for Category, number fields for entry fees/coordinates/rating, a date picker for review date, URL for actual source URLs. Preserve blank/unknown fees and unconfirmed opening hours. Tourism-website source text explicitly says no reliable central website is listed; do not force that sentence into a URL field.

## Template mapping
Home: Destination hero and featured Place relationships.
Places archive: category filter, search, sort and load more.
Single Place: description, main image, categories, gallery, practical fields, related Places, test Reviews and form layout.
Taxonomy archive: category description/image and linked Places.
About/Practical: approved static copy plus Destination practical fields.
Privacy/Cookies/404/Search: separate templates with supplied labels.
Media credits: attribution links and metadata, with original files and license records retained.

## Assignment checks and unresolved decisions
The supplied Part 3 PDF still says WordPress.com Education and explicitly says not LocalWP. The previous conversation reported professor screenshots replacing that section with LocalWP and possibly removing ACF Field Blocks. Those screenshots were not among the three newly supplied files. Keep the preview local as requested; verify the professor's amended instructions before the real CMS setup.
The brief asks for at least 4 items per content type. The final approved content has only 1 Destination by design. Flag this for instructor clarification; do not invent three destinations.
An additional fully developed CPT is an above-and-beyond criterion in the rubric. No extra content type was invented for this bounded preview.
The brief's published WordPress URL and instructor administrator access apply to the final WordPress submission, not this local mockup.
Responsive design, hover/focus states, semantic headings, keyboard controls, labeled inputs, skip navigation and local image alt text are included. WordPress still needs real dynamic templates, CMS validation, SEO metadata/canonicals/sitemap and AEO review, real form processing if enabled, cookie audit, final accessibility testing and publication checks. Hash routes in the preview are not production SEO routes.
Replace PDF image previews with the corresponding approved full-resolution source images before final publication, preserving photographer and license attribution.
No updates to the supplied travel advice or policies were invented. Verify time-sensitive information separately before publication.
