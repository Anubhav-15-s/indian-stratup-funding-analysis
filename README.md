# indian-stratup-funding-analysis

Here’s a `README.md` file for your `main.py` script:

---

# Startup Funding Data Analysis

## 📌 Overview

This project analyzes Indian startup funding data from a CSV file, performing **data cleaning, preprocessing, aggregation, and visualization**.
It produces insights such as yearly trends, top-funded sectors, cities, startups, investors, and investment types.

---

## 📂 Dataset

* **File:** `startup_funding.csv`
* **Columns used:**

  * `Sr No`
  * `Date dd/mm/yyyy`
  * `Startup Name`
  * `Industry Vertical`
  * `SubVertical`
  * `City  Location`
  * `Investors Name`
  * `InvestmentnType`
  * `Amount in USD`
  * `Remarks` *(optional, dropped if present)*

---

## 🛠 Steps Performed

### 1️⃣ Data Cleaning

* Removed **`Remarks`** column (if exists)
* Filled missing values in key columns (`Industry Vertical`, `SubVertical`, `City  Location`, `Investors Name`, `InvestmentnType`) with `"Unknown"`
* Cleaned `Amount in USD`:

  * Removed commas and plus signs
  * Converted to numeric, replacing invalid entries with `0`
* Converted `Date dd/mm/yyyy` to proper datetime format
* Trimmed spaces, removed non-ASCII characters, standardized text to lowercase

### 2️⃣ Feature Engineering

* Extracted:

  * **Funding Year**
  * **Funding Month**

### 3️⃣ Data Aggregation

* **Yearly Funding Trends:** total funding & deal counts per year
* **Monthly Funding Trends:** total funding & deal counts per month
* **Top 10 Lists:**

  * Sectors
  * Cities
  * Startups
  * Investors (by funding & deals)
  * Investment Types (by funding & deals)

### 4️⃣ Data Visualization

Plots generated using **Matplotlib** & **Seaborn**:

1. Yearly funding trends (funding vs deals)
2. Top 10 sectors by funding
3. Top 10 cities by funding
4. Top 10 startups by funding
5. Top 10 investors by funding
6. Top 10 investors by deals
7. Top 10 investment types by funding
8. Top 10 investment types by deals

---

## 📦 Requirements

```bash
pip install pandas matplotlib seaborn
```

---

## ▶️ Usage

1. Place `startup_funding.csv` in the project directory
2. Run:

```bash
python main.py
```

3. The script will:

   * Clean & process data
   * Show top aggregated tables
   * Display charts for trends & top categories

---

## 📊 Output Examples

* **Yearly funding growth over time**
* **Top investors and their funding amounts**
* **Most funded sectors and cities**

---

## 📜 License

This project is for educational and analytical purposes.

