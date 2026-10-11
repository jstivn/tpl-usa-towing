# Car Recovery Pro Dubai

Production landing page and dispatch interface for a 24/7 commercial vehicle recovery and heavy transport service operating across the Emirate of Dubai, UAE.

Client: **BALODA CARGO TRANSPORT BY HEAVY TRUCKS (L.L.C)**  
Commercial License: **PCFC - Trakhees License No. 614541**  
Live Deployment: [carrecoverypro.com](https://carrecoverypro.com) | Edge Mirror: [evo1.jstivn.workers.dev](https://evo1.jstivn.workers.dev)

---

## Overview

A responsive single-page web application engineered for high-intent emergency towing inquiries in Dubai. Designed to achieve zero layout shifts, instant touch response on mobile viewports, and compliance with Dubai Department of Economy and Tourism (DET) and Trakhees business verification standards.

---

## Technical Specifications

### Core Stack
- **Markup**: Semantic HTML5 (accessible document outline, explicit ARIA roles).
- **Styling**: Tailwind CSS (custom design tokens for UAE roadside assistance branding).
- **Typography**: Google Fonts (*Barlow Semi Condensed* for primary headlines, *DM Sans* for body copy).
- **Icons**: Font Awesome 6.5 SVG vector set.
- **Hosting & Delivery**: Cloudflare Edge CDN with global asset caching and DNS routing.

### Key Engineering Features

1. **Dynamic Rate Estimator**
   - Client-side rate calculation engine for multiple vehicle categories (Motorcycles, Sedans, SUVs, Sports/Luxury vehicles).
   - Real-time updates without page reloads or layout thrashing.

2. **Mobile Viewport & Touch Optimization**
   - Explicit `touch-action: pan-y` and horizontal overflow containment (`overflow-x: hidden !important`) to eliminate accidental horizontal swiping on mobile browsers.
   - Decoupled static header positioning on small screens to prevent iOS Safari dynamic toolbar clipping.

3. **Structured Data (Schema.org JSON-LD)**
   - Complete `EmergencyService` schema embedded in `<head>`.
   - Incorporates street-level address (`Liwan Mazaya, Dubai, AE`), geographic coordinates (`25.1189, 55.3783`), operating hours (`24/7`), phone dispatch line, and official trade license number.
   - Calibrated for Google Local Map Pack indexing.

4. **Direct Telephony and WhatsApp Dispatch Protocol**
   - Pre-formatted URL encoding for WhatsApp messaging that automatically structures user vehicle type, location, and service requirements into the dispatch queue.

---

## Repository Structure

```
├── index.html               # Main production document with embedded JSON-LD
├── images/                  # Catalog vehicle cutouts, background assets, service photography
│   └── evo2/               # Client fleet photography (heavy-duty flatbed haulers)
├── car_recovery_logo.jpg    # Primary identity asset
├── .gitignore               # Build, local tooling, and OS artifact filter
└── README.md                # System documentation
```

---

## Performance & Optimization

- **Cumulative Layout Shift (CLS)**: 0.00
- **Time to First Byte (TTFB)**: < 50ms via Cloudflare Edge Network
- **Zero Heavy Framework Runtime**: Pure static assets for instant evaluation on unstable 4G/5G mobile connections in desert transit corridors (E11, E311, E611).

---

## Legal & Accreditation

Developed under contract for BALODA CARGO TRANSPORT BY HEAVY TRUCKS (L.L.C). All commercial trademarks, vehicle registration numbers, and license identifiers are property of the respective legal entity. Code provided for technical evaluation and portfolio review.
