ROLE
You are a senior front-end developer and UI/UX designer. Build a complete, production-quality, fully responsive STATIC multi-page website using PHP (includes only, no database), Bootstrap 5.3, Bootstrap Icons, and vanilla JS. Design reference for look and feel: https://www.cummins.com/en-in/generators (clean industrial corporate style, big hero banners, product cards, strong whitespace, bold typography). Website must be highly informative, with best-in-class UI/UX and a well-organised structure.

BUSINESS
Name: NAYYAR GENERATOR HIRING CO.
Head Office: 304, Brooke Street, Meerut Cantt. - 250001 (U.P.), India
Email: winkle_n@yahoo.com
Phone: +91-9837020709, +91-9810032004
International office: Dubai
Tagline idea: "Power You Can Trust. Anywhere. Anytime."
Brands: Perkins (Diesel Power), Cummins, Stamford | AvK alternators, Leroy Somer alternators.
Key facts from company brochure:
- Authorized OEM of Perkins powered diesel generating sets from 30 KVA onwards with international warranty.
- New-age Stamford / Leroy Somer alternators from 7.5 KVA to 2250 KVA, low voltage 400 V up to high voltage 33 KV output.
- Supplier of Cummins diesel generators from 7.5 KVA to 2250 KVA as per customer requirement; also supplies ISO containerised diesel gensets.
- One of the largest exporters of Perkins and Cummins diesel generators from India; international office in Dubai.
- Supplied to more than 65 countries; actively seeking new markets.
- Soundproof diesel generators of Germinal Technologies Pvt. Ltd. range from 7.5 KVA to 2250 KVA.
- Containerised gensets are fully self-sufficient, plug and play; entire fuel, exhaust and cooling system is integral to the container, designed for all-weather performance; housed in ISO container for easy lifting and quick transportation.
- Services: design and advice on generator installation for commercial and industrial outfits; bespoke generator solutions or captive power plants considering property size, power usage and budget; consideration of civil work, transformers, control and switchgear, AMF and synchronous controls, generator and UPS, acoustic and complete fuel handling solutions; automation of the entire power generation process for uninterrupted supply; ongoing maintenance support so the generator runs at peak efficiency.

THEME & DESIGN SYSTEM
- Colors: Primary Red #D71920 (hover darker red #A8121A), Black #111111, White #FFFFFF, Light Grey #F5F5F5, Mid Grey #6B6B6B, Dark Teal accent #007A6E (from brochure "What we do" block, use sparingly). Define all as CSS variables on :root.
- Fonts (Google Fonts): "Raleway" for headings, "Poppins" or "Inter" for body.
- Buttons (IMPORTANT):
  1. Primary button: red background, white text, fully rounded PILL (border-radius 50rem), padding 12px 28px, bold. Hover: black background, white text, smooth 0.3s transition.
  2. Secondary button: white background, black text, 2px black border, PILL. Hover: black background, white text.
  3. Use primary for main CTAs (Get Quote, Call Now), secondary for "View Details", "Download Brochure", etc.
- Cards: white, subtle shadow, 12px radius, hover lift (translateY -6px) + red top border.
- Section titles: bold heading with short red underline bar (like brochure).
- Sticky navbar with shadow on scroll, white background, red active link underline, red pill "Get a Quote" button on right.
- Top bar above navbar: phone numbers, email, small social icons.
- Smooth scroll, AOS or CSS fade-in-on-scroll animations, back-to-top red circular button, floating WhatsApp button (link wa.me/919837020709).
- Accessible (alt text, aria labels, good contrast), fast (lazy-load images).

PHP STRUCTURE
/index.php
/about.php
/products.php (tabs: Perkins | Cummins | Containerised | Soundproof)
/services.php
/rental.php
/industries.php (or clients.php)
/contact.php (form posts to contact-handler.php which validates and uses mail(); show Bootstrap alert on success/fail; add honeypot field + basic server-side sanitisation)
/includes/header.php (head, meta, topbar, navbar)
/includes/footer.php (footer, scripts)
/includes/config.php (site name, phone, email, address as variables, reused everywhere)
/data/perkins.php and /data/cummins.php (PHP arrays of models, looped to render tables)
/assets/css/style.css, /assets/js/main.js, /assets/img/
Each page sets $pageTitle and $pageDesc before including header.php for SEO. Add Open Graph tags, favicon, sitemap.xml, robots.txt.

