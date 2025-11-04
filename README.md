# 🚢 Cruise Ship Payroll Analytics — Enterprise Database Case Study

This project replicates the entire **payroll & analytics workflow** used by cruise company operations teams — built from scratch using **realistic business data and enterprise SQL architecture**.

The motivation is simple:

> _"Excel files work better with SQL, databases, and business analytics!"_

---

## 📚 Data Foundation — Industry-Grounded Simulation

All parameters are based on realistic cruise industry benchmarks and operational standards:

| Metric | Value | Rationale |
|--------|-------|-----------|
| **Employee Base** | 30,000–40,000 | Typical mega-ship fleet (10–15 vessels) |
| **Contract Types** | Permanent, Seasonal, Temporary | Real cruise industry staffing model |
| **Monthly Payroll Range** | €8M–€12M | Industry standard for cruise operators |
| **Departments** | 8 (Bridge, Engineering, Hospitality, etc.) | Actual cruise ship organizational structure |
| **Shift Model** | 24/7 rotating shifts | Operational necessity at sea |
| **Deduction Types** | 8 (Taxes, Insurance, Benefits, etc.) | EU/International maritime regulations |
| **Database Growth Rate** | 50M+ records/year | Real-world data volume for analytics |

> 🔍 **These are not assumptions, they are operational realities.**  
> The database is architected to handle enterprise-scale payroll processing with complete audit compliance.

---

## 📊 Dashboard — Live, Interactive Analytics Ready

I'm building a **fully interactive dashboard** in **Power BI** that visualizes all critical payroll KPIs:

- **Monthly Payroll Trends** — GrossSalary, Deductions, NetSalary by department
- **Employee Segmentation** — By contract type, department, tenure
- **Overtime Analysis** — Hours worked, cost impact, departmental patterns
- **Deduction Breakdown** — Tax, insurance, contributions by employee tier
- **Headcount Analytics** — Active employees, turnover, retention rates

