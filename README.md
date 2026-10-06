# Employee Attrition Analysis Dashboard

An Excel-based analytics project that explores **why employees leave** an organization. It uses a dataset of ~74,500 employee records, a set of business questions, headline KPIs, pivot-table charts and an interactive dashboard with slicers.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [Workbook Structure](#workbook-structure)
4. [Dataset Description](#dataset-description)
5. [Key KPIs](#key-kpis)
6. [Business Questions Answered](#business-questions-answered)
7. [Charts & Visualizations](#charts--visualizations)
8. [Dashboard & Slicers](#dashboard--slicers)
9. [How to Use](#how-to-use)
10. [Tools & Techniques](#tools--techniques)
11. [Data Notes](#data-notes)
12. [Possible Next Steps](#possible-next-steps)

---

## Project Overview

Employee attrition is costly: lost knowledge, recruitment and onboarding expenses, and lower team morale. This project analyses employee data to identify **which factors are most associated with attrition** (age, role, overtime, pay, work-life balance, satisfaction, tenure, etc.) so HR and leadership can target retention efforts.

- **File:** `Emp_attrition.xlsx`
- **Records:** 74,498 employees
- **Features:** 26 columns (demographic, job, compensation, environment and satisfaction attributes)
- **Target variable:** `Attrition` (Stayed / Left) with numeric `Attrition Flag` (0 = Stayed, 1 = Left)

## Objectives

- Measure the overall attrition rate and its split across key segments.
- Compare attrition across demographics, job roles/levels, compensation, work environment and satisfaction.
- Identify high-risk groups (e.g., overtime workers, specific roles or age bands).
- Deliver an interactive dashboard that lets stakeholders filter and explore the data themselves.

## Workbook Structure

| Sheet | Purpose |
|---|---|
| `Emp_attrition_csv` | Raw dataset (74,498 rows × 26 columns) |
| `QUESTIONS` | The 23 business questions that guide the analysis, grouped by theme |
| `KPI` | Headline KPIs and the list of dashboard slicers |
| `CHARTS` | Pivot tables and pivot charts (13 major charts) |
| `DASHBOARD` | Final dashboard combining KPIs, charts and slicers |

## Dataset Description

| Category | Columns |
|---|---|
| **Identifier** | `Employee ID` |
| **Demographics** | `Age`, `AGE GROUP` (<25, 25-35, 35-45, 45-55, 55+), `Gender`, `Marital Status`, `Number of Dependents`, `Education Level` |
| **Job & Company** | `Job Role` (Education, Technology, Finance, Healthcare, Media), `Job Level` (Entry, Mid, Senior), `Company Size` (Small, Medium, Large), `Years at Company`, `Company Tenure (In Months)` |
| **Compensation & Growth** | `Monthly Income`, `Number of Promotions`, `Leadership Opportunities`, `Innovation Opportunities` |
| **Work Environment** | `Overtime`, `Remote Work`, `Distance from Home`, `Work-Life Balance` (Poor/Fair/Good/Excellent) |
| **Satisfaction & Perception** | `Job Satisfaction`, `Performance Rating`, `Employee Recognition`, `Company Reputation` |
| **Target** | `Attrition` (Stayed/Left), `Attrition Flag` (0/1) |

The dataset has **no missing values**.

## Key KPIs

| KPI | Value |
|---|---|
| Overall attrition rate | ~47.5% |
| Total employees | ~74,498 |
| Total attrition (employees who left) | 35,361 |
| Avg. monthly income: Left vs Stayed | 7,318 vs 7,368 |
| Avg. tenure (months) | ~55.7 |
| Attrition rate among overtime employees | ~51.5% |
| Avg. years at company | ~15.7 |
| Avg. work-life balance | included as a KPI card |

> **Attrition rate** = average of `Attrition Flag` (employees who left ÷ total employees).

## Business Questions Answered

The `QUESTIONS` sheet organises the analysis into themes:

- **Demographics** – overall rate, age group, gender, marital status
- **Job & Department** – job role, job level, company size
- **Compensation & Growth** – income vs attrition, number of promotions, promotions for employees with 3+ years' service
- **Work Environment** – overtime, work-life balance, remote work, leadership & innovation opportunities
- **Satisfaction & Recognition** – job satisfaction, recognition level, company reputation
- **Tenure & Personal Factors** – attrition trend by tenure, distance from home, number of dependents
- **Contribution analysis** – share of total attrition by job role, age group and work-life balance category

## Charts & Visualizations

The `CHARTS` sheet contains pivot tables and pivot charts for:

1. Attrition rate by job role
2. Attrition rate by age group
3. Attrition rate by overtime status
4. Average monthly income: left vs stayed
5. Attrition trend over company tenure
6. Attrition rate by work-life balance rating
7. Attrition rate by gender
8. Attrition rate by marital status
9. Attrition rate by job level
10. Attrition rate by number of promotions
11. Attrition rate by job satisfaction
12. Attrition rate by remote work status
13. Job role × gender attrition heatmap

## Dashboard & Slicers

The `DASHBOARD` sheet brings the KPIs and charts together. The following slicers allow interactive filtering:

- Attrition (Yes / No)
- Job Role
- Age Group
- Gender
- Overtime
- Remote Work Status

## How to Use

1. Open `Emp_attrition.xlsx` in **Microsoft Excel** (desktop version recommended, since slicers and pivot charts are used).
2. Go to the **DASHBOARD** sheet and use the slicers to filter the view.
3. Review the **KPI** and **CHARTS** sheets for detail, and the **QUESTIONS** sheet for the analysis scope.
4. If the raw data changes, go to **Data → Refresh All** to update the pivot tables and charts.

## Tools & Techniques

- Microsoft Excel
- Pivot tables and pivot charts
- Slicers for interactive filtering
- Calculated KPIs (averages, counts, rates)
- Conditional formatting (heatmap)

## Data Notes

- The `KPI` sheet shows total employees as 74,499 while the dataset contains 74,498 records (likely a count that included the header row). As a result, the KPI attrition rate (47.4651%) differs very slightly from the rate computed on the data itself (47.4657%). The difference is negligible but worth fixing for consistency.
- Some column values are synthetic-looking (e.g., `Years at Company` can exceed what would be expected for a given `Age`), so treat results as exploratory rather than as conclusions about a real organization.
- `Monthly Income` contains a few high outliers (max ≈ 50,030 vs. median ≈ 7,349).

## Possible Next Steps

- Build a predictive model (logistic regression, random forest, XGBoost) to estimate attrition risk per employee.
- Run statistical tests (chi-square, t-tests) to confirm which differences are significant.
- Add cost-of-attrition estimates to quantify business impact.
- Recreate the dashboard in Power BI or Tableau for easier sharing.
- Add a short "Key Insights & Recommendations" section once the final findings are confirmed.

---

*Project: Employee Attrition Analysis | Tool: Microsoft Excel*
