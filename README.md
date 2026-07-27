<div align="center">

<img src="img/ChatGPT Image Jun 10, 2026, 12_33_06 AM.png" alt="LUMAVI Properties" width="180"/>

# LUMAVI Properties

### *Rescatando hogares. Restaurando comunidades.*

**A full-stack, Airtable-backed SaaS real estate platform for Puerto Rico — built to rescue abandoned properties and return them to families as dignified homes.**

[![Live Site](https://img.shields.io/badge/🌐_Live_Site-lumavipr.com-8dc648?style=for-the-badge)](https://lumavipr.com)
[![Made in PR](https://img.shields.io/badge/Made_in-Puerto_Rico_🇵🇷-blue?style=for-the-badge)](https://lumavipr.com)
[![Built with Claude](https://img.shields.io/badge/Built_with-Claude_AI-D97757?style=for-the-badge&logo=anthropic)](https://anthropic.com)

[**Visit the Site →**](https://lumavipr.com) · [**Read the Blog**](https://lumavipr.com/blog.html) · [**Meet the Team**](https://lumavipr.com/nosotros.html) · [**Contractors →**](https://lumavipr.com/contratistas.html)

</div>

---

## 🏡 About LUMAVI

LUMAVI Properties exists for one reason: **to give abandoned and deteriorated properties in Puerto Rico a second life.** We work with herederos, families dealing with sucesiones, and owners off-island — handling each property with the dignity its story deserves.

Our name comes from three generations of *Luz* — **Lu**z (abuela) · *Luz* — **Lu**z (mom) · **Lu**ière (Lumi) — and **Xav**i, my son Xavier. Three generations of light, now used to bring light back to homes that have lived in darkness for years.

> *"Cada casa abandonada es una historia esperando a ser restaurada."*
> — Lumier Rodríguez, CEO & Fundadora

---

## ⚡ What This Platform Does

This isn't a brochure site. It's a full operating system for a real estate company — a SaaS-like platform where the team logs in through one website, and everything they do is backed by a real relational database.

### 🏠 For the Public

- **Property rescue services** — direct contact to sell, rent, or finance properties
- **Contractor network** — prominent recruitment banner + registration with photo upload
- **Job applications** with role-specific workflows
- **Blog** with individual SEO-optimized post pages, JSON-LD schema, Open Graph tags
- **Team page** — meet the humans behind the work
- **Installable mobile app** (PWA) — works offline, works on iPhone and Android

### 🔧 For the Team (Internal Portal)

**📞 Customer Service & Sales:**
- **Bitácora de Contactos** — customer support call log with routing, escalation, callback tracking, follow-up threads
- **Lead capture** during client calls — instant pipeline entry
- **Seguimiento** — track leads through the sales pipeline
- **Wiki interna** — searchable knowledge base with markdown editing, categories, tags, attachments

**📱 Field Operations:**
- **Field capture** with GPS auto-fill + camera + offline support
- **Visit mode** — comprehensive 10-zone property inspections with star ratings, photos per zone, and voice notes (max 2 min)

**🔨 Construction Operations:**
- **Bitácora de Obra** — daily construction log with 8 categories (progreso, problema, materiales, contratista, inspección, hito, gasto, nota), photo attachments, voice notes, GPS tagging
- **Project management** — from acquisition through rehabilitation to delivery

**📊 Analysis & Business:**
- **Deal analyzer** — 9 investment strategies with custom LUMAVI parameters (1.5% rule, 12% cap rate minimum, MAO formula, flip targets)
- **Investor reports** — automated metrics and KPIs

**🔐 Access Control:**
- **6 role hierarchy** — admin, analyst, ops_manager, editor, support, temp
- Different views + permissions for each role
- Netlify Identity single sign-on

---

## 🛠️ Tech Stack

Built fast, built right, no vendor lock-in:

### Frontend
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?style=flat&logo=pwa&logoColor=white)

### Backend & Serverless
![Netlify_Functions](https://img.shields.io/badge/Netlify_Functions-00C7B7?style=flat&logo=netlify&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)

### Database (SaaS Backend)
![Airtable](https://img.shields.io/badge/Airtable-3_bases-FCB400?style=flat&logo=airtable&logoColor=white)
![Attachments](https://img.shields.io/badge/Airtable_Content_API-attachments-orange?style=flat)

### Hosting & DevOps
![Netlify](https://img.shields.io/badge/Netlify-Hosting-00C7B7?style=flat&logo=netlify&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)

### Content Management
![Decap_CMS](https://img.shields.io/badge/Decap_CMS-Blog_+_Team-FF0049?style=flat)
![Markdown](https://img.shields.io/badge/Markdown-blog_posts-000000?style=flat&logo=markdown&logoColor=white)

### Public Forms & Auth
![Netlify_Identity](https://img.shields.io/badge/Netlify_Identity-team_auth-00C7B7?style=flat&logo=netlify&logoColor=white)
![Formspree](https://img.shields.io/badge/Formspree-public_forms-E5122E?style=flat)

### Analytics & SEO
![Google_Analytics](https://img.shields.io/badge/Google_Analytics-E37400?style=flat&logo=googleanalytics&logoColor=white)
![Schema.org](https://img.shields.io/badge/Schema.org-JSON--LD-1A8FD3?style=flat)
![Open_Graph](https://img.shields.io/badge/Open_Graph-social_previews-1877F2?style=flat)

---

## 🏗️ Architecture

Three-tier design with clean separation:

```
┌────────────────────────────────────────────────────────────────────┐
│                       LAYER 1: LUMAVIPR.COM                         │
│                (Public + Internal HTML — Netlify hosted)            │
├────────────────────────────────────────────────────────────────────┤
│  PUBLIC PAGES (SEO-indexed)      INTERNAL PORTAL (auth required)   │
│  ├─ index.html                    ├─ interno.html (team home)      │
│  ├─ blog.html + /blog/[slug]      ├─ bitacora-contactos.html       │
│  ├─ nosotros.html (team)          ├─ bitacora.html (construction)  │
│  ├─ contratistas.html             ├─ wiki.html (searchable)         │
│  ├─ aplica.html (3 programs)      ├─ captura.html + captura-campo  │
│  ├─ ayuda.html                    ├─ seguimiento.html               │
│  └─ empleos.html                  ├─ visita.html (inspections)      │
│                                   ├─ analisis.html (deal analyzer) │
│                                   ├─ proyectos.html                 │
│                                   └─ admin/ (CMS: blog + team)      │
└────────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌────────────────────────────────────────────────────────────────────┐
│                  LAYER 2: NETLIFY FUNCTIONS                         │
│              (Invisible API proxy — hides API keys)                 │
├────────────────────────────────────────────────────────────────────┤
│  /.netlify/functions/bitacora     → LUMAVI Operations base         │
│  /.netlify/functions/contactos    → LUMAVI Contactos base          │
│  /.netlify/functions/wiki         → LUMAVI Knowledge Base          │
└────────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌────────────────────────────────────────────────────────────────────┐
│                  LAYER 3: AIRTABLE (SaaS Database)                  │
│                  (Single source of truth for operations)            │
├────────────────────────────────────────────────────────────────────┤
│  📊 LUMAVI Operations            📚 LUMAVI Knowledge Base           │
│  ├─ Projects (12 fields)         └─ Wiki Articles (10 fields)       │
│  └─ Bitácora Entries (11 fields)                                    │
│                                                                     │
│  ☎️ LUMAVI Contactos            🎨 LUMAVI Content Engine            │
│  └─ Bitácora de Contactos       └─ Marketing content                │
│     (14 fields — routing,          (existing base)                 │
│      escalation, callbacks)                                         │
└────────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌────────────────────────────────────────────────────────────────────┐
│                    ATTACHMENTS & STATIC BUILD                       │
│  Airtable Content API  ◀── Photos + voice notes (permanent)         │
│  GitHub markdown       ──▶ build.js  ──▶ posts.json + team.json    │
│                                       ──▶ /blog/[slug].html (SEO)   │
│                                       ──▶ sitemap.xml               │
│  Formspree             ◀── Public forms (aplica, ayuda, empleos)    │
└────────────────────────────────────────────────────────────────────┘
```

---

## 🚀 Key Features

| Feature | What It Does |
|---|---|
| 📱 **PWA** | Installs to phone home screen. Works offline (critical in rural PR). Camera + GPS access. |
| 🔍 **SEO-Optimized** | Each blog post gets its own URL, JSON-LD schema, Open Graph tags, sitemap.xml, canonical URLs |
| ☎️ **Call Center** | Full customer support ticketing — priority, routing, escalation, callback tracking |
| 🔨 **Construction Log** | Daily field log with 8 categories, photos, voice notes, GPS per entry |
| 📚 **Searchable Wiki** | Real-time filter across all articles, category sidebar, inline markdown editing |
| 📍 **Field Capture** | Team captures leads on-site with GPS auto-fill, camera, and offline queue |
| 🎤 **Visit Mode** | 10-zone property inspections with star ratings, multi-zone photos, voice notes |
| 📊 **Deal Analyzer** | 9 investment strategies, custom LUMAVI parameters, instant verdict |
| 🔐 **6 Role Hierarchy** | Admin / Analyst / Ops Manager / Editor / Support / Temp via Netlify Identity |
| 📝 **CMS-Powered** | Non-technical team members publish blog posts and team profiles without touching code |
| 🔄 **Offline-First** | Forms queue locally when no signal, auto-sync when reconnected |
| 🌐 **Bilingual-Ready** | Built in Spanish, structured to support English translations |
| 📎 **Permanent Attachments** | Photos + voice notes stored in Airtable (never lost, unlike localStorage) |
| 💬 **WhatsApp Integration** | One-click WhatsApp for contractor applications and consultations |
| 📈 **Analytics** | Google Analytics + custom event tracking across all flows |

---

## 📊 By the Numbers

- **31** HTML pages (public + internal)
- **3** Netlify Functions (serverless proxies to Airtable)
- **3** dedicated Airtable databases (Operations, Knowledge Base, Contactos)
- **37** fields across the operational database
- **8** categories in the construction log
- **10** call types in the customer support system
- **9** investment strategies in the deal analyzer
- **10** inspection zones in visit mode
- **6** user role hierarchies with granular permissions
- **6** social media platforms integrated
- **1** mission: restoring homes, restoring communities

---

## 🎯 What Makes This Different

Most real estate companies have a website. LUMAVI has a **complete operating system**:

- **Built as a SaaS platform** — team logs into a familiar-looking website, but behind the scenes runs on a real relational database (Airtable) with proper attachments, comments, revision history
- **Built for the field, not just the desk** — half the platform runs from a phone with camera + GPS + voice recording + offline sync
- **Built for non-technical teams** — customer support person logs calls in 30 seconds, ops manager documents construction in 30 seconds, editor publishes blog posts without touching code
- **Built for Puerto Rico specifically** — bilingual considerations, spotty internet (offline-first), SURI compliance considerations, herederos + sucesiones workflows
- **Built with dignity in mind** — every form, every page, treats clients and contractors like the experts they are

The team never sees Airtable. They see LUMAVI's branded pages. But everything they do is stored in a real database, forever, searchable, with photos and voice notes as permanent attachments.

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
- **Contractor / craftsperson?** → [Join our network](https://lumavipr.com/contratistas.html) ⭐ *Actively recruiting*
- **Looking for a job?** → [See openings](https://lumavipr.com/empleos.html)
- **Need help understanding your options?** → [Ask anything (Consultas desde $25)](https://lumavipr.com/ayuda.html)

---

## ⚖️ License & Credits

© 2025-2026 **LUMAVI Management Inc.** All rights reserved.

This codebase is the proprietary intellectual property of LUMAVI Management Inc.

Developed with assistance from **[Claude AI by Anthropic](https://anthropic.com)** — a productive collaboration between human vision and AI capability, building a real operational platform from scratch.

---

<div align="center">

**Restaurando hogares. Restaurando comunidades.**
*One property at a time.*

🇵🇷 Made with care in San Juan, Puerto Rico 🇵🇷

</div>
