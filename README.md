# 🎭 DigitalTix – Theatre Booking Platform

> A modern, full-featured theatre ticket booking platform built for the digital age.  
> Inspired by the scheduling excellence of **Setmore** and the frictionless booking UX of **Calendly**.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Issues](https://img.shields.io/github/issues/DigitalTix/theatre-booking-platform)](https://github.com/DigitalTix/theatre-booking-platform/issues)
[![Project Board](https://img.shields.io/badge/Project-Board-blue)](https://github.com/orgs/DigitalTix/projects/1)

---

## 🌟 Vision

DigitalTix aims to be the go-to platform for discovering, booking, and attending theatre performances — offering a seamless experience from browsing shows to scanning your QR ticket at the door.

---

## 🗺️ Epics Overview

| # | Epic | Priority | Sprint |
|---|------|----------|--------|
| 1 | [User Management & Authentication](#) | 🔴 Critical | Sprint 1 |
| 2 | [Venue & Theatre Management](#) | 🔴 Critical | Sprint 2 |
| 3 | [Show & Event Management](#) | 🔴 Critical | Sprint 2 |
| 4 | [Seat Selection & Reservation Engine](#) | 🔴 Critical | Sprint 3 |
| 5 | [Booking & Checkout Flow](#) | 🔴 Critical | Sprint 3 |
| 6 | [Payment Processing & Financial Management](#) | 🔴 Critical | Sprint 4 |
| 7 | [Digital Tickets & QR Code System](#) | 🟠 High | Sprint 4 |
| 8 | [Notifications & Reminders System](#) | 🟠 High | Sprint 5 |
| 9 | [Customer Portal & Self-Service](#) | 🟠 High | Sprint 5 |
| 10 | [Admin Panel & Operations Dashboard](#) | 🟠 High | Sprint 6 |
| 11 | [Search, Discovery & Recommendations](#) | 🟠 High | Sprint 7 |
| 12 | [Analytics & Business Insights](#) | 🟡 Medium | Sprint 8 |
| 13 | [Public API & Third-Party Integrations](#) | 🟡 Medium | Sprint 8 |
| 14 | [Infrastructure, DevOps & CI/CD](#) | 🟠 High | Sprint 1+ |
| 15 | [Accessibility, Mobile & Performance](#) | 🟡 Medium | Sprint 8 |

---

## 🏗️ Architecture Overview

```
┌─────────────────────────────────────────────┐
│            Clients (Web + Mobile)           │
└─────────────────┬───────────────────────────┘
                  │
┌─────────────────▼───────────────────────────┐
│                API Gateway                  │
└──┬──────────┬──────────┬────────────────────┘
   │          │          │
┌──▼──┐  ┌───▼───┐  ┌───▼──────────┐
│Auth │  │ Show  │  │   Booking &  │
│Svc  │  │ & Venue│  │  Payment Svc │
└─────┘  └───────┘  └──────────────┘
   │          │          │
┌──▼──────────▼──────────▼──────────┐
│         PostgreSQL + Redis         │
└───────────────────────────────────┘
   │                    │
┌──▼──────────┐  ┌──────▼────────┐
│ Notification │  │  Queue Worker │
│  Service     │  │ (Tickets, PDF)│
└─────────────┘  └───────────────┘
```

---

## 🎯 Core Features

### For Customers
- 🔍 **Discover** shows by genre, date, city, or mood
- 🗺️ **Interactive seat maps** with real-time availability
- 🛒 **Seamless checkout** in 4 steps or less
- 💳 **Multiple payment methods** (card, UPI, wallets)
- 📱 **Digital e-tickets** with QR codes
- 🍎 **Apple & Google Wallet** integration
- 🔔 **Smart reminders** before your show
- ⭐ **Reviews and ratings** post-show

### For Venue Admins
- 🏛️ **Manage venues**, halls, and seating layouts
- 🎭 **Schedule shows** with rich content and media
- 📊 **Real-time analytics** — occupancy, revenue, trends
- 🎟️ **QR check-in** for venue staff
- 📣 **Bulk notifications** to attendees

### For Platform Admins
- 👥 **Full user management** with role-based access
- 💰 **Financial oversight** — transactions, refunds, reports
- 🏷️ **Promo code management**
- 🔍 **Audit logs** for all sensitive actions
- ⚙️ **System configuration** and settings

---

## 🛠️ Suggested Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Next.js / React, TailwindCSS |
| Backend | Node.js / Express or NestJS |
| Database | PostgreSQL, Redis |
| Queue | BullMQ |
| Payments | Stripe |
| Email | SendGrid / Resend |
| SMS | Twilio |
| Storage | AWS S3 / Cloudflare R2 |
| Auth | JWT + OAuth2 |
| CI/CD | GitHub Actions |
| Hosting | AWS / GCP / Vercel |

---

## 📋 Project Board

👉 [View the Project Board](https://github.com/orgs/DigitalTix/projects/1)

---

## 🏃 Sprint Structure

| Sprint | Focus | Key Deliverables |
|--------|-------|-----------------|
| Sprint 1 | Foundation | Auth, roles, CI/CD, project setup |
| Sprint 2 | Content | Venue & show management |
| Sprint 3 | Core Booking | Seat map, reservation, checkout |
| Sprint 4 | Monetisation | Payments, e-tickets, QR codes |
| Sprint 5 | Engagement | Notifications, customer portal |
| Sprint 6 | Operations | Admin panel, reporting |
| Sprint 7 | Discovery | Search, filters, recommendations |
| Sprint 8 | Polish | Analytics, accessibility, performance |

---

## 🏷️ Labels Guide

| Label | Description |
|-------|-------------|
| `epic` | Parent feature initiative |
| `feature` | New functionality |
| `bug` | Defect to fix |
| `tech-debt` | Refactor or improvement |
| `priority: critical` | Blocks release |
| `priority: high` | Important for next sprint |
| `priority: medium` | Normal priority |
| `priority: low` | Future consideration |
| `area: frontend` | UI/UX work |
| `area: backend` | Server and API |
| `area: payments` | Payment processing |
| `needs-design` | Requires UX/UI design first |

---

## 🤝 Contributing

This repository is managed by the DigitalTix product team. Issues are created by the Product Owner and picked up during sprint planning.

---

## 📄 License

MIT © DigitalTix