HOME PAGE SECTIONS (in order)
1. HERO: full-width carousel (3 slides) with dark overlay. Slide headlines: "Authorized OEM of Perkins Powered Diesel Generators", "Cummins Diesel Generators from 7.5 to 2250 KVA", "Plug & Play Containerised Power Solutions". Buttons: red pill "Get a Quote" + white pill "View Products".
2. STATS STRIP (animated counters, red background, white text): 65+ Countries Supplied, 7.5-2250 KVA Range, 400V to 33KV Output, Dubai International Office.
3. ABOUT SNIPPET: left image, right text: authorized OEM of Perkins powered diesel gensets from 30 KVA onward with international warranty; supplier of Cummins gensets 7.5-2250 KVA; one of the largest exporters of Perkins and Cummins generators from India. Pill button "Know More".
4. BRAND LOGOS ROW: Perkins, Cummins, Stamford AvK, Leroy Somer (grayscale, color on hover).
5. PRODUCT CATEGORIES (4 cards): Perkins Generators (30-2250 kVA), Cummins Generators (7.5-2250 kVA), Soundproof / Silent Gensets, ISO Containerised Gensets. Each with "View Details" white-black pill.
6. KVA RANGE FINDER: small interactive widget - user selects kVA range (7.5-50, 60-250, 300-750, 810-2250) and sees matching models with link to products page.
7. WHY CHOOSE US (6 icon boxes): Authorized OEM, International Warranty, 65+ Countries Exported, Custom-Designed Power Solutions, AMF/Synchronising Automation, Ongoing AMC & Maintenance Support.
8. SERVICES PREVIEW: design and advisory, captive power plant, civil work, transformers, control and switchgear, AMF and synchronous panels, UPS, acoustic solutions, fuel handling, automation, maintenance.
9. CONTAINERISED GENSET FEATURE BLOCK: dark background, text: fully self-sufficient, plug and play, fuel/exhaust/cooling integrated, designed for all weather, ISO container for easy lifting and quick transport.
10. HOW IT WORKS / PROCESS (4 steps with numbered red circles): Consultation -> Design and Proposal -> Supply and Installation -> Maintenance and Support.
11. INDUSTRIES SERVED (icon grid): Hospitals, Hotels and Hospitality, Telecom, Metro and Infrastructure, Manufacturing and FMCG, Real Estate, Retail, Printing and Publishing, Government and Institutions.
12. TRUSTED CLIENTS: logo grid/marquee: Kiranakart, Mifco, Delhi Metro, Fenaka Corporation, The Leela Palaces Hotels Resorts, Big Daddy, Airtel, Vodafone, Pepsi, EIL, Tata Harrier, United Printing and Publishing, Delhi State Cancer Institute, Shirdi Sai Baba institution, NBCC. (Use text placeholders if logos are not available.)
13. REVIEWS / TESTIMONIALS: Bootstrap carousel, 3 cards visible on desktop, 1 on mobile. Star ratings, name, designation, company. Write 5-6 realistic PLACEHOLDER reviews (clearly marked in a code comment as sample to be replaced with real ones). Themes: reliable uptime, timely delivery, great after-sales service, silent operation.
14. FAQ: Bootstrap accordion, 6-8 questions: difference between kVA and kW, how to choose genset size, do you offer warranty, do you export, soundproof vs open type, AMC availability, rental availability, delivery time.
15. CTA BANNER: red background, white text "Need Power Solution? Talk to Our Experts", white pill button with black text (hover black bg, white text) + phone number.
16. FOOTER: black background; 4 columns: About + logo, Quick Links, Products, Contact (address, phones, email). Bottom bar with copyright and brand logos.

