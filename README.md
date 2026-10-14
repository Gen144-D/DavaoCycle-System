# DavaoCycle System Design 

This document specifies the design system, visual identity, and user interface guidelines for **DavaoCycle**, a bike-sharing and micro-mobility rental platform based in Davao City. 

## Application Screenshot


<img width="1200" height="541" alt="download" src="https://github.com/user-attachments/assets/a5fac705-54a3-418b-865f-59f341d22ead" />
---

## 1. Brand Identity & Strategy
* **System Name:** DavaoCycle (CamelCase preferred for app elements; "Davao Cycle" for general copy).
* **Core Philosophy:** Eco-friendly urban mobility, accessible city commuting, and recreational health.
* **Target Environment:** Seamless integration with the [Davao City Bicycle Ordinance](https://idisphil.org/wp-content/uploads/2019/02/Bicycle-Ordinance-of-2010.pdf "Bicycle-Ordinance-of-2010.pdf") framework, supporting local city bicycle lane networks.

---

## 2. Color Palette (Design Tokens)

| Token Name | Hex Value | Purpose & Usage |
| :--- | :--- | :--- |
| **`brand-primary`** | `#00875A` | **Durian Eco-Green**: Primary brand color representing sustainability and local identity. |
| **`brand-secondary`** | `#FFC72C` | **Davao Sunshine**: Accents, active bicycle pins, system notifications, and primary warnings. |
| **`ui-dark`** | `#1A202C` | **Asphalt Gray**: High-contrast text, major background elements, and footer sections. |
| **`ui-light`** | `#F7FAFC` | **Off-White**: Application backgrounds, canvas cards, and default viewports. |
| **`status-active`** | `#2B6CB0` | **Lane Blue**: Represents active routes or designated local bike lanes. |

---

## 3. Typography
* **Primary System Font:** `Inter`, `system-ui`, `-apple-system`, sans-serif (Clean, modern geometric sans to ensure readability on mobile screens during outdoor bike navigation).
* **Headings (`H1`, `H2`, `H3`):** Bold weights (`700`), slight track compression (`letter-spacing: -0.02em`).
* **Body Text:** Regular weight (`400`), highly readable `line-height: 1.6`.

---

## 4. Key UI Components & Layout Logic

### A. Mobile App Map View (Main Screen)
* **Background:** OpenStreetMap canvas styled with light minimal tokens.
* **Overlays:** 
  * Floating search bar at the top for "Find a Dock" or "Find a Bike."
  * Custom map markers utilizing `brand-primary` circles with an embedded white bicycle icon to represent available fleets.
  * Low-stock docks switch automatically to a `brand-secondary` highlight color.

### B. Fleet & QR Scanner Screen
* **Scanner Target:** Centered viewbox with interactive safety overlay lines.
* **Bottom Sheet Modal:** Pops up instantly upon scanning a bike's QR code. Shows:
  * Bike ID and battery/mechanical status.
  * Clear action buttons styled in solid `brand-primary` with white text.

### C. Booking & Web Dashboard Layout
* **Cards:** White canvas with minimal borders (`1px solid #E2E8F0`) and smooth rounded corners (`border-radius: 12px`).
* **Tables:** Clean alternating striping for trip histories, highlighting rental costs and distances covered.

---

## 5. Compliance & Structural Standards
* **Local Regulations:** The digital checkout flow must explicitly prompt or display local rules such as **mandatory helmet use**, adherence to dedicated lanes, and checking standard safety features (brakes, reflectors) in compliance with the [Davao City Transport and Traffic Code](https://lissp2.davaocity.gov.ph/uploads/items/5659/Ordinance%20No.%200782-21.pdf "Ordinance No. 0782-21.pdf").
* **Responsive Breakpoints:**
  * Mobile: `< 640px` (Default core interface layout for smartphone users unlocking bikes).
  * Desktop: `> 1024px` (Admin panel for managing fleets, bike stations, and user accounts).



