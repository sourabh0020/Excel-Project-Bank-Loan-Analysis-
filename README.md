🏦 Bank Loan Analysis Dashboard – Excel + SQL Project
📊 Overview
This project features an interactive Excel dashboard that analyzes over 38,000 bank loan applications. It tracks loan performance metrics such as:

Total Applications, Amount Funded, Amount Received

Average Interest Rate & DTI (Debt-to-Income Ratio)

Application breakdowns by Purpose, State, Term, Grade, and Employment Length

The goal was to transform raw data into actionable insights for business and credit risk analysis.

❓ Problem Statement
The raw loan dataset lacked structure, making it difficult to extract trends and monitor performance effectively:

No time-based or category-wise breakdown

Hard to distinguish between good and bad loan segments

No way to validate the accuracy of Excel logic

🎯 Objectives
Clean, transform, and visualize loan data in Excel

Validate all calculations and filters using SQL queries

Deliver a user-friendly, insight-rich dashboard for business stakeholders

🛠️ Project Workflow
🧹 Step 1: Data Cleaning in Excel
Removed duplicates and standardized categorical values

Added helper columns for MoM%, MTD, Loan Status grouping, etc.

Prepared the dataset using Excel formulas and lookup functions

🛠️ Step 2: Data Validation Using SQL
Before dashboard creation, all key metrics and aggregations were validated using SQL to ensure accuracy:

Verified total loan applications, amounts, and group-level counts

Cross-checked bad loan percentages, averages (interest, DTI), and categorical splits

Ensured calculated fields in Excel matched SQL logic results

✅ This step helped ensure data accuracy and trustworthiness of the final Excel dashboard.

📈 Step 3: Dashboard Creation in Excel
The dashboard consists of two main views:

📌 Overview Dashboard
KPIs: Total Applications, Funded Amount, Received Amount, Avg Interest Rate, Avg DTI

Charts:

Monthly Application Trends (line chart)

Application by State (map chart)

Purpose-wise Applications (bar & tree map)

Term-wise Distribution (donut chart)

Employee Length vs Application Count (bar chart)

📌 Summary Dashboard
Loan Quality Split:

✅ Good Loans Issued: % and amounts (green gauge)

❌ Bad Loans Issued: % and amounts (red gauge)

Additional Metrics:

Application Status (Fully Paid, Charged-off, Current)

Funded vs Received Amount

Interest Rate and DTI grouped comparisons

Filters:

Interactive slicers for Grade and Purpose

🔍 Key Insights
✅ 85.88% of applications resulted in good loans

❌ 14.12% are bad loans, with specific patterns across purpose and geography

💳 Top purpose: Credit card loans (5,000+ applications)

🗺️ High application states: California, Texas, Florida

📅 Peak month: December (4.3K applications submitted)


🧰 Tools & Skills Used
Tool	Purpose
SQL	Data validation, metric accuracy
Excel	Data cleaning, dashboard building
Formulas	SUMIFS, VLOOKUP, IF, DATEDIF, etc.
Slicers	Interactive filtering
Charts	Line, Bar, Donut, Tree Map, Maps

👤 Author
Sourabh Yadav
Data Analyst | Excel + SQL Enthusiast | Turning raw data into decision-ready visuals

🔗 Let’s Connect
📬 Reach out via LinkedIn or check out more of my work on GitHub!
Questions or feedback are always welcome.