OTHER PAGES
- ABOUT: company story, "What we do" content (OEM, exporter, Dubai office, 65+ countries), mission/vision, timeline placeholder, team placeholder, certifications placeholder, brand partner logos.
- PRODUCTS:
  * Bootstrap pill tabs (red active pill, white/black-border inactive).
  * Perkins tab: table loaded from data/perkins.php. Columns: Genset Model, kVA, kWe, Perkins Engine Model, BHP, Enclosure L x W x H (mm), Weight (kg). Data (50 Hz, 0.8 PF):
    GT30P 30/24 1103A-33G 40 2500x1050x1370 1000
    GT45P 45/36 1103A-33TG1 62 2500x1050x1370 1050
    GT60P 60/48 1103A-33TG2 81 2500x1050x1370 1100
    GT400P 400/320 2206D-E13TAG3 485 5151x1920x2042 5800
    GT500P 500/400 2506D-E15TAG2 605 5151x1920x2042 6000
    GT625P 625/500 2806D-E18TAG1A 724 5151x1920x2042 6400
    GT750P 750/600 4006D-E23TAG2 894 6800x2100x2500 8800
    GT810P 810/648 4008D-E30TAG1 914 7800x2300x2675 10000
    GT910P 910/728 4008D-E30TAG2 1020 7800x2300x2675 10500
    GT1010P 1010/808 4008-30TAG2 1208 7800x2300x2675 11000
    GT1250P 1250/1000 4012-46TAG0A 1497 8500x2500x2775 13500
    GT1500P 1500/1200 4012-46TAG2A 1785 8500x2500x2775 14000
    GT1700P 1700/1360 4012-46TAG3A 2012 8500x2500x3100 15000
    GT1850P 1850/1480 4016-61TRG1 2209 10000x2500x3750 17500
    GT2000P 2000/1600 4016-61TRG2 2378 10000x2500x3750 18000
    GT2250P 2250/1800 4016-61TRG3 2647 10000x2500x3750 18500
  * Cummins tab: table from data/cummins.php (50 Hz, 0.8 PF). Columns: Genset Model, kVA, kW, Cummins Engine Model, BHP, L x W x H (mm), Weight (kg). Data:
    GT7.5D5P 7.5/6 X1.3TAA-G1 23 1460x940x915 550
    GT10D5P 10/8 X1.3TAA-G1 23 1460x940x915 550
    GT15D5P 15/12 X1.3TAA-G1 23 1500x940x1100 610
    GT20D5P 20/16 X1.3TAA-G7 25.3 1780x940x1100 723
    GT25D5P 25/20 X2.7T-G1 32 2400x940x1400 1090
    GT30D5P 30/24 X2.7TAA-G2 38.5 2400x950x1400 1090
    GT35D5P 35/28 X2.7TAA-G7 47.5 2800x1150x1450 1090
    GT40D5P 40/32 X2.7TAA-G8 51 2800x1150x1450 1090
    GT50D5P 50/40 4BTAA3.3-G11 84 2950x1150x1550 1470
    GT62.5D5P 62.5/50 4BTAA3.3-G11 84 2950x1150x1550 1470
    GT82.5D5P 82.5/66 4BTAA3.9-G4 110 3850x1150x1750 1900
    GT100D5P 100/80 6BTAA5.9-G13 159 4000x1150x1850 2200
    GT125D5P 125/100 6BTAA5.9-G13 159 4000x1150x1850 2200
    GT140D5P 140/112 QSB5.9-G1 184 4000x1150x1850 2565
    GT160D5P 160/128 QSB5.9-G2 206 4000x1150x1850 2603
    GT180D5P 180/144 QSB6.7-G14 234 4200x1350x1850 2856
    GT200D5P 200/160 QSB6.7-G15 256 4200x1350x1850 2856
    GT225D5P 225/180 QSB6.7-G16 280 4200x1350x1850 2856
    GT250D5P 250/200 6L8.9TAA-G4 335 4800x1500x2025 4385
    GT300D5P 300/240 QSL9-G15 399 4800x1500x2025 4265
    GT320D5P 320/256 QSL9-G15 399 4800x1500x2025 4385
    GT365D5P 365/292 QSN14-G1 448 5500x1900x2150 6250
    GT400D5P 400/320 QSN14-G2 487 5500x1900x2150 6250
    GT500D5P 500/400 KTAA19-G10 587 6000x2000x2250 8000
    GT600D5P 600/480 KTAA19-G12 713 6500x2000x2800 9029
    GT625D5P 625/500 KTAA19-G13 739 6500x2000x2800 9029
    GT650D5P 650/520 QSK19-G7 828 6500x2000x2800 9029
    GT750D5P* 750/600 KTA38-G12 1069 8000x2600x3000 13000
    GT810D5P* 810/648 KTA38-G12 1069 8000x2600x3000 13000
    GT910D5P* 910/728 KTA38-G17 1069 8000x2600x3000 13000
    GT1010D5P* 1010/808 KTA38-G5 1180 8000x2600x3000 13873
    GT1250D5P* 1250/1000 KTA50-G3 1470 8600x2800x3282 16457
    GT1500D5P* 1500/1200 KTA50-G8-I 1735 9000x2900x3419 17328
    GT1750D5P* 1750/1400 QSK50-G10 2000 10500x3250x3835 19000
    GT2000D5P* 2000/1600 QSK60-G4 2319 10500x3250x3835 25000
    GT2250D5P* 2250/1800 QSK60-G8 2603 10500x3600x3835 25500
    Footnote: "* 750 kVA and above comes with Cap-in type acoustic enclosure. 750 kVA and above can be supplied with open type or container type acoustic enclosure as per requirement."
  * Table features: sticky header, horizontal scroll on mobile, live search box, kVA filter dropdown, "Enquire" red pill button on each row that prefills the contact form with the model name (via query string).
  * Containerised and Soundproof tabs: image, feature list, "Get Quote" pill.
  * Note under tables: "Specifications subject to change. Contact us for latest data sheet."
  * Pill button "Download Brochure" (white bg, black text, hover black).
