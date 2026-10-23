# 🚚 LogTrack - Logistics & Fleet Management SaaS (Case Study)

> **Note:** The source code for this project is private due to proprietary business logic and client NDAs. This repository serves as a technical case study highlighting the software architecture, database design, and problem-solving methodologies used to build the platform.

## 📖 Overview
LogTrack is a robust, high-performance web-based Logistics Enterprise Resource Planning (ERP) system. Designed as a Multi-tenant SaaS, it optimizes towing operations, vehicle transport, and associated logistical services. The platform controls service providers, issues service orders (OS), calculates dynamic routes, manages financials, evaluates quality (SLA scoring), and issues consolidated corporate reports.

---

*<img width="1896" height="951" alt="Dashlog" src="https://github.com/user-attachments/assets/74999f2b-a95c-4829-9e96-4f5ae220b9a8" />
*

---

## 🚀 Key Features
* **Advanced Dispatch & Routing:** Visual engine running via Leaflet Maps acting as a Control Tower. It calculates projected origins and destinations using latitude/longitude meshes powered by the Haversine Formula.
* **Intelligent Credit & Financial Backoffice:** Generates native Excel (XLSX) spreadsheets for BPO macros and landscape-oriented Analytical PDFs (via jsPDF) that consolidate cross-table relational data.
* **Predictive SLA Scoring:** Consolidates and ranks the network of service providers based on volume, average deadlines, and reported damage levels.
* **360° Provider CRM:** Comprehensive management of transport vehicles, contractual limits, and real-time status with built-in WhatsApp dialer integration.

## 🛠️ Tech Stack & Architecture
Built with a modern, Serverless-ready approach focusing on edge performance and scalable backend logic.

### Frontend
* **Core:** React 19, TypeScript, Vite
* **Routing:** React Router v7
* **UI/UX:** Tailwind CSS v4, Lucide React (Pragmatic, Desktop-like UI optimized for high data density)
* **Data Visualization:** Recharts, Leaflet & React-Leaflet

### Backend & Database (Supabase)
* **Database:** PostgreSQL (Relational)
* **Authentication:** Supabase Auth (RBAC - Role Based Access Control)
* **Security:** Strict Multi-Tenant Row Level Security (RLS) policies directly on the database level.
* **Admin API:** Custom REST Proxy for Super Admin bypass and background operations.

## 🔐 Multi-Tenant Architecture & Governance
The system implements a rigid 4-tier hierarchy (Super Admin, Owner, Manager, Operator). The Postgres RLS architecture prevents cross-tenant data leakage, ensuring that each enterprise branch views 100% isolated operational volume.

