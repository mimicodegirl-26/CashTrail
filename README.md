<div align="center">
  <img src="https://raw.githubusercontent.com/mimicodegirl-26/CashTrail/main/public/cashtrails-logo.svg" width="120" alt="CashTrail Logo" />
  <h1>💰 CashTrail</h1>
  <p><strong>Next-Generation Expense Tracking • Cinematic Glassmorphism UI • Real-Time Financial Intelligence</strong></p>

  📦 **Production Ready Architecture** • ⚡ **Powered by Vite + React** • 🔒 **Fortified by Firebase**

  ---

  [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
  [![React](https://img.shields.io/badge/React-18.3-61DAFB?logo=react&logoColor=white)](https://reactjs.org/)
  [![TypeScript](https://img.shields.io/badge/TypeScript-5.6-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
  [![Vite](https://img.shields.io/badge/Vite-5.4-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
  [![Firebase](https://img.shields.io/badge/Firebase-10.x-FFCA28?logo=firebase&logoColor=white)](https://firebase.google.com/)
</div>

---

## 🎯 The Vision Behind CashTrail

Most expense trackers are digital spreadsheets disguised as apps—dry, clunky, and exhausting to use. **CashTrail** reimagines personal finance by combining a **premium cyber-sapphire glassmorphism UI** with a lightning-fast data layer. 

By blending real-time Cloud Firestore synchronization, custom analytical visualizations, and smart client-side security architecture, CashTrail converts mundane ledger tracking into an immersive, fluid desktop experience.

---

## ✨ Core Pillars & Feature Suite

### 📊 1. Visual Analytics Engine (Multi-Chart Dashboard)
Transform raw financial streams into visual signals right inside `Dashboard.tsx`:
* **🍰 Proportional Pie Charts:** See your current financial footprint split cleanly across customizable categories (e.g., Food, Travel, Utilities, Lifestyle).
* **📈 Trend Line Charts:** Monitor your savings velocity over time, exposing spending patterns before they become habits.
* **📊 Income vs. Expense Bars:** Side-by-side behavioral blocks displaying structural net balance ratios to keep you in the green.

### ⏱️ 2. Advanced Temporal Matrix & Search
* **📅 Date-Wise Logging:** File transaction records down to the exact millisecond using calendar-mapped input parameters.
* **🔍 High-Speed Querying:** Powered by custom logic in `filterStrategies.ts`, query histories smoothly by:
  * **Daily Scope:** Isolate statements from any single calendar day or window.
  * **Monthly Aggregates:** View macro spending sums grouped by automated billing periods.
  * **Yearly Overviews:** Synthesize global asset movements across multi-year horizons.

### 🚨 3. Intelligent Budget Guardrails
* **Custom Category Thresholds:** Set definitive cost ceilings across individual categories or global monthly metrics.
* **Real-Time Calculation:** Run validation checks through `transactionLogic.ts` the moment a transaction is typed.
* **Instant Overspend Alerts:** Crossing your budget triggers the `NotificationFacade` layer immediately, keeping your impulses in check.

### 🔒 4. Bulletproof Onboarding & Security
* **📋 Left-Aligned Serial Ergonomics:** Ditches confusing grid structures for a clean, stacked single-column flow (`RegisterPage.tsx`) tailored for natural scanning.
* **🆔 Unique Username Locks:** Runs sub-second validation queries against Cloud Firestore collections to prevent duplicate profiles during registration.
* **🛡️ Structural Password Guards:** Blocks weak sign-ups using strict regex validation (requires 8+ characters and a flexible mix of uppercase, lowercase, or special symbols).
* **👁️ Micro-Scaling Toggles:** Absolute-positioned native action triggers designed with zero-artifact transparent styling to peek at or hide text inputs cleanly.

### 📥 5. Enterprise Data Portability
* **CSV Bulk Data Processing:** Seamless data ingestion pipeline (`CSVImport.tsx`) allowing you to migrate offline sheets straight into your cloud dashboard without losing your history.

---

## 📁 Inside the Repository

CashTrail relies on a clean, decoupled folder structure that isolates styles, business logic, visual components, and test files:

```text
project/
├── public/
│   └── icons/                 # Interactive interface iconography assets
├── src/
│   ├── components/            # Reusable functional UI components
│   │   ├── CSVImport.tsx      # Batch file parser and ingestion module
│   │   ├── NotificationFacade.tsx # Abstracted high-performance custom toast layers
│   │   ├── ProtectedRoute.tsx # Route fortification & session validation guard
│   │   ├── SummaryCard.tsx    # Live telemetry financial metrics block
│   │   ├── TransactionForm.test.tsx
│   │   ├── TransactionForm.tsx# Real-time ledger entry component
│   │   └── TransactionList.tsx# Scrollable high-density data grid
│   ├── pages/                 # Full-viewport layout orchestrators
│   │   ├── Dashboard.tsx      # Multi-chart financial engine station
│   │   ├── HomePage.tsx       # Landing page presentation node
│   │   ├── LoginPage.tsx      # Authentication interface portal
│   │   ├── RegisterPage.tsx   # Glassmorphic registration wizard
│   │   └── ResetPassword.tsx  # Secure account validation retrieval station
│   ├── styles/                # Clean 1:1 mapped CSS layout sheets
│   │   ├── Dashboard.css
│   │   ├── HomePage.css
│   │   ├── LoginPage.css
│   │   ├── RegisterPage.css
│   │   └── ResetPassword.css
│   ├── utils/                 # Algorithmic state evaluation engines
│   │   ├── filterStrategies.test.ts
│   │   ├── filterStrategies.ts # High-speed temporal search matrices
│   │   ├── transactionLogic.test.ts
│   │   └── transactionLogic.ts # Financial ledger execution engines
│   ├── App.css
│   ├── App.tsx                # Master app routing & configuration hub
│   ├── firebase.ts            # Production core cloud credential export
│   ├── index.css              # Global baseline variables & font tracking
│   ├── main.tsx               # DOM injection bootstrapper
│   └── types.ts               # Centralized global TypeScript interfaces
├── tsconfig.json              # Strict compiler instruction rules
└── vite.config.ts             # Performance automation build system script

```

---

## 🛠️ The Tech Stack

| Tool / Library | Purpose | Highlight |
| --- | --- | --- |
| **React 18.3** | Component UI Core | Declared with lightweight functional hooks and fast state cycles. |
| **TypeScript 5.6** | Static Integrity | Compile-time validation preventing application runtime crashes. |
| **Vite 5.4** | Bundling & Execution | Instantaneous Hot Module Replacement (HMR) for responsive dev loops. |
| **Cloud Firestore** | Storage Architecture | Scalable, real-time database management for profile parameters and transactional logs. |
| **Firebase Auth** | Session Defenses | Hardened identity checks processing secure login tokens. |

---

## 🎨 Interface & Animation Architecture

### 🌌 Background Ambience Shifting

The UI framework uses hardware-accelerated GPU layers to move dual pseudo-elements smoothly behind glass components without adding processing overhead:

```css
@keyframes float {
  from { transform: translate(0, 0); }
  to { transform: translate(35px, 30px); }
}

```

### 📋 Left-Aligned Serial Input

By declaring `.input-box { align-items: flex-start; }`, CashTrail forces clear tracking structures that maintain a clean visual look from top to bottom.

---

## 🔒 Security Lifecycle & Cloud Policy

### Registration Ingestion Flow

```
[ User Form Action ]
         │
         ▼
[ Password Structure Check ] ──► (Denies vulnerable profiles instantly)
         │
         ▼
[ Firestore Index Scan ]     ──► (Queries database to check for username conflicts)
         │
         ▼
[ Firebase Auth Engine ]     ──► (Creates secure account instance with distinct UID)
         │
         ▼
[ Doc Entry Serialization ]  ──► (Saves user payload metadata to path /users/{uid})

```

### 🛡️ Production Firestore Rules Architecture

Ensure your cloud environment sets the following baseline access policies to secure your database routes effectively:

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /users/{userId} {
      allow read, write: if request.auth != null && request.auth.uid == userId;
    }
  }
}

```

---

## 🚀 Local Deployment Lifecycle

### Prerequisites

* **Node.js** Environment v18.0.0+ Installed
* Package systems like **npm** or **yarn**

### Quick Installation

1. **Clone and Navigate:**
```bash
git clone [https://github.com/mimicodegirl-26/CashTrail.git](https://github.com/mimicodegirl-26/CashTrail.git)
cd CashTrail

```


2. **Sync Dependencies:**
```bash
npm install

```


3. **Configure Environment Secrets (`src/firebase.ts`):**
```typescript
import { initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";
import { getFirestore } from "firebase/firestore";

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_AUTH_DOMAIN",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_STORAGE_BUCKET",
  messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
  appId: "YOUR_APP_ID"
};

const app = initializeApp(firebaseConfig);
export const auth = getAuth(app);
export const db = getFirestore(app);

```


4. **Boot Up Development Server:**
```bash
npm run dev

```


*Your server will go live instantaneously at `http://localhost:5173`!*
5. **Run Logic Test Suites:**
```bash
npm run test

```



---

📊 *Tracking data shouldn't look stale. Take the clean path with CashTrail.*

```

```
