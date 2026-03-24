# 💳 Banking & Finance Transaction Analytics

> An interactive Power BI dashboard analyzing financial transaction data — covering transaction patterns, customer profiling, card usage, spending categories, and error monitoring across U.S. states.

---

## 📌 Project Overview

This Power BI report provides a comprehensive view of banking transaction activity using a custom **FinScope Analytics** theme. The dashboard is designed for financial analysts and product teams who need to monitor transaction volume, understand customer demographics, identify high-risk error patterns, and track spending behavior across merchant categories.

---

## 🗂️ Data Model

The report is built on **4 related tables:**

| Table | Description |
|---|---|
| `transactions_data` | Core fact table — transaction records with date, time, amount, payment method, errors, and merchant state |
| `users_data` | Customer demographics — age group, gender, income bracket, credit score range |
| `cards_data` | Card attributes — card brand, card type, chip availability |
| `mcc_codes` | Merchant Category Codes — maps transactions to spending categories |

**Key Measures (DAX):**

| Measure | Description |
|---|---|
| `Total Transactions` | Count of all transactions |
| `Total Amount` | Sum of transaction values |
| `Avg Transaction` | Average transaction value |
| `Total Cards` | Count of active cards |
| `Total Users` | Count of unique customers |
| `Error Rate %` | Share of transactions with errors |
| `Count of Errors` | Total error count |

---

## 📊 Report Pages

### Page 1 — Transaction Overview
**Purpose:** High-level monitoring of transaction volume, value, and operational health.

**KPI Cards:**
- Total Transactions · Total Amount · Avg Transaction · Active Cards · Error Rate %

**Charts:**
- 📈 Transactions & amount by month (line + column combo)
- ⏰ Transactions by hour of day (0–23h) — identify peak usage windows
- 🍩 Payment method breakdown (chip vs. swipe vs. online)
- 🏆 Top 15 U.S. states by transaction count

**Slicers:** Date Range · Card Brand · Payment Method · State

---

### Page 2 — Customer & Cards
**Purpose:** Demographic profiling of the customer base and card portfolio analysis.

**Charts:**
- 👥 Age group distribution
- ⚧️ Gender breakdown
- 💰 Income bracket distribution
- 📊 Credit score range segmentation
- 💳 Card brand market share
- 🃏 Card type breakdown
- 🔲 Chip-enabled cards vs. non-chip

**Slicers:** Date Range · Gender · Card Type

---

### Page 3 — Spending Categories
**Purpose:** Analysis of where and how customers spend, with error pattern monitoring.

**Charts:**
- 🗂️ Spending by MCC category (treemap)
- 📈 Category spending trends over time (line chart)
- 📊 Top categories by volume (bar chart)
- 🗺️ Geographic spending distribution (filled U.S. map)

**Slicers:** Date Range · MCC Category · Error Type

---

## 🛠️ Tools & Techniques

- **Power BI Desktop** — report design and publishing
- **DAX** — calculated measures (Total Amount, Error Rate %, Avg Transaction, etc.)
- **Data Modeling** — star schema with `transactions_data` as fact table
- **Custom Theme** — FinScope Analytics (consistent color palette across all visuals)
- **Interactive Slicers** — cross-filtering across all pages for drill-down analysis

---

## 💡 Key Insights

1. **Hourly patterns** in transaction volume reveal clear peak hours — useful for fraud detection threshold adjustment and infrastructure capacity planning.
2. **Error Rate %** tracked as a KPI card allows real-time monitoring of operational failures, helping flag anomalies quickly.
3. **Geographic distribution** (Top 15 states + filled map) highlights regional concentration risk and expansion opportunities.
4. **Credit score segmentation** combined with spending patterns can support targeted product offerings and credit limit strategies.
5. **MCC category analysis** enables product teams to understand customer spending behavior and design relevant rewards or cashback programs.

---

## 📁 File Structure

```
Banking_and_Finance_Project.pbix
│
├── Data Model
│   ├── transactions_data    ← Fact table (transactions)
│   ├── users_data           ← Customer demographics
│   ├── cards_data           ← Card attributes
│   └── mcc_codes            ← Merchant category lookup
│
└── Report Pages
    ├── 1. Transaction Overview    ← Volume, amount, error rate, geography
    ├── 2. Customer & Cards        ← Demographics, card portfolio
    └── 3. Spending Categories     ← MCC analysis, geographic spend map
```

---

## 🚀 How to Use

1. Download `Banking_and_Finance_Project.pbix`
2. Open with **Power BI Desktop** (free download at [powerbi.microsoft.com](https://powerbi.microsoft.com))
3. Use the **slicers** on each page to filter by date range, card brand, payment method, gender, or MCC category
4. Visuals are cross-filtered — clicking any chart element filters the entire page

> **To publish:** Open in Power BI Desktop → Publish to Power BI Service → share the report link for browser-based access (no Power BI Desktop required for viewers).

---

## 📸 Dashboard Preview

<img width="1680" height="1050" alt="Screenshot 2026-03-24 at 08 25 55" src="https://github.com/user-attachments/assets/6450acbe-da16-4fba-a727-77a96e1e49cc" />

<img width="1680" height="1050" alt="Screenshot 2026-03-24 at 08 26 07" src="https://github.com/user-attachments/assets/c5424dd2-ad2c-4083-a4f8-02dbabf022ba" />

<img width="1680" height="1050" alt="Screenshot 2026-03-24 at 08 26 56" src="https://github.com/user-attachments/assets/412af080-8284-4a18-a0b9-a9ddce9fbdf3" />

| Page | Preview |
|---|---|
| Transaction Overview | `<img width="1680" height="1050" alt="Screenshot 2026-03-24 at 08 25 55" src="https://github.com/user-attachments/assets/f7a14373-6e10-4b93-9d79-d05fe16f4a4a" />` |
| Customer & Cards | `screenshots/02_customer_cards.png` |
| Spending Categories | `screenshots/03_spending_categories.png` |

---

## 👤 Author

**Vo Quang Khai**
Data Analyst | Finance & Data Science Background
[LinkedIn](https://www.linkedin.com/in/voquangkhaikg2003/) · [GitHub](https://github.com/voquangkhai2003)