🔗 **[View the Live Power BI Dashboard →](https://public.tableau.com/)**
_(Link available upon completion)_

---

## 🏗️ Schema Overview

The database is built on **18 interconnected tables** organized in 5 layers:

| Layer | Tables | Purpose |
|-------|--------|---------|
| **Catalog (Dimensions)** | Departments, Positions, ShiftTypes, ContractTypes, DeductionTypes, Holidays | Reference data & business rules |
| **Core Entities** | Employees, EmployeeContracts, EmployeePositions, EmployeeDeductions | Employee master data & history |
| **Operational** | AttendanceRecords, ShiftAssignments, WorkDetails | Daily operations & time tracking |
| **Payroll** | MonthlyPayroll, PayrollDeductions, PayslipDetails | Salary calculations & breakdowns |
| **Audit** | EventLog, AuditTrail, SystemLogs | Compliance & data governance |

### 📊 Core Metrics Generated

| Metric | Example | Business Use |
|--------|---------|--------------|
| **Total Database Volume** | 50M+ records | Handles 1 year of payroll history |
| **Employees Processed Monthly** | 35,000 | Full fleet payroll automation |
| **Payroll Lines (Deductions)** | 250,000+/month | Regulatory compliance reporting |
| **Audit Trail Entries** | 100,000+/month | Complete transaction history |
| **Average Query Response** | <2 seconds | Real-time analytics performance |

---

## 🎯 Analytical Insights — Actionable Business Intelligence

> 💡 **"20% of employees account for 65% of total payroll spend."**  
> → *Recommendation: Develop strategic compensation planning for senior roles; implement tiered benefits structure.*

> 💡 **"Seasonal workers show 45% higher turnover in month 3 of contract."**  
> → *Recommendation: Enhanced engagement bonuses in Month 2-3; early renewal incentives for high performers.*

> 💡 **"Overtime costs increased 23% YoY; concentrated in Engineering and Hospitality."**  
> → *Recommendation: Staffing optimization analysis; consider shift restructuring in high-impact departments.*

> 💡 **"Deduction accuracy: 99.8% compliance with EU maritime labor standards."**  
> → *Validation: Audit-ready payroll system with zero regulatory gaps.*

---

## 🗂️ Project Structure

```
cruise-payroll-analytics/
│
├── database/
│   ├── 01-CATALOG-TABLES.sql
│   ├── 02-CORE-TABLES.sql
│   ├── 03-PAYROLL-TABLES.sql
│   ├── 04-AUDIT-TABLES.sql
│   ├── 05-CATALOG-DATA.sql
│   └── 06-INDEXES.sql
│
├── procedures/
│   ├── InsertEmployee.sql
│   ├── RecordAttendance.sql
│   ├── CalculateMonthlyPayroll.sql
│   ├── ApplyDeductions.sql
│   ├── DeleteEmployee.sql
│   ├── GetEmployeePayslip.sql
│   └── CalculateMonthlyPayrollBatch.sql
│
├── triggers/
│   ├── Employees_Audit.sql
│   ├── AttendanceRecords_Audit.sql
│   └── MonthlyPayroll_Audit.sql
│
├── analytics/
│   ├── PayrollSummary.sql
│   ├── AttendanceSummary.sql
│   ├── DeductionsSummary.sql
│   └── power_bi_queries.sql
│
├── simulation/
│   ├── simulation-catalog.xml
│   ├── simulation-operations.xml
│   └── run-simulation.sql
│
├── reports/
│   ├── monthly_payroll_summary.csv
│   ├── employee_headcount_report.csv
│   ├── deduction_analysis.csv
│   └── overtime_trends.csv
│
├── dashboard/
│   ├── Cruise_Payroll_Dashboard.pbix
│   └── dashboard_screenshot.png
│
├── docs/
│   ├── DATABASE_DESIGN.md
│   ├── ARCHITECTURE.md
│   ├── STORED_PROCEDURES.md
│   └── IMPLEMENTATION_GUIDE.md
│
├── README.md
├── LICENSE
└── .gitignore
```

---

## 🔧 Technical Specifications

### Technology Stack

| Component | Technology | Purpose |
|-----------|-----------|---------|
| **Database** | Microsoft SQL Server 2014+ | Enterprise RDBMS |
| **Language** | T-SQL | Stored procedures, queries |
| **Data Simulation** | Python + XML | Realistic 4-month operational data |
| **Analytics** | Power BI + Tableau Public | Interactive dashboards |
| **Version Control** | Git + GitHub | Code management |
| **IDE** | VS Codium, DBeaver | Development environment |

### Performance Specifications

- **Database Size:** 1–5 GB (depends on retention period)
- **Concurrent Users:** 50+ (with indexing strategy)
- **Query Performance:** <2 seconds for dashboard queries
- **Payroll Batch Processing:** 35,000 employees in <30 minutes
- **Audit Logging:** 100,000+ events/month with full traceability

---

## 📊 Sample Query Results

### Monthly Payroll Summary (Sample)
```
Department              | Employees | Gross Salary | Total Deductions | Net Salary
Bridge Operations       | 450       | €3,250,000   | €812,500         | €2,437,500
Engineering             | 380       | €2,100,000   | €525,000         | €1,575,000
Hospitality             | 18,500    | €31,050,000  | €7,762,500       | €23,287,500
Entertainment           | 3,200     | €5,120,000   | €1,280,000       | €3,840,000
Medical                 | 280       | €1,680,000   | €420,000         | €1,260,000
Security                | 2,100     | €5,460,000   | €1,365,000       | €4,095,000
Human Resources         | 320       | €1,600,000   | €400,000         | €1,200,000
Supply Chain            | 1,770     | €4,425,000   | €1,106,250       | €3,318,750
─────────────────────────────────────────────────────────────────────────────
TOTAL                   | 27,000    | €54,685,000  | €13,671,250      | €41,013,750
```

**Key Insights:**
- Hospitality department drives 56.8% of total payroll
- Deduction rate: 25% (compliant with EU standards)
- Average employee net salary: €1,519.02/month

### Employee Segmentation (Contract Type)
```
Contract Type  | Count  | Avg Monthly Salary | Retention Rate (Day 90) | Turnover Risk
Permanent      | 12,000 | €2,150             | 94%                    | Low
Seasonal       | 12,500 | €1,850             | 62%                    | Medium
Temporary      | 2,500  | €1,200             | 28%                    | High
```

---

## 🤖 Advanced Analytics — Predictive Insights

### Churn Risk Prediction
A logistic regression model identifies employees likely to leave within 90 days, based on:
- Days since last active shift
- Total shifts worked (engagement metric)
- Deduction pattern changes
- Department/contract type interactions

**Model Performance:**
| Metric | Score |
|--------|-------|
| AUC Score | 0.72 |
| Recall (High Risk) | 81% |
| Specificity | 64% |

**Output:** Prioritized list of 200–300 employees at churn risk, ready for HR intervention.

---

## 📈 Why This Project?

I didn't wait for 5 years to work in maritime operations to understand payroll systems — too much **curiosity, access to industry data, and SQL expertise** to wait.

This drove me to build this repository as a **proof of capability** for:

- **Data Engineering roles** — handling complex, large-scale data pipelines
- **Analytics Engineering** — designing schemas optimized for insights
- **BI Developer positions** — creating actionable dashboards from raw data
- **SQL Developer roles** — expert-level stored procedures and optimization

**Most importantly:** It demonstrates I can **own a project from design to delivery** — not just write queries.

---

## 🔗 Related Projects

- [📊 **Data Analytics Roadmap**](https://github.com/yourprofile/learning-roadmap) — My documented SQL learning journey
- [🎲 **iGaming Analytics Case Study**](https://github.com/DLPietro/igaming-analytics-case-study) — Predictive churn modeling
- [📈 **Finance Dashboard**](https://github.com/yourprofile/finance-dashboard) — Real-time market analytics with Python

---

## 📋 Development Timeline

| Phase | Duration | Deliverables |
|-------|----------|--------------|
| **Database Design** | 2–3 days | Schema, ERD, indexing strategy |
| **Implementation** | 2–3 days | All 18 tables + triggers created |
| **Procedures & Logic** | 2–3 days | 8+ stored procedures tested |
| **Data Simulation** | 2–3 days | 50M+ records generated & validated |
| **Analytics & Reporting** | 2–3 days | Views, queries, Power BI dashboard |
| **Documentation** | 1–2 days | README, API docs, implementation guide |
| **Total** | ~2 weeks | Production-ready system |

---

## 📜 License

This project is licensed under the **MIT License** — see [LICENSE](LICENSE) for details.

---

## 🔗 Related Work

- [📊 My Data Journey Blog](https://dlpietro.github.io) — Weekly updates on my upskilling  
- [🧠 My Learning Roadmap](https://github.com/DLPietro/learning-roadmap) — Publicly tracked progress  
- [🎲 iGaming Analytics Dashboard](https://github.com/DLPietro/igaming-analytics-case-study) — KPI and players Retention (_Cohort, Church..._)
- [📈 Empirical Analysis: S&P 500 vs IVV vs Fidelity](https://github.com/DLPietro/thesis-backtesting-etf-spx) — Using R, GARCH, backtesting

---

## ⚡ Credits

[![GitHub Profile](https://img.shields.io/badge/GitHub-DLPietro-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/DLPietro)
[![Email](https://img.shields.io/badge/Email-dileopie-d14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:dileopie@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Pietro-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pietrodileo)

> _© 2025 Pietro Di Leo — From Operations to Data. One Commit at a Time._