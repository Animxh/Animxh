<div align="center">

# Animesh Sen

**Process Associate → Data Analyst · FinTech & Compliance · Guwahati, India**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-animeshsen03-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/animeshsen03)
[![GitHub](https://img.shields.io/badge/GitHub-Animxh-181717?style=flat&logo=github&logoColor=white)](https://github.com/Animxh)
[![Email](https://img.shields.io/badge/Email-sen.animesh099@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:sen.animesh099@gmail.com)
[![HackerRank](https://img.shields.io/badge/HackerRank-SQL_Gold-2EC866?style=flat&logo=hackerrank&logoColor=white)](https://www.hackerrank.com)

</div>

---

## About

I've spent four-plus years in mutual fund operations at KFIN Technologies Ltd, a SEBI-regulated RTA. KYC verifications, regulatory filings — work that looks routine from the outside but sits on top of genuinely messy, inconsistent data once you start pulling at it.

That messiness is what got me into analytics. Not a course, not a career pivot plan. Just the slow frustration of watching processes that could be automated stay manual, and reports that could answer real questions stay decorative. I started querying our data on the side. Then I started building things.

The projects here all came from something I actually wanted to understand or fix. The churn model came from asking what a BCG-style analysis would look like if I did it properly from scratch — the kind of work where you make real modelling decisions, not just run a tutorial notebook. The AML screener came from sitting with compliance & operaions work every day and thinking seriously about which parts of it an LLM could assist with. Neither project started as a portfolio item. They started as questions.

I'm now looking to move into a data or product analyst role. Four years of compliance & operations give me domain knowledge that most analytics candidates don't have. The projects show the rest.

---

## Tech

**Languages & Analysis**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=flat&logo=mysql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=flat&logo=microsoftsqlserver&logoColor=white)

**Libraries**

![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)

**Visualisation**

![Tableau](https://img.shields.io/badge/Tableau-E97627?style=flat&logo=tableau&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Excel](https://img.shields.io/badge/Excel_Advanced-217346?style=flat&logo=microsoftexcel&logoColor=white)

**Stack**

![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

**Statistical Methods**

Regression Analysis · Hypothesis Testing · KPI Development · Financial Risk Metrics (Sharpe Ratio · Volatility · ROI · Max Drawdown)

SQL specifics: CTEs, window functions, subqueries, joins across multi-table schemas. The COVID SQL project is a reasonable sample of how I actually write queries.

Excel specifics: VBA, Macros, Pivot Tables, VLOOKUP — the kind of Excel that handles real compliance reporting, not just basic formulas.

SQL specifics: CTEs, window functions, subqueries, joins across multi-table schemas. The COVID SQL project is a reasonable sample of how I actually write queries.

---

## Projects

### [PowerCo SME Churn Prediction](https://github.com/Animxh/powerco-churn-prediction)

BCG X / Forage simulation. Raw energy utility data goes in across four Jupyter notebooks; a trained churn model and an executive summary slide come out. The interesting part happened in the middle.

The dataset has a 9.7% churn rate. That sounds manageable. It isn't. A model that predicts "no churn" for every single customer scores 90.3% accuracy and catches nobody. I've seen people submit models like that in tutorial courses and call it a win. The whole modelling section here is built around not doing that: `class_weight='balanced'` on the Random Forest, evaluation anchored on recall and ROC-AUC rather than accuracy, stratified splits so both halves of the data carry the same churn proportion.

The finding I didn't expect: price variables barely matter. I went in assuming customers leave because prices went up. They don't — or not primarily. The top two features by importance were both margin-related. `net_margin_per_kwh` (importance 0.118) and `margin_gross_pow_ele` (0.106) ranked above every price variable. Low-margin customers are the ones who leave. That completely changed what the business recommendations said.

Final numbers: ROC-AUC 0.682, recall 52.9%, 14,606 customers, 29 engineered features.

`Python` `scikit-learn` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Jupyter`

---

### [AML Compliance Risk Screener](https://github.com/Animxh/compliance-risk-screener)

A Streamlit app that takes a transaction description or entity name and returns a structured risk assessment — risk tier, FIU-IND reporting obligation, applicable regulations, recommended action — with every query logged to a PostgreSQL audit table.

I built this because a large part of AML compliance work is pattern recognition, and I wanted to find out how far an LLM actually gets when you load the regulatory context properly. Further than I expected, it turns out.

The regulatory framework reads from a `regulations.json` config file at runtime and rebuilds the system prompt on every call. When SEBI issues a new circular — and they do, regularly — one JSON entry is the entire update. No code changes, no redeployment. That design came directly from watching compliance teams manually update spreadsheet lookups every time the RBI revised its KYC directions.

Coverage: PMLA 2002 (amended 2023), FEMA, RBI KYC Master Direction 2024, SEBI AML/CFT Master Circular June 2024, FATF 40 Recommendations, UN/OFAC/EU/UK sanctions lists.

`Python` `Streamlit` `Groq API (Llama 3.1)` `PostgreSQL` `SQLAlchemy`

---

### [COVID-19 SQL Exploration](https://github.com/Animxh/SqlProject)

Multi-table SQL analysis on COVID-19 data — rolling averages, death rate calculations, country-level comparisons. Queries built around window functions and CTEs, not basic SELECT statements.

`SQL` `PostgreSQL` `CTEs` `Window Functions`

---

### [COVID-19 Tableau Dashboard](https://public.tableau.com/app/profile/animesh.sen8522/viz/CovidDashboard_16795122521650/Dashboard1)

Interactive global trends dashboard across 180+ countries. The harder problem was the data itself — countries reported numbers differently, on different schedules, with different definitions of what counted as a case.

`Tableau` `Data Cleaning` `Dashboard Design`

---

## Certifications

| Certification | Issuer |
|---|---|
| Google Data Analytics Professional Certificate | Google / Coursera |
| Advanced Data Analytics | Coursera |
| Data Analysis with Microsoft Excel | Microsoft |
| BCG X Data Science Job Simulation | BCG X / Forage |
| NISM Series II-B (Investment Adviser) | SEBI / NISM |
| SQL — Gold Badge | HackerRank |

---

## GitHub Stats

<div align="center">

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Animxh&show_icons=true&theme=github_dark&hide_border=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Animxh&layout=compact&theme=github_dark&hide_border=true)

![GitHub Streak](https://streak-stats.demolab.com/?user=Animxh&theme=github-dark-blue&hide_border=true)

</div>

---

## Currently

## Currently

Actively looking for data or product analyst roles in India- anything
with serious data behind it.

The goal is not just to make the transition. It's to become genuinely good at this — the kind
of analyst who can move between a messy dataset, a business question, and a clear recommendation
without losing anything in translation. Four years inside a SEBI-regulated RTA gave me the
domain foundation. The projects above are where I'm building the technical depth to match it.


If you're reading this and have a role that fits — or just want to talk through the projects — my email is above.

---

<div align="center">

![Visitor Count](https://komarev.com/ghpvc/?username=Animxh&color=blue&style=flat&label=Profile+Views)

</div>
