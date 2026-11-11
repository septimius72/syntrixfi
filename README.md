[project_readme.md](https://github.com/user-attachments/files/34706443/project_readme.md)
# SyntrixFi — Modern Cash Ledger & Liquidity Register

A fast, lightweight, and modern single-page cash ledger designed with a clean fintech aesthetic. SyntrixFi tracks inbound earnings, outbound expenses, free-form category tags, and real-time running balances without backend dependencies or tracking.

---

## ✨ Features

- **Real-Time Running Balance Engine:** Automatically sorts entries chronologically to compute cumulative cash flow from zero, displaying records newest-first for rapid scanning.
- **Rapid Inline Entry:** An always-visible input bar pinned above the table with quick `+ In` / `- Out` toggling, keyboard shortcuts, and instant submit.
- **Direct Click-to-Edit Cells:** Edit descriptions, dates, category tags, or numeric values directly inside table cells (`contenteditable`) with instant recalculation on blur or <kbd>Enter</kbd>.
- **Titanium & Obsidian Aesthetic:** Modern glassmorphism UI with frosted glass backdrops, tabular monospace typography for currency, and high-contrast electric neon accents (Emerald & Rose).
- **Adaptive Day / Night Modes:** Automatic system theme detection with a manual dark/light toggle.
- **Zero-Dependency Architecture:** Single standalone HTML file with Tailwind CSS and Phosphor Icons loaded via CDN. Runs locally straight out of the box.
- **Privacy & Local-First:** All financial data remains on your machine. Includes a safe storage fallback layer to ensure full functionality even when launched directly via `file:///` protocols in locked-down browser profiles.
- **Universal CSV Export:** Export your entire register to a standard `.csv` format ready for Excel, Apple Numbers, or Google Sheets.

---

## 🚀 Quick Start

SyntrixFi requires **no build tools, runtime environments, or web servers**.

### 1. Download or Clone
```bash
git clone https://github.com/your-username/syntrixfi.git
cd syntrixfi
```

### 2. Launch
Double-click `index.html` or open it with your browser:
```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

---

## ⌨️ How to Use

### Adding an Entry
1. Select the **Date** (defaults to today).
2. Type a **Description** (e.g., `Client Retainer`, `Grocery Run`).
3. Enter a **Category Tag** (e.g., `Salary`, `Food`, `Utilities`).
4. Toggle between **`+ In`** (Inbound / Earning) or **`- Out`** (Outbound / Spending).
5. Type the **Amount** and press <kbd>Enter</kbd> or click the `+` button.

### Editing an Existing Row
- Click directly on any cell in the table (Date, Description, Category Tag, or Amount).
- Modify the text or number.
- Press <kbd>Enter</kbd> or click outside the cell to commit. The running balances will recalculate automatically across the entire register.

### Deleting a Row
- Hover over any row and click the trash icon on the far right.

### Exporting Data
- Click **Export CSV** in the top navigation bar to download a full spreadsheet export named `SyntrixFi_Ledger_YYYY-MM-DD.csv`.

---

## 🛠️ Tech Stack

- **HTML5 & Vanilla JavaScript (ES6+)**
- **[Tailwind CSS](https://tailwindcss.com/)** (CDN runtime)
- **[Phosphor Icons](https://phosphoricons.com/)** (Scalable UI icons)
- **SafeStorage Adapter** (Dual `localStorage` and runtime in-memory storage fallback)

---

## 📁 File Structure

```text
├── index.html       # Self-contained single-page web app (structure, styles, logic)
└── README.md        # Documentation
```

---

## 🔒 Security & Privacy

SyntrixFi does not send your financial numbers across the internet. There are no tracking scripts, third-party analytics, or remote database connections. All records are persisted locally within your browser's private storage.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
