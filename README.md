# Wema Bank Plc HR Analytics Dashboard Project

An Excel-based HR Analytics case study analyzing workforce distribution, employee engagement, performance, satisfaction, and training effectiveness across Wema Bank Plc, using interactive dashboards, PivotTables, KPI cards, and data visualization techniques.

## Table of Contents

- [Dashboard Preview](#dashboard-preview)
- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Project Objectives](#project-objectives)
- [Dataset Information](#dataset-information)
- [Tools & Technologies Used](#tools--technologies-used)
- [Data Cleaning Process](#data-cleaning-process)
- [New Calculated Columns](#new-calculated-columns)
- [Data Analysis Process](#data-analysis-process)
- [Pivot Table Analysis](#pivot-table-analysis)
- [Dashboard Development](#dashboard-development)
- [Key Insights](#key-insights)
- [Business Recommendations](#business-recommendations)
- [Challenges Encountered](#challenges-encountered)
- [Conclusion](#conclusion)
- [Author Information](#author-information)

---

## Dashboard Preview

### 1. Workforce Overview Dashboard
<img width="1097" height="668" alt="HR final dash1" src="https://github.com/user-attachments/assets/bca42689-fc53-46da-85db-a3d0fed121ec" />


### 2. Employee Performance & Engagement Dashboard
<img width="976" height="670" alt="HR final dash2" src="https://github.com/user-attachments/assets/89067b69-6119-4ac1-934f-23c84f57b4b9" />


### 3. Training & HR Investment Dashboard
<img width="1003" height="661" alt="HR final dash3" src="https://github.com/user-attachments/assets/76d6d137-80a9-47d1-98f3-a28b77298261" />


---

## Project Overview

This project was completed as part of the **30 Days Data Analytics Challenge – Week 1**, an HR Analytics business case study. It focuses on analyzing workforce performance, employee engagement, satisfaction, and training effectiveness at Wema Bank Plc using Microsoft Excel.

The analysis was carried out using PivotTables, PivotCharts, KPI cards, conditional formatting, interactive slicers, and dashboard design techniques, transforming raw HR data into three professional dashboards suitable for management decision-making.

---

## Business Problem

A multinational company — represented in this case study by Wema Bank Plc — was experiencing challenges monitoring employee performance, workforce engagement, employee satisfaction, and training effectiveness across its departments. Without reliable HR analytics:

- Employee dissatisfaction could go unnoticed.
- High-performing and low-performing departments could not be identified quickly.
- Training investments could fail to deliver measurable value.
- Workforce productivity could decline over time without warning.
- HR decisions risked relying on assumptions rather than data.

The HR management team needed data-driven insights to improve workforce productivity, employee development, and overall organizational performance.

---

## Project Objectives

- Clean and prepare the HR dataset for analysis.
- Analyze workforce distribution across departments and business units.
- Monitor employee performance and engagement levels.
- Evaluate employee satisfaction and work-life balance.
- Measure training effectiveness and HR investment performance.
- Build three professional, interactive Excel dashboards with KPI cards, charts, and slicers.
- Present clear business insights and HR recommendations for management.

---

## Dataset Information

- **Source:** HR records from Wema Bank Plc
- **Original row count:** 2,845
- **Final cleaned row count:** 2,845 (no records removed)
- **Date range:** 2022 – 2023

**Columns include:**
Employee ID, Department Type, Division, Gender Code, Performance Score, Engagement Score, Satisfaction Score, Work-Life Balance Score, Training Outcome, Training Date, Training Type, Training Program Name, Training Duration (Days), Training Cost, Age, and more.

**Raw Dataset**
<img width="1895" height="782" alt="HR_raw_data" src="https://github.com/user-attachments/assets/a6a6719e-9718-43f3-b919-86e0347af7f1" />

**Clean Dataset**
<img width="1907" height="815" alt="HR_clean_data" src="https://github.com/user-attachments/assets/5649fcc5-dc40-4c9f-8edf-a5479d608db3" />




---

## Tools & Technologies Used

| Tool | Purpose |
|---|---|
| Microsoft Excel | Data Cleaning & Analysis |
| Pivot Tables | Data Aggregation |
| Pivot Charts | Visualization |
| KPI Cards | Performance Tracking |
| Slicers | Filtering |
| Dashboard Design | Reporting |

---

## Data Cleaning Process

- **Duplicate Check:** The dataset was checked for duplicate records using Employee ID — no duplicates were found.
- **Missing Values:** The dataset was reviewed for blank or missing entries — no missing values were detected across any column.
- **Text Standardization:** All text columns were standardized using the `=PROPER()` function for consistent capitalization and the `=TRIM()` function to remove extra leading/trailing spaces.

Because the dataset arrived clean, no rows were removed during this process, keeping the final row count identical to the original (2,845).

---

## New Calculated Columns

Several additional columns were created to support deeper HR analysis:

**Age Group**
Created using an `=IF()` statement to categorize employees into age bands for workforce demographic analysis. Categories: Young Adults, Adults, Middle Age, Old.

**Tenure**
Calculated using an IF-based formula referencing each employee's start date to determine years of service at Wema Bank Plc, used to assess workforce experience levels and retention.

**Engagement Level**
Built using a nested IF statement that grouped engagement scores into Low, Medium, and High engagement bands, helping flag departments with a higher concentration of low-engagement staff.

**Satisfaction Level**
Built using a nested IF statement that grouped satisfaction scores into Low, Moderate, and High satisfaction bands, giving a quick read on employee morale across the organization.

**Performance Category**
Built using a nested IF statement that grouped performance ratings into Low Performer, Average Performer, and High Performer bands, making it easier to compare performance trends across departments.

**Training Efficiency**
Built using an IF-based formula comparing each employee's training outcome against their performance indicators, used to flag whether training investment was translating into measurable performance improvement.

---

## Data Analysis Process

The analysis was structured around the three required dashboard areas:

- **Workforce composition** was analyzed by aggregating employee counts by department, business unit, gender, and age group to understand overall organizational structure.
- **Performance and engagement** were analyzed by grouping performance, engagement, satisfaction, and work-life balance scores by department and division, identifying where morale and output were strongest or weakest.
- **Training and HR investment** were analyzed by aggregating training cost, completion rate, and outcomes by department and training program, evaluating whether HR spending was translating into successful training outcomes.

All calculations were built using PivotTables and validated against the KPI cards displayed on each dashboard.

---

## Pivot Table Analysis

The following PivotTables were built in Excel to support the three dashboards:

**Workforce Overview**
| PivotTable | Row Field | Value Field |
|---|---|---|
| Total Employees | — | Count of Employee ID |
| Average Employee Age | — | Average of Age |
| Male / Female Employees | Gender | Count of Employee ID |
| Average Tenure | — | Average of Tenure |
| Employee Count by Department | Department | Count of Employee ID |
| Gender Distribution | Gender | Count of Employee ID |
| Employee Count by Business Unit | Business Unit | Count of Employee ID |
| Workforce Distribution by Age Group | Age Group | Count of Employee ID |

<img width="1871" height="707" alt="HR_pivot1" src="https://github.com/user-attachments/assets/84ca892a-1a2c-4018-b732-106dd4bb5c35" />


**Performance & Engagement**
| PivotTable | Row Field | Value Field |
|---|---|---|
| Average Engagement / Satisfaction / Work-Life Balance / Employee Rating | — | Average of respective score |
| High Performer Count | Performance Category | Count of Employee ID |
| Performance Score by Department | Department | Count of Performance Score |
| Engagement Level Distribution | Engagement Level | Count of Employee ID |
| Top 5 Satisfaction Score by Division | Division | Count of Satisfaction Score |
| Top Performing Departments | Department | Count of Employee ID |

<img width="1478" height="667" alt="HR_pivot2" src="https://github.com/user-attachments/assets/d53ec372-3444-490b-aa26-00a2b689c8e6" />
<img width="1333" height="728" alt="HR_pivot3" src="https://github.com/user-attachments/assets/7b3c01d6-e870-4fe5-93ac-f46dfbcefc76" />



**Training & HR Investment**
| PivotTable | Row Field | Value Field |
|---|---|---|
| Total Training Programs | Training Program Name | Distinct Count |
| Total Training Cost | — | Sum of Training Cost |
| Training Completion Rate | Department | Sum of Completed ÷ Count of Employee ID |
| Average Training Duration | — | Average of Training Duration (Days) |
| Successful Training Count | Training Outcome | Count of Employee ID |
| Training Programme Attendance | Training Program Name | Count of Employee ID |
| Training Cost by Department | Department | Sum of Training Cost |
| Training Outcome Analysis | Training Outcome | Count of Employee ID |

<img width="1212" height="715" alt="HR_pivot4" src="https://github.com/user-attachments/assets/27918c4c-e77d-441a-9956-47a7fde661f2" />
<img width="1167" height="656" alt="HR_5" src="https://github.com/user-attachments/assets/20588e3a-edd8-4847-8a5e-7a1d6ca00e88" />



---

## Dashboard Development

Three dashboards were built, each with its own KPI cards, charts, and slicer, in a consistent Wema Bank–themed design.

### 1. Workforce Overview Dashboard
**KPIs:** Total Employees (2,845), Average Employee Age (49), Female Employees (1,588), Male Employees (1,257), Average Tenure (5 Years)
**Charts:** Employee Count by Department, Gender Distribution, Workforce Distribution by Age Group, Employee Count by Business Unit
**Slicer:** Department

### 2. Employee Performance & Engagement Dashboard
**KPIs:** Average Engagement Score (2.9), Average Satisfaction Score (3.1), Average Work-Life Balance Score (2.8), Average Employee Rating (3.0), High Performer Count (70)
**Charts:** Performance Score by Department, Engagement Level Distribution, Top 5 Satisfaction Score by Division, Top Performing Departments
**Slicer:** Business Unit

### 3. Training & HR Investment Dashboard
**KPIs:** Total Training Cost ($1,591,148.63), Total Training Programs (5), Training Completion Rate (50.8%), Average Training Duration (3.0 days), Successful Training Count (709)
**Charts:** Training Programme Attendance, Training Type Performance, Training Outcome Analysis, Training Cost by Department
**Slicer:** Training Program Name

<img width="1097" height="668" alt="HR final dash1" src="https://github.com/user-attachments/assets/bca42689-fc53-46da-85db-a3d0fed121ec" />
<img width="976" height="670" alt="HR final dash2" src="https://github.com/user-attachments/assets/89067b69-6119-4ac1-934f-23c84f57b4b9" />
<img width="1003" height="661" alt="HR final dash3" src="https://github.com/user-attachments/assets/76d6d137-80a9-47d1-98f3-a28b77298261" />

---

## Key Insights

**Workforce Composition**
1. Wema Bank Plc employs **2,845 people** across 6 departments, with an average employee age of **49** and an average tenure of **5 years**.
2. The workforce skews female, with **1,588 female employees (56%)** versus **1,257 male employees (44%)**.
3. **Production** is by far the largest department, accounting for **1,910 employees (67% of the entire workforce)** - every other department combined makes up less than a third of staff.
4. Age distribution skews older: **34% of employees fall in the "Old" age group**, followed by Adult (24%), Middle Age (23%), and Young Adult (18%).
5. Business unit distribution is unusually even - each of the 10 business units holds roughly **281–291 employees**, suggesting workforce allocation across units is deliberately balanced.

**Performance & Engagement**

6. Average engagement score sits at **2.9**, average satisfaction at **3.0**, and average work-life balance at **2.99** - all landing in a middle-of-scale range rather than strongly positive.
7. Engagement is a concern area: **43% of employees fall into the "Low Engagement" band**, compared to 40% Medium and only 17% High - meaning fewer than 1 in 5 employees are highly engaged.
8. Only **70 employees are classified as High Performers** company-wide, a small fraction of the 2,845-person workforce.
9. **Field Operations** leads all divisions in satisfaction score, well ahead of General Operations, Engineers, and other divisions.

**Training & HR Investment**

10. Wema Bank invested **$1,591,148.63** in training across **5 programs**, but the **training completion rate is just 50.8%** - roughly half of enrolled training activity does not reach completion.
11. Training outcomes are mixed: **737 were marked Completed, 709 Passed, 731 Incomplete, and 668 Failed** - meaning Failed and Incomplete outcomes combined actually exceed the Completed count.
12. Training spend is heavily concentrated in **Production**, which absorbed **$1,070,266.20** - roughly **67% of the entire training budget** - proportional to its share of headcount, but still the single largest cost center by a wide margin.
13. **Communication Skills** was the most-attended training program (633 employees), followed by Project Management (585) and Leadership Development (544).

---

## Business Recommendations

**1. Address Low Engagement Before It Affects Retention**
With 43% of employees in the "Low Engagement" band, Wema Bank should investigate root causes - workload, management practices, recognition, or role clarity — starting with departments outside Production, where the bulk of the workforce is concentrated. Pulse surveys and manager check-ins in the lowest-scoring divisions would help pinpoint specific drivers.

**2. Investigate the Training Completion Gap**
A 50.8% completion rate, with failed and incomplete outcomes exceeding completed ones, suggests either program design, scheduling, or employee bandwidth issues. Before increasing the $1.59M training budget further, HR should audit why over half of training activity isn't reaching successful completion - this could free up significant budget currently being spent inefficiently.

**3. Diversify Development Beyond Production**
Since Production represents 67% of the workforce and absorbs a proportional share of training cost, smaller departments (Executive Office, Admin Offices, Software Engineering) may be underserved in training variety or frequency. A review of training equity across departments could help ensure smaller teams aren't overlooked.

**4. Study What Drives High Performance in Field Operations**
Field Operations leads all divisions in satisfaction score. Understanding what makes this division stand out - management style, workload, team structure - could offer a replicable model for improving satisfaction in lower-scoring divisions like Wireline Construction.

**5. Expand the High Performer Pipeline**
With only 70 employees classified as High Performers out of 2,845, Wema Bank has room to grow this pool. Combining performance and engagement data could help HR identify "Medium Engagement, Average Performer" employees who are close to the High Performer threshold and would benefit most from targeted coaching or stretch assignments.

**6. Monitor Workforce Age Trends**
With 34% of the workforce in the "Old" age group and an average age of 49, succession planning and knowledge transfer should be prioritized in departments with senior-heavy staffing, to reduce risk from upcoming retirements.

---

## Challenges Encountered

One notable challenge on this project was reconstructing parts of the documentation after project completion — the original notes detailing the exact score thresholds used for the Engagement Level, Satisfaction Level, and Performance Category calculated columns were lost, requiring the underlying IF-statement logic to be recalled and rebuilt from memory rather than copied directly from working notes.

Balancing the Training & HR Investment dashboard also required care, since the training outcome data was mixed - with Incomplete and Failed counts nearly matching Completed and Passed counts - making it important to present the completion rate honestly rather than only highlighting favorable numbers.

Designing three separate dashboards, each with its own KPI cards, charts, and slicer, while maintaining a consistent visual theme in line with Wema Bank Plc's branding, also required deliberate layout planning to keep each dashboard clear and readable on its own.

---

## Conclusion

This HR Analytics Dashboard Project successfully transformed raw HR data into actionable business insights for Wema Bank Plc using Microsoft Excel. The workforce is large and stable, with a slight female majority and an aging employee base, but engagement levels reveal a real area of concern, with fewer than 1 in 5 employees highly engaged. Training investment is substantial but underperforming, with just over half of training activity reaching successful completion.

The dashboards give management a clear, interactive way to monitor workforce trends, performance, and training effectiveness — and the recommendations above outline concrete next steps for improving engagement, training ROI, and workforce planning going forward.

---

## Author Information

**Abdraheem Waliu Ajekunle**
Data Analyst | Business Intelligence Enthusiast

- Microsoft Excel
- Power BI
- SQL
- Data Visualization
- Dashboard Development
- Business Analytics

### Connect With Me

[![LinkedIn](https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&style=flat)](http://www.linkedin.com/in/waliuabdraheem)
