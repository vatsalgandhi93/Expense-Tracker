# 💸 Personal Expense Tracker

A clean, interactive monthly expense tracker that runs entirely in your browser — no signup, no backend, no data leaving your machine. One HTML file. Open it and go.

> 🔗 **[Live Demo →](https://vatsalgandhi93.github.io/Expense-Tracker)**

---

![Expense Tracker Dashboard](screenshot-dashboard.png)
<!-- Replace with your actual screenshot filename -->

---

## ✨ What's Inside

### Money management
- **Multi-account support** — add multiple bank accounts and credit cards. Each credit card is linked to the bank account that pays it off, so the money flow is modelled accurately.
- **10 spending categories** — Housing & Utilities, Household Essentials & Supplies, Food & Dining, Transportation, Childcare & Kids' Expenses, Lifestyle Spending, Healthcare & Insurance, Travel & Entertainment, Savings & Investments, Miscellaneous
- **Net income & savings tracking** — enter your monthly take-home and watch your savings (or deficit) update in real time. The savings card flips red if you overspend.

### Statement import (auto-categorised)
- **Upload PDF statements** — drag-and-drop or click to upload
- **Two flows for two statement types**:
  - **Credit Card** — every line is parsed as a charge
  - **Bank Account** — debits and credits are separated; credits (deposits, payroll) are excluded by default or optionally added to your income
- **100+ merchant keyword dictionary** — Whole Foods → Food & Dining, Shell → Transportation, Netflix → Travel & Entertainment, and so on
- **Smart credit/debit detection** for bank statements — payroll, ACH credits, refunds, transfers, and Zelle deposits are auto-flagged
- **Review before importing** — every transaction is shown with its auto-assigned category. Edit anything, uncheck transactions you don't want, then confirm.
- **Quick "Add new card / account"** — create a new account inline during import without leaving the modal
- **Raw text viewer** — debug tool to see exactly what was extracted from the PDF in case the parser missed something

### Live visualisations
- **Donut chart** — category breakdown with percentages
- **Bar chart** — spending by category, ranked largest to smallest
- **Sankey flow diagram** — traces every dollar across 3 stages:
  ```
  Bank Account  →  Credit Card  →  Category
  ```
  Wider ribbons = more money flowed that way. Bank-direct expenses skip the credit card column.

### 🆕 Interactive Sankey drill-down
- **Click any category node** in the Sankey and the diagram expands into a per-merchant view
- **Merchants are intelligently grouped** — five Starbucks visits become one node labeled "Starbucks (5×)" with the total combined
- **Smart name normalisation** — store numbers, transaction codes, and entity suffixes (LLC, INC) are automatically stripped, so "STARBUCKS #1234" and "STARBUCKS #5678" merge into one
- **"Back to overview"** button returns to the standard 3-stage view
- **Auto-exits** if the focused category becomes empty (e.g. all expenses deleted)

### Export
- **Save as PDF** — one-click PDF export of your current view, perfect for monthly archives or sharing
- Hidden elements (forms, buttons, tooltips) are automatically excluded from the print output for a clean snapshot

### Extras
- **Built-in "How to use" guide** — a comprehensive tutorial modal for first-time users
- **Dark mode** — automatically follows your system preference
- **Fully offline** — no server, no API calls, no tracking, no cookies
- **Responsive design** — works on desktop, tablet, and mobile

---

## 🚀 Getting Started

### Option 1 — Use the live demo
Click the **[Live Demo](https://vatsalgandhi93.github.io/Expense-Tracker)** link above. Nothing to install.

### Option 2 — Run locally
```bash
# Clone the repo
git clone https://github.com/vatsalgandhi93/Expense-Tracker.git

# Open in your browser — that's it
open index.html
```

No build step. No `npm install`. No config. Just open the file.

---

## 🗂️ How to Use

1. **Add a bank account** — open the Accounts panel, enter a name (e.g. Chase Checking) and optionally last 4 digits
2. **Add credit cards** *(optional)* — enter the card name and select which bank account pays it off
3. **Log expenses** — either manually (description, amount, category, account) or by importing a PDF statement
4. **Set your net income** — type your monthly take-home in the income tile to see your savings calculated automatically
5. **Explore the Sankey** — click any category node to drill down into individual merchants
6. **Save your view as PDF** — click the download icon in the header to export a clean snapshot
7. **Delete any entry** — click the trash icon in the expense log; all charts update instantly

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | CSS3 (custom properties, dark mode, print styles) |
| Logic | Vanilla JavaScript (ES6+) |
| Charts | [Chart.js 4.4](https://www.chartjs.org/) |
| Sankey diagram | Custom renderer built on [D3.js 7](https://d3js.org/) |
| PDF parsing | [PDF.js 3.11](https://mozilla.github.io/pdf.js/) |
| Icons | [Tabler Icons](https://tabler-icons.io/) |

No frameworks. No bundler. No dependencies to install. Everything is loaded from CDNs at runtime.

---

## 🔒 Privacy

This app runs **100% in your browser**. There is no backend, no server, no database. Your financial data:
- Never leaves your machine
- Is never sent anywhere
- Is never logged or tracked
- Disappears when you close the tab (no persistence by design)

When you upload a PDF statement, PDF.js parses it locally — the file is never uploaded to a server.

---

## 📁 Project Structure

```
Expense-Tracker/
├── index.html        # The entire application — self-contained
├── README.md         # This file
└── LICENSE.md        # Usage terms
```

---

## 📸 Screenshots

| Dashboard Overview | Sankey Flow Diagram |
|---|---|
| ![Dashboard](screenshot-charts.png) | ![Sankey](screenshot-sankey.png) |

| Sankey Drill-down | Statement Import |
|---|---|
| ![Drilldown](screenshot-drilldown.png) | ![Import](screenshot-import.png) |

<!-- Replace with your own screenshots -->

---

## 🆕 What's New

**Latest update — Interactive Sankey + Statement Import + Expanded Categories**

- ✨ Click any category node in the Sankey to drill into a per-merchant breakdown
- ✨ Upload PDF statements (credit card or bank account) for auto-categorised import
- ✨ Smart credit/debit detection for bank statements — deposits handled separately from expenses
- ✨ Added 10th category: **Household Essentials & Supplies**
- ✨ Renamed "Personal Care, Fitness & Discretionary" to **Lifestyle Spending**
- ✨ Save as PDF for monthly archives
- ✨ "How to use" guide accessible from the header at any time

---

## 🤝 Feedback

Have a suggestion or found a bug? I'd love to hear from you.

- 📧 [vatsalgandhi93@gmail.com](mailto:vatsalgandhi93@gmail.com)
- 💼 [linkedin.com/in/vatsalgandhi93](https://www.linkedin.com/in/vatsalgandhi93)

---

## 📄 License

This project is licensed under a custom proprietary license.
See [LICENSE.md](LICENSE.md) for full terms.

**TL;DR:** Free for personal, non-commercial use. Redistribution, modification, and commercial use are prohibited.

© 2026 Vatsal Gandhi. All rights reserved.

---

*Built with [Claude](https://claude.ai) as a thinking partner.*
