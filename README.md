# Real-Estate-Sales-Analysis-Project



## 📌 Project Overview

| | |
|---|---|
| **Project Name** | Real Estate Sales Analyzing |
| **Client (Simulated)** | Municipal Planning and Zoning Board |
| **Objective** | Analyze real estate sales trends, identify top-performing towns, and compare property values & sales ratios |
| **Dataset Period** | 2011 – 2022 |
| **Tool Used** | Tableau Desktop / Public (v2026.2) |
| **File Type** | Packaged Workbook (`.twbx`) |
| **Data Source** | `Real_Estate_Sales_2011-2022_GL_1.xlsx` |

---

## 🎯 Business Problem

Over the past decade, property transactions have fluctuated significantly across towns and property types. Municipal stakeholders lacked a single, intuitive view of these patterns to guide zoning and taxation decisions. This project translates raw transaction-level data into an interactive dashboard and narrative story that non-technical stakeholders can explore independently.

---

## 🗂️ Dataset

Each record represents a single property sale, with fields including:

`Serial Number` · `List Year` · `Date Recorded` · `Town` · `Address` · `Assessed Value` · `Sale Amount` · `Sales Ratio` · `Property Type` · `Residential Type` · `Non Use Code` · `Assessor / OPM Remarks` · `State`

---

## 🛠️ Project Workflow

### 1. Data Preparation & Exploration
- Connected the Excel dataset directly in Tableau and profiled field types and null values.
- Built derived fields for time-based and value-based analysis (see **Calculated Fields** below).

### 2. Calculated Fields & Parameters
| Name | Type | Logic |
|---|---|---|
| **Sale Year** | Dimension | `YEAR([Date Recorded])` |
| **Sale Category** | Dimension | Buckets `Sale Amount` into **High** (≥ 500,000), **Medium** (200,000–499,999), and **Low** (< 200,000) |
| **Select Metrics** | Parameter | Lets users toggle the analysis lens between `Sale Amount` and `Assessed Value` |
| **Selected Metric** | Measure | `CASE` field that dynamically returns `Assessed Value` or `Sale Amount` based on the parameter |
| **Sale Amount (bin)** | Bin | Powers the sale-price distribution histogram |

### 3. Visual Exploration
| Worksheet | Chart Type | Insight |
|---|---|---|
| Total Sale Amount by Town | Bar Chart | Ranks towns by total transaction value |
| Yearly Sales Trend | Line Chart | Year-over-year sales trend, 2011–2022 |
| Monthly Sale Trend / MoM (Line Chart) | Line Chart | Month-on-month seasonality |
| Pie Chart | Pie Chart | Distribution of sales across Property Types |
| Highlight Table | Highlight Table | Average Sales Ratio by Town × Residential Type |
| Treemap | Treemap | Sales volume by Residential Type |
| Histogram | Histogram | Distribution of sale amounts (using Sale Amount bin) |
| State Map | Filled/Symbol Map | Geographic distribution of sales |

### 4. Dashboard & Interactivity
The visuals are combined into a single interactive dashboard featuring:
- **Filters:** Town, Sale Year, Property Type
- **Highlight Action** — hovering emphasizes related marks across a town/property category (`Highlight1`)
- **Filter Action** — clicking a chart element cross-filters the rest of the dashboard (`Filter1`)
- **URL Actions** — dynamic hyperlinks (`Hyperlink1`, `Hyperlink2`) that open a web page (e.g., Wikipedia / real-estate portal) based on the selected **Town**
- **Parameter Control** — toggle between `Sale Amount` and `Assessed Value` to re-lens every chart on the fly

### 5. Storytelling
A **4-slide Tableau Story** narrates the analysis end to end:
1. **Overall Trends By Year** — macro view of the market across the decade
2. **Town-wise Performance & Sales Ratio** — which towns lead in volume and assessment accuracy
3. **Property Type Composition** — the mix of Residential / Commercial / Industrial activity
4. **Key Insights & Recommendations** — actionable takeaways for the Board

---

## 📊 Key Insights

