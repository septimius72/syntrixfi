# SyntrixFi — Household Financial Operating System

<div align="center">

![SyntrixFi Banner](https://img.shields.io/badge/Syntrix-Fi-4f46e5?style=for-the-badge&logo=cashapp&logoColor=white)
![Build](https://img.shields.io/badge/Architecture-Single--File%20(Vanilla%20JS)-emerald?style=for-the-badge)
![Data Privacy](https://img.shields.io/badge/Storage-100%25%20Local--First-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-slate?style=for-the-badge)

**A deterministic, zero-server household finance engine combining zero-based envelope budgeting, dynamic sinking fund accruals, and an algorithmic debt elimination cascade.**

[Live Demo](#live-deployment) • [Key Features](#core-pillars) • [Quick Start](#quick-start) • [Data & Privacy](#data-sovereignty--privacy)

</div>

---

## ⚡ Overview

Most personal finance software falls into one of two traps: bloated SaaS applications that demand bank credentials and monthly subscriptions, or rigid spreadsheets with high maintenance friction.

**SyntrixFi** is built on a single-file, local-first paradigm. It runs entirely inside any modern web browser without dependencies, Node runtimes, build chains, or remote backends. Your financial data is saved locally on your device in `localStorage`, never leaving your machine.

---

## 🏛️ Core Pillars

### 1. Zero-Based Envelope Budgeting & Cash-Flow Ledger
- **Every Dollar Has a Duty:** Live reconciliation between monthly household net inflow and allocated category ceilings.
- **Dynamic Overrun Gauges:** Multi-tier color indicators (Emerald `<80%`, Amber `80–99%`, Rose `100%+`) alert you before overspending becomes structural.
- **Auditable Ledger:** Chronological transaction log with multi-parameter filtering (by flow type, envelope category, or text query).
- **Keyboard Ergonomics:** Press `N` anywhere to log an entry; use `Esc` to instantly dismiss modals.

### 2. Sinking Funds Dynamic Accrual Engine
Irregular annual or semi-annual obligations (auto insurance renewals, municipal property taxes, holiday gifts) often derail monthly budgets. 

SyntrixFi calculates dynamic monthly drips using a deterministic accrual model:

$$\text{Monthly Drip} = \frac{\text{Target Goal} - \text{Accumulated Balance}}{\max(1, \text{Months Until Target Date})}$$

- **One-Click Auto-Drip:** Automatically distribute recommended savings across all sinking funds in a single click.
- **Spend & Drain Workflow:** Disburse funds when the bill arrives, book the expense into the cash-flow ledger, and reset the target date for the next renewal cycle.

### 3. Debt Accelerator (Snowball vs. Avalanche)
Eliminate household liabilities methodically by isolating mandatory minimum payments from an accelerated attack fund:

- **❄️ Debt Snowball (Dave Ramsey Method):** Targets the smallest balance first for psychological momentum.
- **⚡ Debt Avalanche (Mathematically Optimal):** Targets the highest APR debt first to minimize total interest paid.
- **Surplus Accelerator Pairing:** Automatically captures surplus funds budgeted to the Debt envelope and routes 100% of the booster into the active `#1 Priority Bullseye`.
- **Household Burndown Tracker:** Real-time visual progress showing total debt principal reduction and cleared liabilities.

---

## 🔒 Data Sovereignty & Privacy

- **Zero Cloud Servers:** SyntrixFi does not send your data to external endpoints, analytics services, or cloud providers.
- **Spreadsheet Interoperability:** Export and import standard CSV transaction registers for seamless use with Microsoft Excel or Google Sheets.
- **Disaster Recovery:** Export one-click encrypted JSON snapshots to back up your full ledger, envelopes, sinking funds, and debts.

---

## 🚀 Quick Start

SyntrixFi requires **no installation, Node.js, npm, or build step**.

### Option A: Direct Browser Launch
1. Download or clone this repository:
   ```bash
   git clone https://github.com/your-username/syntrixfi.git
   ```
2. Open `index.html` directly in any web browser (Chrome, Firefox, Safari, Edge, Brave).

### Option B: Local HTTP Server (Optional)
```bash
cd syntrixfi
python3 -m http.server 8080
# Open http://localhost:8080 in your browser
```

---

## 🛠️ Tech Stack & Architecture

- **Core Runtime:** Pure Vanilla JavaScript (ES6+), HTML5, CSS3.
- **Styling Engine:** [Tailwind CSS](https://tailwindcss.com/) (delivered via CDN).
- **Iconography:** [Phosphor Icons](https://phosphoricons.com/).
- **Persistence Layer:** Browser `localStorage` API under the atomic key `syntrixfi_state`.
- **Footprint:** Single `index.html` file.

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| <kbd>N</kbd> | Open New Transaction / Entry Modal |
| <kbd>Esc</kbd> | Close any open modal |

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for further details.