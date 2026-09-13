# CAMPUS 360 — Progressive Web App (PWA)

**CAMPUS 360** is a modern, mobile-responsive single-page Progressive Web App designed with a dark glassmorphism aesthetic. It features three integrated portals: a Student Grievance Desk, a Parent Live Presence Verification Tracker, and a PIN-protected Administrative Management Console with full CRUD operations (including 🗑️ delete buttons) and real-time cross-tab / cross-device synchronization.

---

## Architecture Highlights

- **Single-File Architecture (`index.html`)**: Contains all HTML5 markup, embedded modern dark glassmorphism CSS, inline SVG icons, JavaScript business logic, embedded Web App Manifest (data URI), and inline Service Worker blob.
- **Zero Configuration**: No Node.js, Webpack, or external CDN dependencies needed. Open and run instantly offline or online.
- **GitHub Pages Ready**: 100% immune to multi-page 404 routing errors or broken relative asset links.

---

## Portals & Features

### 1. 🎓 Student Portal (Home & Grievance Desk)
- **Grievance Submission Form**:
  - Roll Number input with auto-fill of student details from roster.
  - Full Name, Category selector (Hostel, Academic, Safety, Mess, Infrastructure, Medical, Admin).
  - Urgency level (`Standard`, `Urgent`, `Critical`).
  - Detailed concern description.
  - Automatic ticket generation (e.g. `GRV-2026-XXXX`).
- **Grievance Tracker**:
  - Live status tracking (`🟡 Pending`, `🔵 In Progress`, `🟢 Resolved`).
  - View administrator resolution notes and timestamps.
  - Search filter by Roll Number, Name, or Ticket ID.

### 2. 👨‍👩‍👧 Parent Portal (Live Presence & Safety Tracker)
- **Live Presence Search**:
  - Search by Student Roll Number (with quick demo chips e.g. `CS2026-001`, `EC2026-014`, `ME2026-007`).
- **Visual Presence Card**:
  - `🟢 PRESENT (Inside Campus)` — displays campus zone, RFID gate check-in time, and hostel info.
  - `🔴 ABSENT (Outside Campus)` — displays departure gate and outpass authorization info.
  - Attendance percentage and direct buttons to call Campus Security Hotline and Hostel Warden.

### 3. 🛡️ Admin Dashboard (PIN-Protected Console)
- **Security Gatekeeper**: Protected by passcode (`admin123` with a 1-click **⚡ Demo Quick Unlock** button).
- **Grievance Management**: Filter by category/status, search, update status, save remarks, and a prominent **🗑️ Delete** button on each complaint.
- **Student Attendance Management**: Real-time presence counters, **Add / Register Student** form, **✏️ Edit Student** modal, **🔄 1-Click Status Toggle** button, and **🗑️ Delete Student Record** option with safety confirmations.
- **Cloud & Cross-Device Sync**:
  - Automatic `localStorage` persistence.
  - `BroadcastChannel` real-time sync across multiple open browser tabs.
  - **Export Backup JSON** and **Import Backup JSON** tools to transfer live data between phones and laptops.

---

## Deployment & Usage

### 1. Local Run
Double-click `index.html` or open in any web browser (Chrome, Edge, Safari, Firefox).

### 2. Deploy to GitHub Pages
1. Create a GitHub repository (e.g. `campus-360`).
2. Upload `index.html` to the repository root.
3. In GitHub, go to **Settings > Pages**.
4. Set source branch to `main` (or `master`) and directory to `/ (root)`.
5. Click **Save** — your site will be live immediately.
