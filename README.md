<div align="center">

<img src="img/LUMAVI_Roof_Clear.png" alt="LUMAVI Properties" width="180"/>

# LUMAVI Properties

### *Rescatando hogares. Restaurando comunidades.*

**A full-stack real estate platform for Puerto Rico — built to rescue abandoned properties and return them to families as dignified homes.**

[![Live Site](https://img.shields.io/badge/🌐_Live_Site-lumavipr.com-8dc648?style=for-the-badge)](https://lumavipr.com)
[![Made in PR](https://img.shields.io/badge/Made_in-Puerto_Rico_🇵🇷-blue?style=for-the-badge)](https://lumavipr.com)
[![Built with Claude](https://img.shields.io/badge/Built_with-Claude_AI-D97757?style=for-the-badge&logo=anthropic)](https://anthropic.com)

[**Visit the Site →**](https://lumavipr.com) · [**Read the Blog**](https://lumavipr.com/blog.html) · [**Meet the Team**](https://lumavipr.com/nosotros.html)

</div>

---

## 🏡 About LUMAVI

LUMAVI Properties exists for one reason: **to give abandoned and deteriorated properties in Puerto Rico a second life.** We work with herederos, families dealing with sucesiones, and owners off-island — handling each property with the dignity its story deserves.

Our name comes from three generations of *Luz* — **Lu**z (abuela) · **Lu**ière (Lumi) — and **Av**i, my son Xavier. Three generations of light, now used to bring light back to homes that have lived in darkness for years.

> *"Cada casa abandonada es una historia esperando a ser restaurada."*
> — Lumier Rodríguez, CEO & Fundador

---

## ⚡ What This Platform Does

This isn't a brochure site. It's a full operating system for a real estate company:

### 🏠 For the Public

- **Property rescue services** — direct contact to sell, rent, or finance properties
- **Contractor registration** with photo upload and skill matching
- **Job applications** with role-specific workflows
- **Blog** with stories from the field — SEO-optimized for search visibility
- **Team page** — meet the humans behind the work
- **Installable mobile app** (PWA) — works offline, works on iPhone and Android

### 🔧 For the Team (Internal Portal)

- **Lead capture** during client calls — instant pipeline entry
- **Field capture** with GPS auto-fill + camera + offline support
- **Visit mode** — comprehensive 10-zone property inspections with star ratings, photos per zone, and voice notes (max 2 min)
- **Deal analyzer** — 9 investment strategies with custom LUMAVI parameters (1.5% rule, 12% cap rate minimum, MAO formula, flip targets)
- **Project management** — from acquisition through rehabilitation to delivery
- **Internal wiki** — scripts, procedures, FAQs, training, legal, policies
- **Investor reports** — automated metrics and KPIs
- **Role-based access** — admin, analyst, editor, temp roles with proper permissions

---

## 🛠️ Tech Stack

Built fast, built right, no vendor lock-in:

### Frontend
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat&logo=pwa&logoColor=white)

### Hosting & DevOps
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat&logo=netlify&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)

### Content & Data
![Decap CMS](https://img.shields.io/badge/Decap_CMS-FF0049?style=flat)
![Google Sheets](https://img.shields.io/badge/Google_Sheets-34A853?style=flat&logo=googlesheets&logoColor=white)
![Apps Script](https://img.shields.io/badge/Apps_Script-4285F4?style=flat&logo=google&logoColor=white)
![Airtable](https://img.shields.io/badge/Airtable-FCB400?style=flat&logo=airtable&logoColor=white)

### Forms & Auth
![Netlify Identity](https://img.shields.io/badge/Netlify_Identity-00C7B7?style=flat&logo=netlify&logoColor=white)
![Formspree](https://img.shields.io/badge/Formspree-E5122E?style=flat)

### Analytics & SEO
![Google Analytics](https://img.shields.io/badge/Google_Analytics-E37400?style=flat&logo=googleanalytics&logoColor=white)
![Schema.org](https://img.shields.io/badge/Schema.org-1A8FD3?style=flat)

---

## 🏗️ Architecture

```
┌────────────────────────────────────────────────────────────────────┐
│                         LUMAVIPR.COM                                │
├────────────────────────────────────────────────────────────────────┤
│  PUBLIC PAGES (SEO-indexed)        INTERNAL PORTAL (auth required) │
│  ├─ index.html (home)              ├─ interno.html (team home)    │
│  ├─ blog.html + /blog/[slug]       ├─ captura.html (call entry)    │
│  ├─ nosotros.html (team)           ├─ captura-campo.html (field)   │
│  ├─ contratistas.html              ├─ visita.html (inspection)     │
│  ├─ aplica.html (3 programs)       ├─ seguimiento.html (pipeline)  │
│  ├─ ayuda.html                     ├─ analisis.html (deal analyzer)│
│  └─ empleos.html                   ├─ proyectos.html               │
│                                    ├─ wiki.html (knowledge base)   │
│                                    └─ admin/ (CMS)                 │
└────────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌────────────────────────────────────────────────────────────────────┐
│                       BUILD PIPELINE                                │
│  /posts/*.md  ──┐                                                  │
│  /wiki/*.md   ──┼──▶  build.js  ──▶  posts.json + wiki.json       │
│  /team/*.md   ──┘                ──▶  team.json                    │
│                                  ──▶  /blog/[slug].html (SEO)      │
│                                  ──▶  sitemap.xml                  │
└────────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌────────────────────────────────────────────────────────────────────┐
│                    DATA INTEGRATIONS                                │
│  • Google Sheets ◀──── Apps Script ◀──── Form submissions          │
│  • Airtable      ◀──── Direct API   ◀──── Deal analyzer            │
│  • Google Drive  ◀──── Direct upload ◀─── Contractor photos        │
│  • Formspree     ◀──── Public forms                                │
└────────────────────────────────────────────────────────────────────┘
```

---

## 🚀 Key Features

| Feature | What It Does |
|---|---|
| 📱 **PWA** | Installs to phone home screen. Works offline (critical in rural PR). Camera + GPS access. |
| 🔍 **SEO-Optimized** | Each blog post gets its own URL, JSON-LD schema, Open Graph tags, sitemap.xml |
| 📍 **Field Capture** | Team captures leads on-site with GPS auto-fill, camera, and offline queue |
| 🎤 **Visit Mode** | 10-zone property inspections with star ratings, multi-zone photos, voice notes |
| 📊 **Deal Analyzer** | 9 investment strategies, custom LUMAVI parameters, instant verdict |
| 🔐 **Role-Based Auth** | Admin / Analyst / Editor / Temp roles via Netlify Identity |
| 📝 **CMS-Powered** | Non-technical team members publish blog posts, wiki articles, team profiles |
| 🔄 **Offline-First** | Forms queue locally when no signal, auto-sync when reconnected |
| 🌐 **Bilingual-Ready** | Built in Spanish, structured to support English translations |
| 📈 **Analytics** | Google Analytics + custom event tracking across all flows |

---

## 📊 By the Numbers

- **28** HTML pages
- **3** CMS-managed content collections (blog, wiki, team)
- **9** investment strategies in the deal analyzer
- **10** inspection zones in visit mode
- **7** user role hierarchies
- **6** social media platforms integrated
- **1** mission: restoring homes, restoring communities

---

## 🎯 What Makes This Different

Most real estate companies have a website. We have an **operating system**:

- **Built for the field**, not just the desk — half the platform runs from a phone
- **Built for non-technical teams** — wife edits the blog, HR posts jobs, temps capture leads, all without touching code
- **Built for Puerto Rico specifically** — bilingual considerations, spotty internet, SURI compliance, herederos workflows
- **Built with dignity in mind** — every form, every page, treats clients and contractors like the experts they are

---

## 📞 Get in Touch

**LUMAVI Properties** is actively rescuing properties across Puerto Rico.

- 🌐 **Website:** [lumavipr.com](https://lumavipr.com)
- 📧 **Email:** [casaslumavi@gmail.com](mailto:casaslumavi@gmail.com)
- 📱 **Phone / WhatsApp:** [(787) 454-2924](tel:+17874542924)
- 📍 **Location:** San Juan, Puerto Rico

### Follow Us

[![Instagram](https://img.shields.io/badge/Instagram-@lumaviproperties-E4405F?style=flat&logo=instagram&logoColor=white)](https://www.instagram.com/lumaviproperties/)
[![TikTok](https://img.shields.io/badge/TikTok-@lumaviproperties-000000?style=flat&logo=tiktok&logoColor=white)](https://www.tiktok.com/@lumaviproperties)
[![Facebook](https://img.shields.io/badge/Facebook-LUMAVI_Properties-1877F2?style=flat&logo=facebook&logoColor=white)](https://www.facebook.com/LUMAVIPROPERTIES/)
[![Threads](https://img.shields.io/badge/Threads-@lumaviproperties-000000?style=flat&logo=threads&logoColor=white)](https://www.threads.com/@lumaviproperties)
[![X](https://img.shields.io/badge/X-@lumavipropertie-000000?style=flat&logo=x&logoColor=white)](https://x.com/lumavipropertie)
[![Snapchat](https://img.shields.io/badge/Snapchat-@casaslumavi-FFFC00?style=flat&logo=snapchat&logoColor=black)](https://www.snapchat.com/@casaslumavi)

---

## 🤝 Want to Work With LUMAVI?

- **Selling, renting, or financing a property?** → [Apply here](https://lumavipr.com/aplica.html)
- **Contractor / craftsperson?** → [Join our team](https://lumavipr.com/contratistas.html)
- **Looking for a job?** → [See openings](https://lumavipr.com/empleos.html)
- **Need help understanding your options?** → [Ask anything](https://lumavipr.com/ayuda.html)

---

## ⚖️ License & Credits

© 2025-2026 **LUMAVI Management Inc.** All rights reserved.

This codebase is the proprietary intellectual property of LUMAVI Management Inc.

Developed with assistance from **[Claude AI by Anthropic](https://anthropic.com)** — a productive collaboration between human vision and AI capability.

---

<div align="center">

**Restaurando hogares. Restaurando comunidades.**
*One property at a time.*

🇵🇷 Made with care in San Juan, Puerto Rico 🇵🇷

</div>
