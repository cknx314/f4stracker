Customer Tracker (PWA) — Overview

A lightweight, installable web app for tracking customers, payments, pledges, and follow-ups — with no server and no sign-in. Everything runs in the browser, works offline, and exports clean PDF/CSV/JSON when you need to share or back up.

What it does
- Keeps a customer list with company/contact, phone, email, amount, date, status (Paid/Pledged/Invoiced), notes, and next contact date.
- Filters by status and date range (All/This Month/Last Month/YTD), plus search and sorting.
- Shows a goal and animated progress ring with a “Goal Reached!” badge.
- Exports:
  • Single Customer PDF (includes notes)
  • All Customers PDF (respects search/status/date filters and sort)
  • CSV export (also respects filters/sort)
  • JSON backup/restore
- Lets you upload a logo once; it appears centered at the top of every PDF.
- Has an undo delete toast, duplicate detection, and demo data toggle.
- Theme toggle (light/dark).

Why it’s different
- Private by default: data stays on the device (IndexedDB/localStorage). No backend.
- Offline-first: install to Home Screen (PWA) and use without internet.
- Zero setup: drop the files on static hosting; no databases or APIs.

How it stores data
- Primary storage: IndexedDB (with a migration from localStorage for durability).
- JSON backup/restore for moving data between browsers/devices.
- No third-party services, analytics, or tracking.

PDFs & CSVs
- Single customer PDF for one-pagers (details + notes).
- All Customers PDF and CSV exports match your current filters and sorting, so reports reflect exactly what you’re viewing.
- Logo: upload once in Settings → Set PDF Logo (stored locally) for a consistent, branded header.

PWA & updates
- Installable on iOS/Android/Desktop (Add to Home Screen).
- Service worker caches core files and serves an offline page gracefully.
- Built-in update banner prompts a reload when a new version is published.
- Maskable icon included for better Android home-screen appearance.

Tech highlights
- Plain HTML + JS with Tailwind (CDN).
- jsPDF for PDF generation.
- Service Worker + Web App Manifest for PWA behavior.
- Icons: icon-192.png, icon-512.png, icon-512-maskable.png.

Intended use
Nonprofits, clubs, small teams, and campaigns that need a simple, private tracker for pledges/payments and follow-ups — without standing up a backend.

Limitations
- Single-user per browser; no automatic cloud sync (use JSON export/import to move data).
- Public hosting (e.g., GitHub Pages) serves the app publicly, but your data remains local to each user’s device.

Questions or tweaks (extra fields, branding colors, alternate exports)? Say the word and I’ll tailor it.
