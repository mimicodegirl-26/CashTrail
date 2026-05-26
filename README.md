# 🪙 CashTrail — Smart Expense Tracker

Welcome to **CashTrail**, a beautiful, next-generation expense tracking web application. Built with **React, TypeScript, and Firebase**, CashTrail features a stunning dark-themed glassmorphism UI, fluid interactive animations, secure multi-attribute authentication, and instantaneous data syncing.

Take control of your financial journey through a seamless, cinematic user experience!

---

## ✨ Features at a Glance

* **🎬 Cinematic Glassmorphism UI:** Built using premium modern design philosophies with dynamic radial gradient floating backgrounds and glass-like components (`backdrop-filter`).
* **👤 Multi-Layer Unique Registration:** Fully optimized serial onboarding form tracking Full Name, Email, and dynamic **Unique User Name** checking via live database verification.
* **🔒 Strict Shield Passwords:** Smart client-side regex security rules that block weak passwords instantly coupled with a smooth interactive eye-toggle asset.
* **⚡ Live Firebase Synchronicity:** Direct pipeline integration into Firebase Authentication and Google Cloud Firestore.

---

## 🛠️ Tech Stack & Architecture

CashTrail leverages a reliable, fast, and scalable modular architecture:

| Category | Technology | Purpose |
| --- | --- | --- |
| **Frontend Core** | React 18 & TypeScript | Component-driven UI with robust compile-time type safety. |
| **Styling Engine** | Custom CSS3 + Poppins | Pure layout control handling serial workflows and glass effects. |
| **Auth Engine** | Firebase Authentication | Secure storage, creation, and session handling of accounts. |
| **Database Tier** | Cloud Firestore | Real-time unique constraint checking for custom user tags. |
| **Alert System** | NotificationFacade Layer | Isolated static feedback mechanism for cross-app alerts. |

---

## 🚀 Quick Start & Installation

Follow these steps to get CashTrail running locally on your machine.

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/cashtrail.git
cd cashtrail

```

### 2. Install Dependencies

```bash
npm install

```

### 3. Configure Environment / Firebase

Ensure you have a `src/firebase.ts` file configured with your active web app credentials. Your configuration file should export the `auth` and `db` contexts directly:

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

### 4. Run the Development Server

```bash
npm run dev

```

Open your browser to the local address displayed in your terminal (usually `http://localhost:5173`) to experience CashTrail!

---

## 🎨 Interactive Animation & UI Deep-Dive

CashTrail doesn't just display components—it feels alive. Here is how the UI works under the hood:

### 🌌 Kinetic Floating Background

The register layout maintains an immersive ambient look using native GPU-accelerated CSS animations. It pairs dual pseudo-elements (`::before` and `::after`) using structural blurs and keyframe translations:

```css
@keyframes float {
  from { transform: translate(0, 0); }
  to { transform: translate(35px, 30px); }
}

```

### 📋 Left-Aligned Serial Onboarding

Inputs are built in a strict vertical column stack (`flex-direction: column`) rather than cluttered grid forms. Labels are explicitly anchored using `.input-box { align-items: flex-start; }` ensuring a seamless, scannable visual read from top to bottom.

### 👁️ Zero-Artifact Password Input

The absolute-positioned interactive eye utility is perfectly anchored alongside input fields without disruptive background circles, utilizing native CSS layer scaling (`transform: scale(1.1)`) and micro-opacity changes upon hovering.

---

## 🔒 Security & Database Integrity Layer

### Account Creation Workflow

```
[ User Form Entry ]
       │
       ▼
[ Client Validation ] ──► (Min 8 Characters + At least 1 letter/special char)
       │
       ▼
[ Firestore Check ]   ──► (Queries DB to verify if 'userName' is unique)
       │
       ▼
[ Firebase Auth ]     ──► (Creates user account instance)
       │
       ▼
[ Sync & Reserve ]    ──► (Saves user data object to Firestore /users/ collection)

```

1. **Gatekeeping Weak Passwords:** CashTrail enforces strict password boundaries through an input evaluation pipeline. Registration fails instantly if the field doesn't match safety metrics or evaluates to `Weak`.
2. **Cloud Username Lock:** Before creating an authentication entry, the pipeline queries your Firestore collection to see if the unique username is claimed. If clear, it registers the account and locks down that username to the user's explicit UID permanently.

---

## ⚙️ Core Firebase Configuration Rules

For data operations to work properly, verify your cloud environment settings mirror the definitions below:

### 🛡️ Firestore Security Rules

Ensure your security profile allows reading and document validation checks during registration:

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /users/{userId} {
      allow read, write: if true; // Secure this configuration conditionally before live production!
    }
  }
}

```

### 🔑 Authentication Provider

* Navigate to your **Firebase Console ➔ Authentication ➔ Sign-in Method**.
* Verify the **Email/Password** toggle is switched to **Enabled**.

---

📊 *Tracking expenses shouldn't be boring. Happy financial pathfinding via CashTrail!*
