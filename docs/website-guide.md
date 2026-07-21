# Marcel Cato Website Guide

This guide documents the structure, content, visual system, navigation behavior, metadata, assets, and maintenance considerations for the Marcel Cato personal website. It is organized page by page, with cross-site notes for shared styling and reusable assets.

## 1. Website Overview

### Purpose

The website presents Marcel Cato's public-facing professional profile. Its primary message is a public-service trajectory rooted in New York City, centered on politics, urban planning, civic administration, institutional leadership, and future-facing government work.

### Core audiences

- Public-service, policy, and government professionals evaluating Marcel's background.
- University, nonprofit, and civic-institution contacts seeking résumé, experience, or contact information.
- Search engines and social platforms that need accurate metadata, images, and structured profile information.
- Visitors on mobile and desktop devices who need quick navigation to biography, platform, experience, education, résumé, LinkedIn, and email.

### Current pages and documents

| File | Role |
| --- | --- |
| `index.html` | Primary landing page and full professional narrative. |
| `education.html` | Education-focused secondary page. |
| `style.css` | Shared design system and page-specific compatibility styles. |
| `resume.pdf` | Downloadable résumé linked from the main page, footer, and education page. |
| `google0db97e79245fe7a6.html` | Google site verification file. |
| `docs/website-guide.md` | This exported website guide. |

### Site identity

The site uses a dark, glassmorphism-style civic portfolio aesthetic: dark radial backgrounds, gold accents, blurred translucent cards, portrait-led storytelling, and formal language. The brand assets are the signature image and Cato seal/favicon.

## 2. Global Design System

### Color palette

The CSS custom properties in `style.css` define the visual language:

- `--bg`: primary near-black background.
- `--bg-alt`: alternate dark background.
- `--panel`: translucent dark panel fill.
- `--panel-soft`: light translucent overlay for glass surfaces.
- `--border`: subtle translucent borders.
- `--text`: warm off-white body text.
- `--muted`: subdued beige text for captions and supporting copy.
- `--gold` and `--gold-deep`: primary accent colors for highlights, buttons, tags, and focus states.

### Typography

The site loads the Inter typeface from Google Fonts. Headings use large, responsive clamp values, while body text uses a readable `line-height` of `1.6`. Uppercase eyebrow labels and pill tags use increased letter spacing to reinforce the formal portfolio style.

### Layout primitives

- `.glass`: reusable blurred panel/card style with translucent backgrounds, borders, and rounded corners.
- `.section`: common content width and vertical spacing wrapper.
- `.section-head`: heading block used before major grids.
- `.chip-row` and `.chip`: compact topical tags.
- `.action-row`, `.btn`, `.btn-primary`: shared call-to-action groups and button styles.
- `.reveal`: scroll-reveal animation class paired with JavaScript intersection observers.

### Responsive behavior

The site adapts at two primary breakpoints:

- `max-width: 860px`: multi-column content collapses to one column, media cards stack vertically, portraits become landscape-friendly, and contact content centers.
- `max-width: 640px`: the fixed navigation compresses, and the signature moves above the nav links.

### Accessibility and progressive enhancement

- A skip link allows keyboard users to jump directly to the main content on the home page.
- Focus states use a gold outline for visible keyboard navigation.
- `prefers-reduced-motion` disables animations and smooth scrolling for users who request reduced motion.
- `prefers-contrast` and forced-colors modes strengthen glass panel contrast.
- A fallback for unsupported `backdrop-filter` gives glass panels an opaque background.

## 3. Home Page: `index.html`

The home page is the site's principal narrative and contains most of the public profile. It is built as a single-page landing experience with anchored sections.

### 3.1 Head, metadata, and SEO

The document declares English language, UTF-8 encoding, and responsive viewport settings. The title is `Marcel Cato | NYU Politics & Urban Planning | Public Service`, which communicates name, academic identity, and public-service positioning.

Key metadata includes:

- A concise meta description for search snippets.
- Canonical URL pointing to `https://marcelcato.github.io/`.
- Open Graph title, description, type, URL, image, and site name for social sharing.
- Twitter summary-large-image card metadata.
- Favicon reference to `favicon-cato.png`.
- Google Fonts import for Inter.
- Stylesheet import for `style.css`.

