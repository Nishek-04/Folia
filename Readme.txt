# 💰 Folia — Premium Finance Dashboard

## 📌 Overview

**Folia** is a frontend-only finance dashboard built as part of an internship evaluation.
It focuses on **clean UI, structured state management, and real-time interactivity** using **Vanilla JavaScript (no frameworks, no backend)**.

The project demonstrates how a static design can be transformed into a **functional, production-like fintech interface**.

---

## 🚀 Features

### 🎨 UI & Design

* Dark luxury theme (charcoal + gold accents)
* Typography: Playfair Display, Outfit, JetBrains Mono
* Smooth transitions and hover effects
* Responsive layout (desktop + mobile)

---

### ⚙️ Core Functionality

* Centralized **AppState management**
* Dynamic **view switching (sidebar navigation)**
* Add transactions (with realistic mock data)
* Real-time **stats calculation**:

  * Total Balance
  * Income
  * Expenses
* Search-based filtering
* History view (mirrors transaction list)
* Theme toggle (dark/light)
* LocalStorage persistence

---

### 📊 State Management Approach

This project uses a **Vanilla JS state architecture**:

```js
const AppState = {
  transactions: [],
  view: "overview",
  dark: true
};
```

### Key Concept:

```js
function setState(patch) {
  Object.assign(AppState, patch);
  save();
  render();
}
```

👉 This ensures:

* Single source of truth
* Predictable UI updates
* Clean and interview-friendly logic

---

## 🧱 Architecture

### Render Flow

```js
render() {
  renderView();
  renderStats();
  renderTransactions();
  renderHistory();
  renderGreeting();
}
```

### Data Flow

User Action → setState() → AppState Update → render() → UI Update

---

## 🔐 Role-Based Access (Planned / Extendable)

* Admin → Full access (add/edit/delete/export)
* Viewer → Read-only UI

(Current version is structured to support RBAC easily)

---

## 📱 Responsiveness

* Sidebar becomes toggleable on mobile
* Content adjusts without hiding key components
* Table becomes scrollable horizontally

---

## 💾 Persistence

* Uses `localStorage`
* Transactions survive page refresh
* Theme preference retained

---

## 🧪 Mock Data

* Preloaded transactions for testing
* Random transaction generator for demo

---

## 🛠️ Tech Stack

* HTML (Single file)
* CSS (Custom, no frameworks)
* JavaScript (Vanilla)

---

## ▶️ How to Run

1. Download the project
2. Open `index.html` in any browser
3. No setup or dependencies required

---

## 🎯 Key Highlights (For Interviewers)

* No frameworks used — demonstrates core JS strength
* Clean state-driven architecture
* Functional UI (not just design)
* Scalable structure for future backend integration
* Focus on UX + engineering balance

---

## 🚧 Future Improvements

* Dynamic charts (bar + donut)
* Advanced filters (date range, category)
* Pagination system
* CSV / JSON export
* Full RBAC implementation

---

## 🧠 Conclusion

Folia is designed to showcase:

> “How to think like a frontend engineer, not just design like one.”

It bridges the gap between:

* **Beautiful UI**
* **Functional product behavior**

---

## 👤 Author

Built by: *[Nishek]*
Role: Frontend Developer / Aspiring Product Engineer

---
