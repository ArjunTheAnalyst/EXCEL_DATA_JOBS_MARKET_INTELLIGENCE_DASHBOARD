# 📊 Data Jobs Market Intelligence Dashboard

## Overview

The Data Jobs Market Intelligence Dashboard is an end-to-end Business Intelligence project built in Microsoft Excel to analyze salary trends, skill demand, and compensation patterns across data-related careers.

The project leverages Power Query for ETL and data transformation, Power Pivot for relational data modeling, DAX for advanced calculations, and interactive dashboards for business insights.

This project demonstrates the complete BI workflow from raw data preparation to actionable business insights.

---

## 🎯 Business Problem

The data job market is highly competitive and continuously evolving. Professionals often face challenges in identifying:

- Which data roles offer the highest salaries
- Which technical skills are most in demand
- Which skills command premium compensation
- Whether acquiring more skills leads to better pay
- How salaries vary across job titles and countries

This dashboard addresses these questions through data-driven analysis of job posting data.

---

## 🛠️ Tools & Technologies

| Category | Technology |
|-----------|------------|
| Data Cleaning | Power Query |
| Data Modeling | Power Pivot |
| Calculations | DAX |
| Dashboarding | Microsoft Excel |
| Visualization | Pivot Charts |
| Interactive Filtering | Slicers |
| Analysis | Pivot Tables |

---

# 🔄 Project Workflow

```text
Raw Job Posting Dataset
            │
            ▼
     Power Query ETL
            │
            ▼
      Data Modeling
      (Power Pivot)
            │
            ▼
       DAX Measures
            │
            ▼
 Interactive Dashboard
            │
            ▼
      Business Insights
```

---

# 📥 Data Preparation & ETL

The raw dataset required extensive transformation before analysis.

### Transformations Performed

- Promoted Headers
- Corrected Data Types
- Renamed Columns
- Created Date Fields
- Created Month Fields
- Added Index Column
- Removed Unnecessary Columns
- Standardized Skill Names
- Cleaned Text Fields
- Created Reference Tables
- Prepared Data for Modeling

---

## Power Query Workflow

### Power Query - Jobs Dataset

![Power Query Jobs Dataset](images/power-query-jobs.png)

**Highlights**
- Cleaned and transformed the primary jobs dataset
- Created additional date fields for reporting
- Optimized data structure for analysis

---

### Power Query - Skills Dataset

![Power Query Skills Dataset](images/power-query-skills.png)

**Highlights**
- Split multi-value skill fields
- Unpivoted skill columns
- Standardized skill naming conventions
- Built a normalized skills table for analysis

---

# 🧩 Data Modeling

A relational data model was created using Power Pivot.

### Model Structure

| Table | Description |
|---------|------------|
| data_jobs_all | Main jobs dataset containing salary and job information |
| data_job_skills | Normalized skill dataset containing one record per skill |

### Relationship Design

A one-to-many relationship was established using **Job ID**.

```text
data_jobs_all (1)
        │
        │ Job ID
        ▼
data_job_skills (*)
```

This model enables:

- Cross-table filtering
- Skill-level analysis
- Dynamic aggregations
- Better scalability and maintainability

---

## Power Pivot Data Model

![Power Pivot Data Model](images/data-model.png)

---

# 📐 DAX Measures

Custom measures were created to support dynamic reporting and KPI calculations.

### Key Measures

#### Median Salary

Used throughout the dashboard to compare compensation across:

- Job Titles
- Countries
- Skills

#### Skill Count

Calculates the average number of skills associated with job postings.

#### Skill Likelihood

Measures how frequently a skill appears across job postings.

#### Job Count by Title

Calculates the volume of postings by role.

#### Salary Comparison Metrics

Used to compare compensation across regions and job categories.

---

# 📊 Dashboard Analysis

---

## 1. Salary vs Skills Analysis

### Business Question

> Do more skills equate to better pay?

This analysis compares median salary against the average number of skills required for each role.

### Key Insights

- Senior Data Engineer roles require the highest average skill count.
- Data Engineering positions command strong salaries.
- There is a positive relationship between skill requirements and compensation.

### Dashboard View

![Salary vs Skills Analysis](images/salary-vs-skills.png)

---

## 2. Salary Analysis

### Business Question

> How do salaries compare across job roles and regions?

This dashboard compares median salaries across:

- Job Titles
- Countries
- US vs Non-US Markets

### Key Insights

- Senior-level positions consistently command premium salaries.
- Geographic location significantly impacts compensation.
- Data Engineers and Data Scientists remain among the highest-paid roles.

### Dashboard View

![Salary Analysis](images/salary-analysis.png)

---

## 3. Skill Job Analysis

### Business Question

> What are the most requested skills in the data industry?

This analysis measures skill demand across job postings.

### Top Skills Identified

- SQL
- Excel
- Tableau
- Python
- SAS
- Power BI
- R

### Key Insights

- SQL remains the most requested skill.
- Excel continues to be highly relevant in the market.
- Visualization tools remain critical across multiple roles.

### Dashboard View

![Skill Job Analysis](images/skill-job-analysis.png)

---

## 4. Skill Salary Analysis

### Business Question

> Which skills provide the highest earning potential?

This dashboard combines salary data with skill demand metrics.

### Key Insights

- Python and Tableau are associated with strong compensation.
- SQL combines high demand with competitive salaries.
- Some niche skills command premium salaries despite lower demand.

### Dashboard View

![Skill Salary Analysis](images/skill-salary-analysis.png)

---

# 💡 Key Findings

### Salary Insights

- Senior Data Scientist and Senior Data Engineer roles offer the highest median salaries.
- Compensation varies significantly by geography.
- Technical specialization generally leads to higher earnings.

### Skill Demand Insights

- SQL is the most requested skill in data-related jobs.
- Python remains one of the most valuable technical skills.
- Business intelligence tools continue to be highly relevant.

### Career Insights

- Combining technical and analytical skills improves employability.
- Professionals with broader skillsets generally command higher salaries.
- Demand remains strong across analytics, engineering, and data science roles.

---

# 🚀 Skills Demonstrated

### Data Engineering & Preparation

- Data Cleaning
- ETL Development
- Data Transformation
- Data Normalization

### Business Intelligence

- Power Query
- Power Pivot
- DAX
- Data Modeling
- Relationship Design
- Cardinality Management

### Analytics

- Exploratory Data Analysis
- Salary Analysis
- Skill Demand Analysis
- Workforce Analytics

### Visualization

- Dashboard Design
- Interactive Reporting
- KPI Development
- Data Storytelling

---

# 📂 Repository Structure

```text
data-jobs-market-intelligence-dashboard/
│
├── README.md
├── Data_Jobs_Market_Intelligence_Dashboard.xlsx
│
├── images/
│   ├── power-query-jobs.png
│   ├── power-query-skills.png
│   ├── data-model.png
│   ├── salary-vs-skills.png
│   ├── salary-analysis.png
│   ├── skill-job-analysis.png
│   └── skill-salary-analysis.png


│
└── dataset/
    └── data_jobs.csv
```

---

## 🎓 Key Learnings

Through this project, I gained hands-on experience in:

- Building scalable data models using Power Pivot
- Managing one-to-many relationships and cardinality
- Designing efficient ETL workflows in Power Query
- Developing DAX measures for analytical reporting
- Creating interactive dashboards for decision-making
- Translating raw data into actionable business insights

This project strengthened my understanding of the complete Business Intelligence workflow and reinforced best practices in data preparation, modeling, and visualization.
