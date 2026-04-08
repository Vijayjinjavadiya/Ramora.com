# Ramora Technologies — Company Website

The official website for [Ramora Technologies](https://ramoratech.com), an IoT and embedded systems engineering company. This is a static frontend built in plain HTML, CSS, and JavaScript — no frameworks, no build step, just clean code that loads fast.

---

## What's in here

```
Ramora.com/
├── index.html              # Main landing page
├── about-us.html           # About the team
├── project-details.html    # Case study page (dynamic, query-param driven)
├── style.css               # Global styles
└── images/                 # All assets — logos, product shots, section artwork
    └── logos/              # Tech stack icons
```

The site covers everything a prospective client or partner would want to know: what we do, how we work, who we've built for, and how to get in touch. The portfolio section pulls from a JS data object and renders dynamically, so adding new case studies is a one-file edit.

---

## Pages

**Home (`index.html`)**
Hero, "Concept to Production" section, Why Us, Services overview, Sprint-based project management explainer, Tech Stack, Hire Developers (tabbed by discipline), Portfolio with category filters, and a Contact form.

**About Us (`about-us.html`)**
Company background, team philosophy, and core principles — End-to-End Expertise, Rapid Prototyping, Transparent Communication.

**Project Details (`project-details.html`)**
Reusable case study template. Pass `?id=<project>` in the URL and it renders the right content. No separate HTML file per project needed.

---

## Portfolio projects covered

| Project | Domain |
|---|---|
| Asset Tracking Solution | Industrial IoT |
| Underwater Diver Safety System | Communication / Marine |
| Intelligent Geofence System | Logistics & Tracking |
| Sub-Centimeter Positioning (UWB) | Worker Safety — UK Rail |
| Depth & Temp Logger | Marine Research |
| Fishermen Gear Accountability | Coastal Fleet Management |
| Lightweight Asset Beacon | Extended Battery / Field Deployment |
| Portable Timing System | Sports Tech (MTB Racing) |
| Lign Light Oxygen Indicator | Diver Safety |

---

## Tech we work with

Things you'll see referenced across the site and the work we've done:

**Embedded & Firmware** — STM32, Nordic nRF series, ESP32/Espressif, Arduino, Raspberry Pi, FreeRTOS  
**Connectivity** — BLE, LoRaWAN, UWB, MQTT  
**Languages** — C, C++, Python  
**Mobile** — Android (Java/Kotlin), iOS (Swift), React Native, Flutter  
**Frontend** — React, Angular  

---

## Running locally

No build tools. Just open the files.

```bash
git clone https://github.com/your-org/Ramora.com.git
cd Ramora.com

# Option 1 — Python (built-in)
python3 -m http.server 8000

# Option 2 — Node (if you have it)
npx serve .
```

Then go to `http://localhost:8000`.

Opening `index.html` directly as a `file://` URL mostly works, but some browser security policies block local font and image requests — the dev server avoids that.

---

## Making changes

**Adding a portfolio project**
Find the portfolio data object in `index.html` (search for `portfolio-title`) and add your entry there. The grid and filters update automatically.

**Adding a case study page**
Add an entry to the project data in `project-details.html`. The template handles layout — you just provide the content.

**Changing services**
Edit the services grid in `index.html` directly. Each card is self-contained.

**Images**
Drop new assets into `/images`. Keep filenames lowercase with hyphens — the existing ones are inconsistent because they came from design exports, but new additions should follow a clean convention.

---

## Contact

**Email:** hello@ramoratech.com  
**Website:** [ramoratech.com](https://ramoratech.com)

For project inquiries, the contact form on the site is the fastest path. For anything code-related, open an issue or PR here.
