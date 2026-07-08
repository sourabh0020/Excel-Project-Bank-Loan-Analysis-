# 🏦 Bank Loan Analysis Dashboard — Excel + SQL

End-to-end analytics project on retail bank lending performance — 38,600+ loan applications totaling $435.8M funded and $473.1M collected. Built to give credit risk and business teams a single source of truth on loan quality, funding performance, and portfolio risk.

**Tools:** SQL (Data Validation) · Excel (Data Cleaning, DAX-style formulas, Dashboard Design)

## 📊 Dashboard Preview

| Overview |
|---|---|
| ![Overview](https://github.com/sourabh0020/Excel-Project-Bank-Loan-Analysis-/blob/main/BANKLOAN%20OVERVIEW.png) 
|---|---|
| Summary |
|---|---|
| ![Summary](https://github.com/sourabh0020/Excel-Project-Bank-Loan-Analysis-/blob/main/BANKLOAN%20SUMMARY%20DASHBOARD%20.png) 

## 🎯 Problem Statement

The raw loan dataset had no structure for the business questions that actually mattered:

- Which loan segments are healthy, and which are at risk?
- How is the portfolio performing month-over-month?
- Which states, purposes, and grades concentrate the most volume — and the most risk?
- Can the Excel logic be trusted, or does it need independent validation?

## 🗂️ Dataset

| | |
|---|---|
| **Scale** | ~38,600 loan applications |
| **Coverage** | All U.S. states · loan issue dates across a full calendar year |
| **Key fields** | issue_date, loan_amount, total_payment, int_rate, dti, term, grade, purpose, emp_length, home_ownership, address_state, loan_status |

The dataset arrived pre-cleaned, so the workflow focused on validating logic and building analysis-ready structure rather than heavy cleansing.

## 🛠️ Workflow

- **Data cleaning in Excel** — removed duplicates, standardized categorical values, and added helper columns for MoM %, MTD, and Loan Status grouping (Good vs. Bad Loan).
- **SQL-based validation** — every KPI and aggregation was independently verified in SQL before being trusted in the dashboard: application counts, funded/received totals, good vs. bad loan splits, and category-level breakdowns by state, term, purpose, employment length, and home ownership. See `Bank_loan_Query.sql`.
- **Dashboard design in Excel** — two linked views (Summary and Overview) with slicers for Grade and Purpose, built using SUMIFS, VLOOKUP, IF, and DATEDIF-based formulas.

## 💡 Key Insights

- **85.88% of applications are good loans** (Fully Paid or Current) — $370.2M funded, $435.8M collected — against **14.12% bad loans** (Charged Off) with $65.5M funded and only $37.3M recovered.
- **Charged-off loans carry the highest average interest rate (13.88%) and DTI (14.00%)** of any status group — the risk was priced in but not fully offset by recovery.
- **Credit card and debt consolidation are the top loan purposes**, together accounting for the largest share of applications and volume.
- **36-month terms dominate the portfolio** (28.2K applications vs. 10.3K for 60-month terms), consistent with lower-risk, shorter-duration lending.
- **California, Texas, and Florida are the highest-volume states** for applications and funded amount.
- **December is peak season** (4.3K applications, the highest single month, +6.9% MoM) — funded and collected amounts also spike at MTD ($54.0M funded, $58.1M collected).
- **Renters and mortgage-holders make up 92%+ of applicants** (18.4K rent, 17.2K mortgage vs. 2.8K own), a useful signal for segmenting credit risk by housing status.

## 📈 Business Impact

These findings support concrete decisions: tightening underwriting criteria for the interest-rate/DTI band most associated with charge-offs, prioritizing collections focus on higher-risk purposes and states, and using the December volume spike to plan staffing and campaign timing for the next cycle.

## 📁 Repo Structure

```
├── README.md
├── sql/
│   └── Bank_loan_Query.sql          # KPI validation & business-question queries
├── docs/
│   └── BANK_LOAN_REPORT_QUERY_DOCUMENT.docx
├── images/
│   ├── BANKLOAN_OVERVIEW.png
│   └── BANKLOAN_SUMMARY_DASHBOARD.png
└── data/
    └── Bank_loan_project.xlsx
```

## 🚀 What I'd Improve Next

- Add a drill-through view from state/purpose into individual loan-level records.
- Build a delinquency early-warning measure using DTI and interest-rate thresholds.
- Migrate the dashboard to Power BI for native DAX time intelligence (rolling MTD/MoM without manual formulas).

**Author:** Sourabh Yadav · LinkedIn · GitHub