The page also contains schema.org JSON-LD structured data using `@type: Person`. This identifies Marcel Cato, the website URL, profile image, job title, description, organizations, affiliations, and LinkedIn profile. This helps search engines understand that the site represents a person rather than only a generic website.

### 3.2 Primary navigation

The home page uses a fixed glass navigation bar at the top. It contains links to:

- Home / top section.
- Biography.
- Platform.
- Experience.
- Education page.
- Contact.

The signature image sits in the middle of the navigation to reinforce personal branding. Internal links rely on section IDs, while the education link navigates to `education.html`.

JavaScript observes page sections and toggles the `active` class on matching nav links as users scroll. This gives visitors a sense of location within the one-page layout.

### 3.3 Hero section

The hero is the first major content area and uses `hero-full.png` as a full-screen background image with dark overlays. Its purpose is to establish immediate identity and positioning.

Content elements:

- Eyebrow: `OFFICIAL SITE OF MARCEL CATO`.
- Main heading: `Marcel Cato`.
- Hero line: `Public Service. Urban Governance. Institutional Leadership.`
- Supporting paragraph explaining NYU Politics and Urban Planning, New York City roots, and public-service preparation.
- Topic chips: NYU Politics & Urban Planning, New York City, Public Service, Washington, DC Preparation.
- Calls to action: View Experience, Download Résumé, Contact.

User flow intent: the hero gives quick identity confirmation and routes visitors toward deeper proof points or direct contact.

### 3.4 Credibility section: “The Work in View”

This section summarizes Marcel's cross-disciplinary credibility before the biography. It combines four proof cards with a Washington, DC image.

Cards:

1. Public & Civic Operations.
2. Urban Governance & Planning.
3. Institutional Administration.
4. Communications & Systems.

The image `Marcel_WashingtonMonumentImage_(9:16).jpg` visually supports the New York-to-Washington public-service arc. The section uses a responsive grid where the key photo spans two rows on desktop and collapses into the flow on mobile.

### 3.5 Biography section

The biography section explains Marcel's academic and professional identity in paragraph form. It emphasizes:

- New York University.
- Politics.
- Urban planning.
- Public administration.
- Civic institutions.
- University administration.
- Nonprofit leadership.
- Election operations.
- Public communications.
- Systems-building.

It includes chip tags for Politics at NYU, Urban Planning Focus, Dean's List, and Public Service & Civic Operations. The section also displays `profile.png` as a headshot portrait inside a glass panel.

### 3.6 Platform section

The platform section states the site's values and public commitments. It is not a campaign platform in a legal/electoral sense; it is a principles section describing what guides Marcel's public-service work.

Principles:

1. Capable Institutions — competence, reliability, transparency, and trust.
2. Cities That Work — housing, mobility, public space, infrastructure, safety, and quality of life.
3. Civic Dignity — treating people as citizens with agency.
4. Disciplined Leadership — preparation, restraint, standards, and follow-through.

Below the principles, `MarcelChairMeeting.png` shows Marcel chairing an NYU HEOP advocacy meeting with staffers at the New York State Capitol. The image reinforces leadership, governance, and institutional context.

### 3.7 Experience section

The experience section is a timeline-style record of institutional, civic, communications, and technical work. It is the page's strongest evidence section.

#### New City Parks — Communications Intern

- Dates: June 2025 – August 2025.
- Themes: communications, public space, community storytelling.
- Image: `Marcel&MayorofPatterson.png` with Mayor Andre Sayegh of Paterson at a parks clean-up event.
- Focus: communications overhaul for a parks-focused nonprofit, design, short-form video, resident storytelling, outreach, canvassing, and strategy proposals.

#### NYU Stern School of Business – Development and Alumni Relations — Undergraduate Office Assistant

- Dates: September 2024 – Present.
- Themes: institutional administration and donor relations.
- Image: `Marcel_Trophy(9:16).jpg`.
- Focus: confidential records, donor information, Blackbaud CRM, events, internal reporting, and professional communication.

#### NYU Parliamentary Debaters Union — Vice President of Operations