- SERVICES: cards for design and advisory, captive power plant, civil work, transformers, control and switchgear, AMF and synchronous controls, generator and UPS integration, acoustic solutions, fuel handling, automation, AMC and maintenance.
- RENTAL: genset hire section (placeholder copy, mark in a comment for owner to confirm), rental benefits, simple rental enquiry form (kVA needed, duration, location, date).
- CLIENTS / INDUSTRIES: full client logo grid + industries + testimonials.
- CONTACT: left form (name, phone, email, kVA requirement dropdown, message, pill submit), right info cards (address, phone with tel: links, email with mailto:), Google Maps embed for Meerut Cantt, Dubai office note, working hours placeholder.

RESPONSIVE DESIGN (ALL DEVICES) - MANDATORY
Site must work perfectly on small phones, large phones, foldables, tablets (portrait + landscape), laptops, desktops, ultra-wide monitors and TV-size screens. Mobile-first CSS.

1. Base
- <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
- html { scroll-behavior: smooth; -webkit-text-size-adjust: 100%; }
- img, video, iframe { max-width: 100%; height: auto; }
- No horizontal scroll anywhere (fix root causes; overflow-x hidden only as fallback).
- Use rem and clamp() for type and spacing.

2. Breakpoints (Bootstrap 5.3): xs <576 (min supported 320px), sm >=576, md >=768, lg >=992, xl >=1200, xxl >=1400, ultra-wide >=1920 (container max-width 1320px centered). Add custom tweaks for 320, 375, 1920, 2560.

3. Fluid typography: h1 clamp(1.8rem, 4vw + 1rem, 3.5rem); h2 clamp(1.5rem, 2.5vw + 1rem, 2.5rem); h3 clamp(1.25rem, 1.5vw + 1rem, 1.75rem); body 16px, line-height 1.6, never below 14px on mobile.

