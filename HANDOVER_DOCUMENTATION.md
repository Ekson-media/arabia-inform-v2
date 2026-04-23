# Project Handover Documentation: Arabia Inform v2

## 📅 Handover Date: April 12, 2026
## 🏷️ Version: 2.6 (Stable - Dual Recipient Email)

---

## 🔗 Online Resources

### 🌍 Live Deployment (Preview)
- **URL:** [https://Ekson-media.github.io/arabia-inform-v2/](https://Ekson-media.github.io/arabia-inform-v2/)
- **Note:** This is the current stable preview hosted via GitHub Pages.

### 💻 GitHub Source Code
- **Repository:** [https://github.com/Ekson-media/arabia-inform-v2](https://github.com/Ekson-media/arabia-inform-v2)
- **Branch:** `main`

### 📦 Production-Ready Download
- **v2.6 Release ZIP:** [Download ZIP](https://github.com/Ekson-media/arabia-inform-v2/archive/refs/tags/v2.6.zip)
- **Local Location:** `D:\Almotahida\arabia-inform-v2.6-Production-Ready.zip`

---

## 🏛️ Website Overview

**Arabia Inform v2** is a high-fidelity, premium website redesign for the world's most continuous archive of Arabic thought and media.

### Key Specifications:
- **Architecture:** 100% Static HTML/CSS/JS (Institutional Grade).
- **Design System:** Corporate Glassmorphism with a Deep Navy (#0F1E35), Teal (#2198B4), and Champagne Gold (#D7BE82) palette.
- **Responsiveness:** Managed via a 3-column CSS Grid system for headers and mobile-first media queries.
- **Multilingual:** Full Bi-directional (LTR/RTL) support for English and Arabic.

---

## 🚀 Recent Major Updates (v2.0)

1. **Unified Header System:**
   - Standardized to a fixed **64px height** with a clean **3-column layout** (`auto 1fr auto`).
   - Resolved all previous navigation overlap issues on tablets and mobile.
   - Fixed active menu underline centering logic.
2. **Standardized Premium Imagery:**
   - Replaced all stock/placeholder images with 13 custom-generated 3D Glassmorphism visualizations.
   - All assets now follow a unified lighting and color theme (Teal/Gold/Navy).
3. **Optimized CTA Button:**
   - Transformed the "Contact / Demo" link into a premium Teal pill-button with interactive hover effects.
4. **Cache Management:**
   - Implemented `?v=8.0` fingerprinting on global CSS files to ensure immediate updates across all user browsers.
5. **Arabic Restoration & CAPTCHA (v2.1):**
   - Restored corrupted Arabic content and encoding for Archive, Contact, and Impact pages.
   - Standardized "+" sign positioning across all Arabic metrics (moved to right side/start of numbers).
   - Enabled CAPTCHA security on both English and Arabic contact/demo forms via FormSubmit.co.
6. **Custom Local Box CAPTCHA (v2.5):**
   - Redesigned the checkbox to appear in a distinct, high-visibility white box.
   - Mimics the premium UI/UX of leading security providers (like Cloudflare Turnstile) without requiring any APIs.
   - Features a green circular checkmark and success message upon verification.
   - Optimized for dark-themed forms to ensure maximum visibility.
7. **Dual Recipient Configuration (v2.6):**
   - Configured form submission to send to multiple recipients.
   - Primary: `jan.diggs@arabiainform.com`
   - CC: `info@arabiainform.com`

---

## 📂 Directory Structure

- `/index.html`: Main entrance.
- `/ar/`: Arabic translation directory (RTL optimized).
- `/css/styles.css`: Core design system and layout.
- `/js/main.js`: Light interactions and language switching.
- `/images/`: All visual assets, including the new `/v2_` unified PNG collection.

---

## 🛠️ Deployment Instructions (for SE Team)

1. **Extraction:** Download/Extract the **v2.6 Production ZIP**.
2. **Server Root:** Upload all files (keeping structure intact) to the root directory of the production web server.
3. **No Build Step:** No `npm install` or compilation is required; the site is ready-to-serve.
4. **Verification:** Check the `Intelligence Platform` and `API Access` sections on the Products page to ensure the images render correctly.


---

## 📧 Contact Form & Email Configuration (Important for Migration)

The contact forms on both the English (`/contact.html`) and Arabic (`/ar/contact.html`) pages are currently powered by **FormSubmit.co**, which handles sending the emails securely without a backend.

**Current Dual-Recipient Setup:**
All submissions are sent to two addresses simultaneously:
1.  **Primary:** `jan.diggs@arabiainform.com`
2.  **CC (Carbon Copy):** `info@arabiainform.com`

### Steps Required When Managing or Changing Servers:

1.  **Server Migration (Domain Change):**
    If the website is moved to a new server/domain name (e.g., from `ekson-media.github.io` to `arabiainform.com`), the forms **must be activated on the new domain**. 
    *   **Action Required:** After deploying to the new server, submit a test request through the form. FormSubmit will automatically send an activation email to `jan.diggs@arabiainform.com`. The owner of that email *must* click "Confirm" in that email for the forms to work on the new server.

2.  **Redirect URLs (`_next` field):**
    The forms are currently hardcoded to redirect the user back to the correct thank-you/contact page upon submission.
    *   **Action Required:** If your production domain is *not* going to be `http://arabiainform.com`, you must update the hidden field `<input type="hidden" name="_next" value="...">` in both `contact.html` and `ar/contact.html` to match your actual live domain.

3.  **Changing the Receiving Email:**
    If you ever need to change who receives these requests:
    *   Change the `action` attribute on the `<form>` tag: `action="https://formsubmit.co/NEW_EMAIL@example.com"`.
    *   Change the CC field (optional): `<input type="hidden" name="_cc" value="ANOTHER_EMAIL@example.com">`.

---
*© 2026 Arabia Inform. Document generated for task completion and handover.*
