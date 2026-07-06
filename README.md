# 🍽️ RestaurantOS

> A full-stack SaaS platform replacing traditional POS systems for restaurants — built with a zero-hardware philosophy.

No tablets. No cash registers. Just a QR code on the table.

---

## 🚀 Overview

RestaurantOS is an AI-powered restaurant management platform that enables customers to order directly from their phone by scanning a QR code on their table — no app download required. Restaurant owners get a full dashboard to manage their menu, track orders in real time, and view analytics.

---

## ✨ Features

### 👥 Customer Experience
- 📱 Scan QR code on the table — no app required
- 🌍 Multi-language support: **Arabic**, **French**, **English** with RTL support
- 🍽️ Browse menu with photos, descriptions, and prep times
- 🤖 **Zivo** — AI-powered voice waiter (speaks & listens in your language)
- 🛒 Add to cart, review order, and confirm with legal disclaimer
- ✅ Session-based security — each QR scan generates a unique 90-minute token
- 🎁 Loyalty points system for returning customers

### 🏪 Owner Dashboard
- 🔐 Secure login with JWT authentication
- 📋 Full menu management — categories, items, prices, availability
- 🖼️ Photo upload for each menu item
- 📦 Real-time order tracking
- 📊 Analytics — sales, top dishes, peak hours, customer insights
- 📱 Tables & QR code management

### 🤖 AI Integration (Zivo)
- Multilingual conversation memory per customer
- Personalized dish recommendations based on order history
- Voice input and text-to-speech output
- Strict restaurant-only context — redirects off-topic questions
- Powered by **Groq AI**

### 🔐 Security
- QR session tokens with 90-minute expiry
- Each scan generates a unique token — prevents remote attacks
- Legal confirmation checkbox before every order
- JWT Bearer authentication for owner dashboard
- IP logging per session

---

## 🏗️ Architecture

```
RestaurantOS/
├── RestaurantOS.API/           ← ASP.NET Core 9 REST API
├── RestaurantOS.Core/          ← Business logic & entities
├── RestaurantOS.Infrastructure/ ← Database & EF Core
└── RestaurantOS.Frontend/      ← React 19 + Vite PWA
```

**Clean Architecture** with separation of concerns across three backend layers.

---

## ⚙️ Tech Stack

| Layer | Technology |
|---|---|
| **Backend** | ASP.NET Core 9, C#, Clean Architecture |
| **Database** | SQL Server, Entity Framework Core |
| **Frontend** | React 19, Vite, Tailwind CSS v4 |
| **Real-time** | SignalR (Kitchen Display System) |
| **AI** | Groq API (Llama / Qwen models) |
| **Auth** | JWT Bearer tokens, BCrypt |
| **Storage** | Local file storage (Azure Blob planned) |

---

## 📱 Customer Flow

```
Scan QR Code
      ↓
Select Language (AR / FR / EN)
      ↓
Enter Phone + Name (optional — for AI personalization)
      ↓
Browse Menu + Chat with Zivo AI Waiter
      ↓
Add to Cart → Checkout
      ↓
Legal Confirmation Checkbox
      ↓
Order Sent to Kitchen (real-time)
```

---

## 🗺️ Roadmap

- [x] Customer ordering flow (QR → menu → checkout)
- [x] Multi-language support (AR/FR/EN)
- [x] AI waiter — Zivo (text + voice)
- [x] Owner dashboard — menu management
- [x] JWT authentication
- [x] Session-based QR security
- [ ] Kitchen Display System (KDS) — real-time
- [ ] Owner analytics dashboard
- [ ] QR code generator for tables
- [ ] Subscription tiers (Starter / Pro / Business)
- [ ] Super-admin panel
- [ ] Azure cloud deployment
- [ ] Google Cloud TTS for natural AI voice
- [ ] WhatsApp daily reports

---

## 👨‍💻 Author

**Moustapha Hammoud**
Senior Software Developer · MSc Computer Science candidate (USJ)
🇱🇧 Beirut, Lebanon

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/moustapha-hammoud)
[![GitHub](https://img.shields.io/badge/GitHub-MoustaphaHammoud--Dev-black)](https://github.com/MoustaphaHammoud-Dev)

---

## 📄 License

This project is proprietary and not open for redistribution.
© 2026 Moustapha Hammoud. All rights reserved.

---

> *"The smartest way to run your restaurant."*