- Dates: May 2025 – Present.
- Themes: leadership, operations, systems-building.
- Image: `Marcel_DebateGroupPhoto.jpg`.
- Focus: logistics, planning, funding coordination, communications, website and IT support.

#### New York City Board of Elections — Election Worker

- Dates: August 2024 – Present.
- Themes: civic operations and election administration.
- Focus: polling-site operations, voter assistance, accessible voting procedures, and practical election administration.

#### Find Community Connection Project — Office Intern, Field Manager, and Group Leader

- Dates: July 2024 – August 2024.
- Themes: nonprofit leadership and government outreach.
- Image: `Marcel_CityCouncilCitation_(9:16).jpg`.
- Focus: nonprofit administration, donor relations, event logistics, elected-office communication, records, correspondence, meetings, events, and Google Workspace/software support.

#### Brooklyn Technical High School — IT Department Intern

- Dates: April 2023 – May 2023.
- Themes: technical support and administration.
- Focus: software, hardware, documentation, and administrative assistance.

### 3.8 Transition banner

The transition banner uses `nyc-banner.jpg` with a dark overlay. Its headline is: `Rooted in New York. Preparing for Washington. Built for public service.`

The purpose is to connect the local New York identity with a broader public-service future. It functions as an emotional bridge between the detailed experience record and the final contact section.

### 3.9 Contact section

The contact section provides professional conversion paths. It includes:

- `profile.png` portrait.
- Heading: `Professional Contact`.
- Copy inviting opportunities related to public service, urban planning, policy, institutional administration, communications strategy, and civic leadership.
- Buttons for email, LinkedIn, and résumé download.
- Signature and Cato seal visual marks.

This is the primary end-of-page action area.

### 3.10 Footer

The home footer repeats identity and utility links:

- Signature image.
- Cato seal.
- Copyright notice.
- Résumé.
- LinkedIn.
- Email.
- Education.
- Return to top.

The footer supports visitors who reach the bottom and need a final action.

### 3.11 Home page JavaScript

The script has two responsibilities:

1. Navigation state tracking: an `IntersectionObserver` watches all sections with IDs and activates the corresponding nav link as sections enter the viewport.
2. Reveal animations: another `IntersectionObserver` adds `.visible` to `.reveal` elements when they enter the viewport.

The JavaScript is lightweight, inline, and does not require a build step.

## 4. Education Page: `education.html`

The education page is a smaller secondary page dedicated to academic background. It uses the same stylesheet and branding assets, but its layout is simpler and retains some legacy CSS compatibility classes.

### 4.1 Head, metadata, and structured data

The title is `Education – Marcel Cato`, and the description summarizes Marcel's educational background as an NYU Politics major with an Urban Planning minor.

The page includes schema.org `Person` structured data with:

- Name and image.
- Website URL.
- Job title.
- NYU Stern DART work association.
- New York University membership.
- Uncommon Collegiate Charter High School alumni relationship.
- Organizational affiliations.
- Awards.
- LinkedIn profile.
- Description focused on diplomacy, public service, donor relations, nonprofit leadership, IT administration, and election facilitation.

### 4.2 Education page navigation

The page uses a `.floating-nav` structure with links for Home, Biography, My Vision, Experience, and Education. Only Home and Education are fully navigable in the current markup. Biography, My Vision, and Experience are placeholder `#` links, so they do not currently route back to the matching home-page anchors.

Recommended future improvement: change these placeholders to `index.html#biography`, `index.html#platform`, and `index.html#experience` for consistency with the home page.

### 4.3 Education content

The main content wrapper uses `.container.page-content`. It contains the heading `My Education` and two card-style school entries.

#### New York University

- Degree: BA in Politics, Minor in Urban Planning.
- Expected completion: 2027.
- Relevant courses: Intro to Political Theory, U.S. Foreign Policy, Research Methods, Shaping the Urban Environment.

#### Uncommon Collegiate Charter High School

- Class of 2023.
- Location: Brooklyn, New York.
- Highlights: Top 10% of class, AP Scholar, student mentor for the college application process.

### 4.4 Education footer

