# Website Specification: Dübi Style Outlet

**The Mission:**
Develop a high-conversion, performance-optimized **Jekyll** static site. The design must translate a physical business card aesthetic into a "Premium Dark Mode" digital experience.

### 1. Visual & Interactive Identity

* **Color Palette (Locked):**
* **Background:** `#0A0A0A` (Deep Matte Black).
* **Primary Accent:** `#4ED7CD` (Electric Teal). Use for headings and primary borders.
* **Action Accent:** `#FF3F6A` (Punchy Pink). **Strictly** for CTAs, discounts, and the `%` slash.


* **Typography:**
* **Headlines:** *Montserrat* or *Syne* (Bold, 700+ weight, 0.05em letter spacing).
* **Body:** *Inter* or *Roboto* for readability against dark backgrounds.


* **Micro-Interactions:**
* **The "Dibi-Pulse":** Buttons should have a 2px solid Teal border that transitions to a solid Pink fill on hover.
* **SVG Animation:** The brand `%` mark should subtly scale (1.05x) when the user scrolls into the Hero section.



---

### 2. The Architectural Build

**A. Jekyll Structure:**

* **Collections:** Implement `_products` with the following Front Matter requirements:
```yaml
layout: product
title: "Brand Name Item"
price: 45.00
discount_percent: 20  # Triggers the Pink % badge
category: "Footwear"
featured: true

```


* **Data Driven:** Use `_data/store.yml` for hours, address, and social links to ensure global updates are "one-file" simple.

**B. Component Breakdown:**

1. **Navbar:** Sticky glassmorphism effect (`backdrop-filter: blur`). Teal links, Pink CTA.
2. **Hero Section:** Ensure the 'DibiStyle' logo itself, including the teal letters, the teal `%` circle, and the pink `%` slash, is recreated with crisp, scalable vector graphics (SVG). The stylized `%` in the 'b' is the core brand mark.
3. **Product Grid:** Use **CSS Grid** (3-column desktop, 1-column mobile). Cards should have a subtle `#1A1A1A` background to lift them off the pure black floor.
4. **Dark Maps:** Integrate MapBox or Leaflet with a "Dark/Monochrome" tile set, using Teal `#4ED7CD` for the location pin.

---

### 3. Performance & SEO Requirements

* **Images:** All product assets must be processed via `jekyll-images` or converted to `.webp`.
* **SEO:** Include `jekyll-seo-tag`. Every product page must auto-generate Meta Descriptions from the first 160 characters of the product Markdown file.
* **Responsiveness:** Mobile-first. The "Find Deals" button must become a fixed-bottom "Sticky Bar" on screens smaller than 600px.

