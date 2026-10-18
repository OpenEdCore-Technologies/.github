
<p align="center">
  <img width="1600" height="900" alt="opened-readme-banner-1600x900" src="https://github.com/user-attachments/assets/cd900ef2-8c01-4be7-ba6f-b5a0e3769bb4" />
</p>

<p align="center">
  <strong>The Full-Stack Next-Generation School & College Management Ecosystem</strong><br/>
  <sub>Powered by Vapor Swift Server & Mobile-First Multiplatform Tech</sub>
</p>

<p align="center">
  <a href="https://openedschool.com"><img src="https://img.shields.io/badge/Production-openedschool.com-0284c7?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Production Portal" /></a>
  <a href="https://staging.openedschool.com"><img src="https://img.shields.io/badge/Staging-staging.openedschool.com-0d9488?style=for-the-badge&logo=render&logoColor=white" alt="Staging Preview" /></a>
  <a href="https://github.com/OpenEdCore-Technologies"><img src="https://img.shields.io/badge/Security-CodeQL_Verified-10b981?style=for-the-badge&logo=github&logoColor=white" alt="CodeQL Verified" /></a>
  <a href="https://github.com/OpenEdCore-Technologies"><img src="https://img.shields.io/badge/Architecture-Multi--Tenant_Cloud-8b5cf6?style=for-the-badge&logo=swift&logoColor=white" alt="Multi Tenant" /></a>
</p>

---

## 🏛️ Executive Summary & Value Proposition

**OpenEdCore** is an all-in-one, modern cloud operating platform engineered to replace fragmented legacy ERPs in modern educational institutions, K-12 school networks, and multi-campus universities.

Unlike obsolete 2000s-era monolithic school software, OpenEdCore delivers:
- **Unified Fullstack Ecosystem**: Seamless synchronization across High-Performance Swift Backends, React 19 Web Dashboards, and Native iOS / Android Mobile Apps.
- **Enterprise Multi-Tenancy**: Zero-leakage database isolation, tenant-specific routing (`X-Tenant-Slug`), and custom domain mapping for multi-school conglomerates.
- **Real-Time Campus Mobility**: Instant push notifications, digital student ID cards with secure QR validation, live attendance check-in, and interactive class timetable rosters.
- **Military-Grade Security**: Automated GitHub CodeQL static vulnerability scanning, OWASP-compliant access gates, and role-based cryptographic access control (Super Admin, Principal, Teacher, Student, Parent).

---

## 🚀 The Three Pillars of the Ecosystem

```mermaid
graph TD
    classDef client fill:#1e293b,stroke:#38bdf8,stroke-width:2px,color:#f8fafc;
    classDef backend fill:#1e293b,stroke:#a855f7,stroke-width:2px,color:#f8fafc;
    classDef data fill:#1e293b,stroke:#34d399,stroke-width:2px,color:#f8fafc;

    subgraph Clients["Presentation Layer"]
        Web["🖥️ Web Portal (opened-school-web)<br/>Next.js 16 • React 19 • Tailwind CSS"]:::client
        Mobile["📱 Mobile App (openedschool-mobile)<br/>SwiftUI • Skip Transpiled Kotlin/Compose"]:::client
    end

    subgraph Platform["Core Platform"]
        API["⚡ OpenEdCore Backend API<br/>Swift 6 • Vapor 4 • REST & GraphQL"]:::backend
        Auth["🔐 Identity & Access Gate<br/>JWT Authentication • RBAC • Multi-Tenant Router"]:::backend
    end

    subgraph Persistence["Storage & Infra"]
        DB[("🐘 PostgreSQL Multi-Tenant DB")]:::data
        Deploy["☁️ Render Cloud / Docker Containers"]:::data
    end

    Web -->|HTTPS / API Requests| API
    Mobile -->|HTTPS / API Requests| API
    API --> Auth
    Auth --> DB
    API --> Deploy
```

---

## 📦 Core Repositories

| Repository | Role & Stack | Key Features | CI/CD & Security |
| :--- | :--- | :--- | :--- |
| [**`OpenEdCore`**](https://github.com/OpenEdCore-Technologies/OpenEdCore) | **High-Concurrency Backend API**<br/>`Swift 6` • `Vapor 4` • `PostgreSQL` | Multi-tenant tenant resolution, academic scheduling, gate security, attendance verification | ![CI](https://img.shields.io/badge/Build-Passing-brightgreen?style=flat-square) ![CodeQL](https://img.shields.io/badge/CodeQL-Passing-blue?style=flat-square) |
| [**`opened-school-web`**](https://github.com/OpenEdCore-Technologies/opened-school-web) | **Administrative Web Portal**<br/>`Next.js 16` • `React 19` • `TypeScript` | Institutional analytics, admissions funnel, student rosters, real-time timetable matrix | ![CI](https://img.shields.io/badge/Build-Passing-brightgreen?style=flat-square) ![CodeQL](https://img.shields.io/badge/CodeQL-Passing-blue?style=flat-square) |
| [**`openedschool-mobile`**](https://github.com/OpenEdCore-Technologies/openedschool-mobile) | **Native iOS & Android Client**<br/>`SwiftUI` • `Skip Tools` • `Jetpack Compose` | Single Swift codebase transpiling to native Android Jetpack Compose, offline-first timetable | ![CI](https://img.shields.io/badge/Build-Passing-brightgreen?style=flat-square) ![CodeQL](https://img.shields.io/badge/CodeQL-Passing-blue?style=flat-square) |

---

## 🌟 Key Platform Capabilities

### 1. Multi-Tenant School Virtualization
- Complete logical isolation per school brand, academic branch, or university campus.
- Automated tenant resolution via subdomain (`greenwood.openedschool.com`), custom domains, or HTTP headers (`X-Tenant-Slug`).

### 2. Interactive Academic Scheduling & Timetables
- Drag-and-drop timetable generator preventing instructor double-booking and room collisions.
- Instant timetable synchronization to students' and teachers' mobile devices.

### 3. Smart Access Gate & Campus Security
- QR-code digital ID card rendering with cryptographic tamper verification.
- Real-time parent alerts and notifications when students enter or leave campus facilities.

### 4. Fully Automated CI/CD & Static Security Analysis
- Every code check-in is compiled, tested, and analyzed with **GitHub CodeQL** across Swift and TypeScript to eliminate vulnerabilities before production deployment.

---

## 📈 Roadmap & Commercial Milestones

- [x] Multi-tenant core data models & database migration infrastructure
- [x] Web Portal Admin & Principal admissions management dashboard
- [x] Cross-platform iOS & Android mobile application with Skip
- [x] Automated CodeQL Advanced Security Scanning across all tiers
- [ ] Enterprise Stripe / Razorpay tuition fee invoicing & auto-collection
- [ ] Real-time GPS bus transport tracking & geofencing integration
- [ ] White-label multi-campus custom branding provisioning for partner school networks

---

<p align="center">
  <sub>Built with precision for the future of education • © 2026 OpenEdCore Technologies</sub>
</p>