- Property sales activity is **concentrated in a handful of towns**, which consistently drive the largest share of total transaction value.
- **Sales Ratio** (Assessed ÷ Sale value) varies meaningfully by town and residential type, flagging municipalities where assessments may be lagging market prices — a direct input for **reassessment/taxation policy**.
- Sales volume shows clear **seasonality**, with predictable monthly peaks useful for planning zoning-office staffing and review cycles.
- **Single-Family** and **Condo** residential types dominate sales volume, while higher-value categories are concentrated in fewer towns.
- The **High/Medium/Low Sale Category split** highlights where luxury/high-value transactions are clustering geographically — useful for targeted zoning review.

---

## 🧰 Skills Demonstrated

- Data cleaning & shaping for BI visualization
- Calculated fields, parameters, and dynamic (CASE-based) measures
- Chart selection best practices (bar, line, pie, highlight table, treemap, histogram, map)
- Dashboard interactivity: filter actions, highlight actions, URL actions
- Data storytelling using Tableau Story Points
- Stakeholder-focused design for non-technical audiences



---

## 🔗 Live Dashboard

https://public.tableau.com/app/profile/trishula.mitra/viz/Tableau_Real_Estate_Sale_Analysis_Project/Dashboard?publish=yes


---

Dashboard Preview
📌 Add your screenshots below — export images from Tableau (Worksheet/Dashboard → Export → Image) and place them in an images/ folder in your repo, then update the paths.

<img width="1881" height="853" alt="Screenshot 2026-07-14 235215" src="https://github.com/user-attachments/assets/578a82e6-542f-4818-99a1-5e27d00cff91" />

---
<img width="1441" height="830" alt="Screenshot 2026-07-14 235236" src="https://github.com/user-attachments/assets/7b717697-47de-4c14-91c6-7fda3893642b" />

---

<img width="1443" height="738" alt="Screenshot 2026-07-10 002428" src="https://github.com/user-attachments/assets/b15b107e-1e49-4398-b91d-f9a10eec77aa" />


---
<img width="1415" height="758" alt="Screenshot 2026-07-10 002600" src="https://github.com/user-attachments/assets/a349f1a3-da27-489e-810d-bbaf36dffc30" />

---

<img width="1423" height="762" alt="Screenshot 2026-07-10 002632" src="https://github.com/user-attachments/assets/aefd5f3e-63da-4653-b45f-b90dd1ef314d" />

---
<img width="1452" height="766" alt="Screenshot 2026-07-10 002659" src="https://github.com/user-attachments/assets/4e7565c1-3127-438b-97b4-ee91e2a7b18c" />

---
<img width="677" height="715" alt="Screenshot 2026-07-10 002712" src="https://github.com/user-attachments/assets/19c251b2-4047-4beb-8f92-e47162dce029" />

---
<img width="1440" height="762" alt="Screenshot 2026-07-10 002805" src="https://github.com/user-attachments/assets/cf39336d-169a-44e9-9334-49a02049ea16" />

---

<img width="1088" height="767" alt="Screenshot 2026-07-14 235433" src="https://github.com/user-attachments/assets/e40fe68c-481d-4763-b77f-153d79a4257e" />

---

<img width="1679" height="763" alt="Screenshot 2026-07-14 235504" src="https://github.com/user-attachments/assets/1f32fc3a-a1c3-4e61-a466-26fa55673b16" />

---

<img width="1679" height="833" alt="Screenshot 2026-07-14 235517" src="https://github.com/user-attachments/assets/9a3a951a-7ff4-40b7-b31b-b58a1b164d89" />


---

<img width="1678" height="745" alt="Screenshot 2026-07-14 235541" src="https://github.com/user-attachments/assets/d82e538c-cc79-45f9-97b7-6587a27a81ee" />


---

<img width="1680" height="761" alt="Screenshot 2026-07-14 235555" src="https://github.com/user-attachments/assets/779f6b24-a3ae-4597-9749-6b261fc592d3" />


---

## 📁 Repository Contents
```
├── Real_Estate_Sales_Analyzing.twbx                 # Packaged workbook (data + dashboard + story)
├── Tableau_Assignment.pdf                            # Original project brief
└── README.md                                         # Project documentation (this file)

---

## 🚀 How to Use

1. Download `Real_Estate_Sales_Analyzing.twbx`.
2. Open with **Tableau Desktop** (or **Tableau Reader** for view-only access) — version 2026.2 or later recommended.
3. Navigate to the **Story** tab to walk through the narrated insights, or explore the dashboard directly using the Town / Year / Property Type filters and the Metric parameter.



