# 🚗 Vaahan Portal — RTO Vehicle Registration Management System

A fully client-side, single-page web application (SPA) simulating an Indian Government RTO (Regional Transport Office) vehicle registration and management portal. Built with pure HTML, CSS, and vanilla JavaScript — no frameworks or backend required.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Pages & Modules](#pages--modules)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Authentication](#authentication)
- [Data Persistence](#data-persistence)
- [UI & Design](#ui--design)
- [Folder Structure](#folder-structure)
- [Known Limitations](#known-limitations)
- [Support](#support)

---

## Overview

Vaahan Portal is a mock government-style web portal that replicates the core features of India's vehicle registration ecosystem. It allows citizens to register vehicles, apply for driving licences, manage challans (traffic fines), transfer ownership, and more — all within a single HTML file without any server or database.

---

## ✨ Features

### Public / Landing Page
- Hero section with portal stats and a call-to-action
- Services overview grid (Registration, Licence, Challan, Fitness, Insurance, NOC, etc.)
- Responsive navigation with Login and Register buttons
- Footer with quick links

### Authentication
- **User Registration** — First name, last name, email, mobile, state, date of birth, and password
- **Login** — Email/mobile + password with Enter-key support
- **Forgot Password** — Reset via registered email
- **Password Visibility Toggle** — Show/hide password using eye icon
- **Password Validation** — Minimum 8 characters with at least one number and one special character
- **Terms & Privacy Policy** checkbox agreement

### Dashboard
- Personalized welcome banner with user name
- KPI cards: Total Vehicles, Active Licences, Pending Challans, Applications
- Recent Activity feed
- Quick Action buttons
- Collapsible sidebar navigation

---

## 📄 Pages & Modules

| Module | Description |
|---|---|
| **Dashboard** | Overview with KPIs, activity, and quick actions |
| **Vehicle Registration** | Multi-step form to register new vehicles with owner & vehicle details |
| **My Vehicles** | Table view of all registered vehicles with status badges |
| **Driving Licence** | Apply for new DL or renewal; view existing licences |
| **Challans** | View, pay, and dispute traffic challans |
| **Fitness Certificate** | Apply for vehicle fitness certification |
| **Insurance** | View and manage vehicle insurance records |
| **NOC** | Apply for No Objection Certificate |
| **Ownership Transfer** | Transfer vehicle ownership between parties |
| **RC Status** | Track Registration Certificate status |
| **Reports** | Generate and view reports |
| **Notifications** | System and activity notifications |
| **Profile** | View and edit personal info; change password |
| **Settings** | Dark mode, font size, compact sidebar, notification preferences |
| **FAQ** | Expandable accordion FAQ section |
| **Support** | Contact/helpdesk information |

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 |
| Styling | Pure CSS3 (CSS Variables, Flexbox, Grid) |
| Scripting | Vanilla JavaScript (ES6+) |
| Fonts | Google Fonts — Rajdhani (headings), Noto Sans (body) |
| Storage | Browser `localStorage` (client-side state persistence) |
| Backend | None — fully static |

---

## 🚀 Getting Started

No installation or build step is needed.

```bash
# Simply open the file in any modern browser
open index.html
```

Or serve it locally:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (npx)
npx serve .
```

Then visit `http://localhost:8000` in your browser.

---

## 🔐 Authentication

All user data is stored in `localStorage` under a `vaahanState` key. Passwords are stored in plain text in local storage (this is a demo/mock application — **not suitable for production**).

**Demo credentials** — You can register a new account directly on the portal. No pre-seeded accounts are required.

---

## 💾 Data Persistence

The app uses a global `state` object that is serialized to `localStorage` on every significant action via a `saveState()` function. On page load, `loadState()` restores the previous session.

State includes:
- `users` — registered user accounts
- `currentUser` — currently logged-in user
- `vehicles` — registered vehicle records
- `challans` — challan/fine records
- `licences` — driving licence records
- `applications` — pending/approved applications

---

## 🎨 UI & Design

The UI follows a government portal aesthetic with a modern, clean design:

- **Color Palette** — Navy (`#0a2463`), Blue (`#1e4db7`), Sky (`#3a86ff`), Accent Gold (`#f7a928`)
- **Dark Mode** — Toggle available in Settings; overrides CSS variables dynamically
- **Responsive** — Fluid grids and media queries for tablet/mobile compatibility
- **Sidebar** — Collapsible with icon-only mode
- **Badges** — Color-coded status indicators (green = active, yellow = pending, red = expired/overdue)
- **Modals** — Animated overlay modals for login and signup
- **Fonts** — Rajdhani for all headings for a bold, official look

---

## 📁 Folder Structure

```
project/
└── index.html      # Entire application (HTML + CSS + JS in one file)
└── README.md       # This file
```

All CSS is embedded in a `<style>` block and all JavaScript in a `<script>` block within `index.html`.

---

## ⚠️ Known Limitations

- **No real backend** — All data lives in the browser's `localStorage` and is lost if the user clears browser data
- **Passwords are not hashed** — This is a prototype/demo only; do not use for real user data
- **No OTP/Aadhaar verification** — Fields for mobile and Aadhaar are present in forms but validation is simulated
- **Single device** — User data does not sync across devices or browsers
- **No real payment gateway** — Challan payment and fee submissions are simulated

---

## 📞 Support

For portal-related queries (as displayed in the app):

- **Toll-Free Helpline:** 1800-180-1222
- **SSL Encryption:** 256-bit (simulated)

---

## 📝 License

This project is a front-end demo/prototype intended for educational and UI demonstration purposes. It is not affiliated with the official Government of India Vaahan portal.
