#  Bank Loan Analysis Report

> An end-to-end Exploratory Data Analysis (EDA) project on a real-world financial loan dataset, uncovering borrower behavior, loan performance, and portfolio health using Python.

---

##  Project Overview

This project performs a comprehensive analysis of a bank's loan portfolio containing **38,576 loan applications**. The goal is to derive actionable insights for risk management, portfolio monitoring, and strategic decision-making — the kind of analysis performed by financial analysts and data teams in banks and NBFCs (Non-Banking Financial Companies).

The analysis covers everything from basic KPIs like total funded amount and repayment rates, to deeper segmentations by geography, loan purpose, employment profile, and home ownership.

---

##  Objectives

- Calculate and monitor key loan portfolio metrics (total applications, funded amount, repayments)
- Distinguish between **Good Loans** (Fully Paid / Current) and **Bad Loans** (Charged Off)
- Identify monthly and seasonal trends in loan disbursement
- Perform regional, demographic, and behavioral segmentation of borrowers
- Visualize findings through clean, professional charts for stakeholder reporting

---

## 📂 Dataset

| File | Description |
|------|-------------|
| `financial_loan.xlsx` | Main dataset containing loan application records |

**Key Columns Used:**

| Column | Description |
|--------|-------------|
| `id` | Unique loan application identifier |
| `issue_date` | Date the loan was issued |
| `loan_amount` | Amount funded to the borrower |
| `total_payment` | Total amount repaid by borrower |
| `int_rate` | Interest rate charged on the loan |
| `dti` | Debt-to-Income ratio of the borrower |
| `loan_status` | Current status: Fully Paid, Current, or Charged Off |
| `address_state` | Borrower's state of residence |
| `term` | Loan term (36 or 60 months) |
| `emp_length` | Borrower's years of employment |
| `purpose` | Stated purpose of the loan |
| `home_ownership` | Borrower's home ownership type |

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python 3** | Core programming language |
| **Pandas** | Data manipulation and aggregation |
| **Matplotlib** | Static data visualizations |
| **Seaborn** | Statistical plot styling |
| **Plotly Express** | Interactive treemap visualization |
| **Google Colab** | Cloud-based development environment |

---

## 📊 Analysis Breakdown

### 1. Portfolio Summary KPIs
- **Total Loan Applications:** 38,576
- **Total Funded Amount:** Aggregated in $Millions
- **Total Amount Received:** Aggregated in $Millions
- **Average Interest Rate** and **Average DTI** computed across all loans
- All metrics also computed for **Month-to-Date (MTD)** — the most recent calendar month in the dataset

### 2. Good Loan vs Bad Loan Classification

Loans are classified based on `loan_status`:

| Category | Status Values | Metrics Computed |
|----------|--------------|-----------------|
| ✅ Good Loan | Fully Paid, Current | Count, Funded Amount, Received Amount, % Share |
| ❌ Bad Loan | Charged Off | Count, Funded Amount, Received Amount, % Share |

>  The portfolio maintains a **~86.5% good loan rate**, reflecting strong overall credit quality.

### 3. Monthly Trend Analysis
- **Total Funded Amount by Month** — Area + Line chart showing month-by-month disbursement growth
- **Total Amount Received by Month** — Tracks monthly repayment inflows
- Both charts reveal **seasonal borrowing patterns** and consistent growth trends

### 4. Regional Analysis (by State)
- Horizontal bar chart of funded amounts across all US states
- Identifies which states drive the highest loan volumes
- Highlights geographic concentration risk in the portfolio

### 5. Loan Term Distribution
- Donut chart comparing **36-month vs 60-month** loan terms
- Both the percentage share and absolute dollar amounts are shown

### 6. Employment Length Analysis
- Examines how funded amounts vary across borrower employment tenure
- Borrowers with **10+ years of employment** receive significantly higher loan amounts

### 7. Loan Purpose Breakdown
- Horizontal bar chart categorizing loans by stated purpose
- **Debt consolidation** dominates, indicating most borrowers are refinancing existing debt

### 8. Home Ownership Analysis
- Interactive **Treemap** (Plotly) showing funded amounts by home ownership category
- Segments: RENT, MORTGAGE, OWN, and others

---

##  How to Run

### Option 1: Google Colab (Recommended)
1. Upload `financial_loan.xlsx` to your Colab session
2. Open or upload `financedomain.py`
3. Ensure the file path in the script matches: `/content/financial_loan.xlsx`
4. Run all cells sequentially

### Option 2: Local Environment
```bash
# 1. Clone or download the project files

# 2. Install required libraries
pip install pandas numpy matplotlib seaborn plotly openpyxl

# 3. Update the file path in the script
#    df = pd.read_excel("path/to/financial_loan.xlsx")

# 4. Run the script
python financedomain.py
```

---

## 📈 Key Insights

| Insight | Detail |
|---------|--------|
| 📉 Portfolio Health | ~86.5% good loan rate indicates low default risk |
| 📅 Seasonal Demand | Loan disbursements show consistent monthly growth |
| 🗺️ Geographic Skew | A few states dominate loan volumes — concentration risk |
| ⏱️ Term Preference | Borrowers prefer 36-month terms over 60-month |
| 💼 Employment Trust | Longer-tenured employees receive larger loan approvals |
| 🔁 Debt Consolidation | Most borrowers use loans to refinance existing debt |
| 🏠 Home Ownership | Renters and mortgagees form the bulk of the borrower base |

---

## 📁 Project Structure

```
bank-loan-analysis/
│
├── financial_loan.xlsx       # Raw dataset
├── financedomain.py          # Main analysis script (converted from Colab notebook)
└── README.md                 # Project documentation
```

---

## 🙋 About This Project

This project was developed as part of a financial domain data analysis case study. It demonstrates practical skills in:
- **Financial data wrangling** with Pandas
- **KPI computation** aligned with real banking metrics (MTD, funded amount, DTI)
- **Risk segmentation** (good vs bad loan classification)
- **Data storytelling** through varied chart types (area charts, bar charts, pie/donut, treemaps)

---

## 📜 License

This project is for educational and portfolio purposes only. The dataset used is anonymized and does not contain any personally identifiable information (PII).