The education footer contains the signature, Cato logo, résumé link, LinkedIn link, and email link. It is styled using `.footer` and `.footer-content`, which are supported by the legacy compatibility section in `style.css`.

## 5. Shared Assets

### Images and brand files

| Asset | Usage |
| --- | --- |
| `hero-full.png` | Home page hero background and social sharing image. |
| `profile.png` | Biography and contact portraits; education page structured data image. |
| `signature.png` | Navigation, contact section, and footer identity mark. |
| `favicon-cato.png` | Browser favicon, footer seal, and contact mark. |
| `favicon-mc.png` | Additional favicon/brand asset currently present but not referenced in the main pages. |
| `nyc-banner.jpg` | Transition banner background. |
| `Marcel_WashingtonMonumentImage_(9:16).jpg` | Credibility section DC visual. |
| `MarcelChairMeeting.png` | Platform leadership visual. |
| `Marcel&MayorofPatterson.png` | New City Parks experience visual. |
| `Marcel_Trophy(9:16).jpg` | NYU Stern experience visual. |
| `Marcel_DebateGroupPhoto.jpg` | NYU Parliamentary Debaters Union experience visual. |
| `Marcel_CityCouncilCitation_(9:16).jpg` | Find Community Connection Project experience visual. |

### Documents and verification files

- `resume.pdf`: downloadable résumé used by calls to action and footers.
- `google0db97e79245fe7a6.html`: Google verification page; it should usually remain unchanged unless Google provides a replacement token.

## 6. Navigation Map and Visitor Paths

### Primary home-page paths

- First-time visitor: Hero → Credibility → Biography → Platform → Experience → Contact.
- Recruiter or professional contact: Hero → Download Résumé or Contact → LinkedIn/email.
- Civic/public-service reviewer: Platform → Experience → Contact.
- Education-focused visitor: Navigation → Education page.

### URL and anchor map

| Destination | URL or anchor |
| --- | --- |
| Home top | `index.html#top` or `/` |
| Biography | `index.html#biography` |
| Platform | `index.html#platform` |
| Experience | `index.html#experience` |
| Contact | `index.html#contact` |
| Education | `education.html` |
| Résumé | `resume.pdf` |
| LinkedIn | `https://www.linkedin.com/in/marcelcato` |
| Email | `mailto:marcelcatowrk@gmail.com` |

## 7. SEO, Social, and Structured Data Notes

### Strengths

- The home page includes canonical, Open Graph, Twitter card, and Person JSON-LD metadata.
- The education page includes Person JSON-LD with education and affiliation context.
- Images include descriptive alt text on the home page.
- Page titles and descriptions clearly identify Marcel and the site's public-service theme.

### Maintenance recommendations

- Keep dates current for roles marked `Present`.
- Keep the résumé PDF synchronized with the experience section.
- Ensure social preview image dimensions remain appropriate for large-card sharing.
- Avoid changing the canonical URL unless the site moves domains.
- If the education page evolves, align its metadata and navigation with the home page.

## 8. Accessibility Notes

### Current accessibility practices

- The home page includes a skip link to `#main-content`.
- Key visual images have alt text or ARIA labels.
- Keyboard focus is visible.
- Reduced-motion preferences are respected.
- High-contrast modes receive stronger backgrounds and borders.

### Suggested future improvements

- Add a skip link to the education page.
- Replace placeholder education-page nav links with working links to home-page anchors.
- Confirm color contrast with an automated accessibility tool after future design changes.
- Consider adding `rel="noopener"` to education-page external links opened in new tabs, matching the safer pattern used on the home page.

## 9. Maintenance Checklist

Before publishing future updates:

1. Confirm all linked image and PDF files exist.
2. Open `index.html` locally and click every navigation item.
3. Open `education.html` locally and click every navigation item.
4. Confirm résumé downloads correctly.
5. Check mobile layouts at narrow screen widths.
6. Validate that structured data remains valid JSON.
7. Confirm footer links are up to date.
8. Run a basic HTML validation pass if possible.
9. Commit changes with a clear message.

## 10. Change Log for This Guide

- Added a complete exported website guide documenting the home page, education page, shared CSS system, assets, navigation map, SEO metadata, accessibility notes, and maintenance checklist.