4. Section behavior
- Top bar: mobile shows phone + email icons only; lg+ full details.
- Navbar: hamburger below lg using Bootstrap offcanvas (right slide-in, full height, large tap targets, red pill "Get a Quote" at bottom). Sticky, shrinks slightly on scroll.
- Hero: 100svh on mobile (min 520px), 80vh on desktop (svh/dvh units). Headline and buttons stack on mobile with full-width pills; side by side on md+. Use <picture> with separate mobile/desktop images. Hide carousel arrows on touch, keep swipe.
- Stats: 2x2 on xs, 4 in a row on md+.
- About snippet: image on top on mobile, two columns on lg+.
- Brand logos: 2 per row xs, 4 per row md+.
- Product category cards: 1 col xs, 2 col sm/md, 4 col xl.
- KVA finder: pill options wrap/scroll horizontally on xs; results as stacked cards.
- Why choose us: 1 col xs, 2 col sm/md, 3 col lg+.
- Services preview: 1 col xs, 2 col md, 3 col xl.
- Process: vertical timeline on mobile, horizontal with connecting line on lg+.
- Industries: 2 col xs, 3 col md, 5 col xl.
- Clients: 2 col xs, 3 col sm, 4-5 col lg+; marquee slower on mobile, paused on hover/touch; respect prefers-reduced-motion.
- Testimonials: 1 card xs/sm, 2 md, 3 lg+; swipe enabled.
- FAQ: full width, large tap-target headers.
- Footer: 1 col xs (centered), 2 col md, 4 col lg+.
- CTA banner: centered text and full-width button on xs; inline on lg+.

5. Product tables (critical)
- Each table in .table-responsive with horizontal scroll and a "Swipe to see more" hint shown only on xs/sm.
- Sticky first column (Genset Model) and sticky header.
- On xs (<576px) convert each row into a stacked CARD (model name as title, kVA in red pill badge, specs as label/value rows via data-label + ::before, "Enquire" pill at bottom).
- Search box and kVA filter stack on xs, inline on md+.
- Tabs: horizontally scrollable pill row on xs, no wrap, hidden scrollbar.

6. Forms: inputs full width, min-height 48px, font-size >=16px (no iOS zoom); proper types (tel, email, inputmode); two columns on lg+, one below; full-width submit pill on xs.

7. Touch + usability
- Tap targets min 44x44px, 8px spacing.
- Wrap hover effects in @media (hover: hover); add :active and :focus-visible states.
- WhatsApp float and back-to-top: bottom-right, safe-area aware (env(safe-area-inset-bottom)), never overlapping each other or footer content. Mobile-only sticky bottom action bar (Call | WhatsApp | Quote) with red/white pills.
- Google Maps iframe: 100% width, 300px high on mobile, 450px on desktop.
- tel: links active on mobile; plain text number on desktop.

8. Images + performance: srcset + sizes, WebP, loading="lazy" below the fold, fetchpriority="high" on hero image only, width/height attributes to prevent layout shift (CLS < 0.1), smaller images for mobile.

9. Other: landscape phones reduce hero height; orientation change must not break layout; SVG logos/icons for retina; print stylesheet for product tables (hide nav/footer/buttons, black on white); support latest Chrome, Safari (iOS 14+), Firefox, Edge, Samsung Internet, Android WebView; keyboard accessible, screen-reader friendly, red focus-visible outlines, prefers-reduced-motion respected.

UX DETAILS
- Breadcrumb banner on inner pages with dark overlay image.
- Product cards show "kVA badge" in a red pill.
- Click-to-call and click-to-email links everywhere.
- Form validation with Bootstrap validation states.
- loading="lazy" on images, WebP where possible, placeholder images from picsum or unsplash if brochure images are unavailable, with clear comments marking where to replace.
- Page transitions subtle; no heavy libraries beyond Bootstrap 5.3, Bootstrap Icons, AOS (optional).
- Lighthouse target (mobile + desktop): 90+ for Performance, Accessibility, Best Practices, SEO.
- Clean commented code, consistent naming, CSS variables for theme colors.

DELIVERABLES
1. Full folder structure.
2. Complete code for every file (header.php, footer.php, config.php, all pages, data files, style.css, main.js, contact-handler.php, sitemap.xml, robots.txt).
3. Short instructions to run locally (php -S localhost:8000) and deploy to shared hosting.
4. Responsive testing checklist: verify widths 320, 360, 375, 390, 414, 576, 768, 820, 992, 1024, 1280, 1440, 1920, 2560; devices iPhone SE, iPhone Pro Max, Galaxy S, Galaxy Fold, Pixel, iPad Mini/Air/Pro, Surface, 13-inch laptop, 27-inch monitor. No horizontal scroll, no overlap, no cut-off text, tables usable everywhere.
5. List of placeholders the owner must replace (images, logos, reviews, rental copy, social links, map coordinates, brochure PDF).