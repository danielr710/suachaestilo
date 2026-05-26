# Suacha Estilo - E-commerce Site

## Goal
Build a working, visually improved e-commerce site for Suacha Estilo (streetwear clothing).

## Constraints & Preferences
- Must work on GitHub Pages (https://danielr710.github.io/suachaestilo)
- Custom PNG files: `SUACHA-ESTILO rojo.png` (logo, favicon, preloader) and `BASE 2026.png` (hero background)
- Fonts: Urae Nium (brand/display, via fonts.cdnfonts.com) + Inter (body) + Bebas Neue (fallback)
- Smooth animations only — no jarring/brusque movements
- No text scramble on h1
- No duplicate scroll observers
- Reduced float/hover intensity
- Product overlay always visible on mobile at bottom
- WhatsApp with pre-filled contextual messages
- Offers/urgency section removed entirely
- Tagline: "Cultura en movimiento"
- 15 products with realistic prices ($34.900–$159.900) and detailed descriptions
- Brand image from Google Photos URL
- All product images replaced with gradient-backed emoji placeholders

## Key Files
- `C:\Users\pipeee\OneDrive\Escritorio\suachaestilo\index.html` — single-file app with inline CSS/JS
- `C:\Users\pipeee\OneDrive\Escritorio\suachaestilo\SUACHA-ESTILO rojo.png` — brand logo PNG
- `C:\Users\pipeee\OneDrive\Escritorio\suachaestilo\BASE 2026.png` — hero background

## Architecture
- Single HTML file (~85 KB)
- Products stored in JS `products` array (IDs 1-15)
- Cart via `localStorage` key `se_cart`
- Cart persisted: `storeCart()`, `loadCart()` on page load
- WhatsApp: floating button + footer + mobile bottom bar + quick-view modal + location section; all pre-filled with contextual messages
- Cart sidebar footer has dynamic WhatsApp button that generates order summary from cart items
- Preloader fades out after 2.1s with pulse animation on logo
- Particles canvas in hero section
- Quick view modal with size/color selectors, stock badge, add-to-cart
- Chatbot IA in bottom right

## Key Decisions
- All `<img>` tags removed from product/gallery/cart/modal rendering — replaced with emoji + gradient placeholders. Only `<img>` remaining: preloader logo (SUACHA-ESTILO rojo.png) and nav logo circle (Facebook CDN URL).
- No `onerror` handlers needed since no external image URLs are used for products
- No urgency/ofertas section, timer, or related JS/CSS
- No text scramble, no duplicate scroll observers, no duplicate scroll progress
- Reduced animation intensity: float 2px (was 8px), card hover -4px (was -8px), no badge float, no h2 span float, no hero h1 span float
- Urae Nium is a non-commercial-use font; needs licensing for commercial use

## All Edits Applied (current session)
- Added Urae Nium CDN link, applied to all `.font-display` and branded elements
- Updated favicon/apple-touch-icon to use SUACHA-ESTILO rojo.png
- Updated body font to Inter
- Hero bg: BASE 2026.png + gradient fallback (no hover scale)
- Preloader: `<img src="SUACHA-ESTILO rojo.png">` with pulse animation
- Hero tagline: "Cultura en movimiento"
- Hero paragraph: full brand story about hip hop culture since 2011
- Removed "Ofertas" from nav, hero CTA, and all related HTML/CSS/JS
- Brand section: Google Photos URL background image, full brand story (two paragraphs), "Suacha Estilo — Desde 2011" quote
- Badge text: "Desde 2011"
- Products array: 15 items with realistic pricing ($49.900–$159.900) and detailed descriptions (grammage, materials)
- Removed urgency section, urgencyProducts array, timer JS/CSS
- Removed all `<img>` / `onerror` / `onload` from product cards, gallery, cart items, quick view modal
- Removed second scroll reveal IIFE, text scramble IIFE, duplicate scroll progress IIFE
- Removed gallery img/onerror references
- Reduced animation intensity: float -2px, card hover -4px, card active .98, badge no float, h2 span no float, h1 span no float, no hover scale on hero bg, no hover scale on product img
- WhatsApp: all links pre-filled with contextual messages, hover scale 1.1 (no rotate), animation plays once on load
- Mobile: product overlay always visible at bottom with gradient
- Cart: emoji placeholders instead of img for cart items

## Blocked
- Netlify/GitHub Pages deployment: no CLIs available in this environment

## Next Steps (if needed)
- Deploy to GitHub Pages via git push
- Optionally: add related products in quick view, social proof notifications, SEO improvements
