<!-- impeccable:product-schema 1 -->
# M3 Media

## Platform
web

## Users
Media professionals, broadcast station operators, podcast creators, on-air talent, and content brands seeking full-service media production, web design, or talent management. Prospective clients evaluating M3 Media's capabilities and initiating contact.

## Product Purpose
Present M3 Media Group as a full-service media company and convert visitors into leads. The site communicates six service lines (broadcast engineering, multimedia production, podcast production, website design, social media management, talent management), showcases a portfolio of conservative media clients, and captures inbound inquiries via a Formspree contact form. A dedicated podcast production subpage sells tiered podcast packages.

## Positioning
Full-service media company rooted in broadcast engineering with 25+ years of experience. Differentiates on technical depth (RF, studio buildouts, FCC compliance) combined with modern digital services (web, social, podcasting) under one roof. Portfolio skews conservative media (Hannity, Joe Pags, Liz Peek, Jeffrey Lord, The Drill Down) and American-branded consumer products (Nashville Distillery, America Is Good). Tagline: "The Future of Media." Proprietary M3 Analytics platform cited as a differentiator for publishers.

## Operating Context
Static marketing site. Two HTML pages (index.html, podcast-production.html) with no build system, no framework, no CMS. Hosted on static infrastructure. Contact form submits to Formspree (endpoint mdalgznk). Phone: 860-940-0455. Email: info@m3media.com (general), podcasts@m3media.com (podcast division). Location stated as New York, NY. Domain: m3media.com.

## Capabilities and Constraints
Can: Display service offerings, portfolio of 9 client sites plus M3 Analytics, talent management overview, podcast pricing tiers (Starter/Professional/Enterprise, "Call for Pricing"), collect leads via contact form.
Cannot: Dynamic content, CMS-driven updates, e-commerce, authenticated user sessions, blog/news publishing, analytics beyond what Formspree provides. No backend. No JavaScript framework. All content is hardcoded in HTML.

## Brand Commitments
Visual identity: Deep navy background (#080F1E to #14253F range), red accent (#C41E2A), white text at varying opacities. Angled/skewed stripe motifs throughout. American flag iconography in nav and hero. Typography: Bebas Neue (display), Barlow/Barlow Condensed (body) on index; Instrument Serif + Outfit on podcast page (inconsistent with index). Clip-path parallelogram shapes on buttons. Scroll-reveal animations. Reduced-motion support present. Voice: Professional, patriotic, direct. "Built for Broadcast," "Proudly American."

## Evidence on Hand
Stats claimed on index: 25+ years experience, 500+ projects, 150+ broadcast stations, 25+ talent managed. Stats claimed on podcast page: 150+ shows produced, 12M total downloads, 98% client retention, 24h average turnaround. No external analytics, testimonials, or third-party validation visible in codebase.

## Product Principles
- Engineering credibility first -- lead with technical broadcast expertise, not generic agency positioning.
- Portfolio as proof -- real client screenshots, not stock imagery.
- Single conversion goal -- drive visitors to the contact form or phone.
- Conservative media alignment -- client roster and "Proudly American" branding signal market positioning without explicit political messaging on the site itself.

## Accessibility & Inclusion
Reduced-motion media query implemented (disables animations, transitions). Aria-labels on social media icon links. No skip-to-content link. No visible focus styles defined beyond browser defaults. Form inputs lack explicit aria attributes. Color contrast of muted text (white at 50-70% opacity on dark navy) likely fails WCAG AA for body copy. Mobile hamburger menu toggles class but no ARIA expanded state. No lang attribute inconsistencies (en declared). No alt text issues observed on portfolio images. Overall: partial accessibility investment, gaps in keyboard navigation and contrast.
