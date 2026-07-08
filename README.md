# HRM Pulse Workspace Portal 🚀

HRM Pulse is a secure, enterprise-grade full-stack (MERN) entry/exit logging terminal. Designed to simulate a physical corporate entrance kiosk, the system utilizes strict state-machine validation, encrypted multi-department tracking, and real-time rolling metrics to monitor building occupancy while preventing proxy punching.

---

## 🏛️ System Architecture

The repository is divided into two distinct, decoupled environments:
* **`entry-exit-frontend`**: A fast, client-side UI built with React, Vite, and Tailwind CSS. Capable of cloud deployment (Vercel) to serve as a public website link for global client access.
* **`entry-exit-backend`**: A localized Node.js/Express server and MongoDB database engine that securely anchors all business logic, credentials, and movement logs locally on the host machine.

---

## ✨ Core Features

### 1. Anti-Proxy PIN Authentication
* Mandatory Secret PIN validation prompt dynamically rendered upon employee selection.
* Universal initial setup PIN (`1234`) for pre-seeded corporate rosters.
* Self-service "Change PIN" management console for individual employee access control.

### 2. State-Machine Entrance Validation
* **Strict Alternating Enforcements**: Employees currently flagged as `Out` can *only* trigger an Entry stamp. Employees currently `In` can *only* trigger an Exit stamp.
* Complete elimination of double-stamping, rapid-fire spamming, or multi-user proxy logs.

### 3. Chronological Side-by-Side Session Logs
* Automatically groups individual raw stamps into localized **"Movements"**.
* Renders an employee's Entry time and matching Exit time horizontally on the exact same row.
* Applies a live `Active Inside` indicator badge if an entry sequence is ongoing.

### 4. Time-Windowed Traffic Metrics
* Real-time analytical dropdown engine allowing managers to filter and compute completed traffic sessions over granular historical spans:
    * Last 5 Minutes
    * Last 10 Minutes
    * Last 1 Hour
    * Last 8 Hours

### 5. Master Administrative Command Console
* **Credential Auditor Grid**: Secure administrative space featuring a hover/click toggle to view plain-text employee PIN strings.
* **Full CRUD Staff Lifecycle**: Forms to instantly onboard new hires or offboard/purge old records from active collections.

---
