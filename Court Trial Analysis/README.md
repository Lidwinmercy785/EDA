**⚖️ Period of Trials by Courts – Exploratory Data Analysis (EDA)**

**📌 Problem Statement**

Delays in the judicial system are a major cause of prolonged under-trials and backlog. To understand the extent and patterns of these delays, this project analyses the duration of court trials across different states and court types in India.

**The goals of this project are:**

- 🔍 Analyse how long cases remain pending across various Indian states

- 🏛️ Compare trial durations across court levels (District/Session Judge, Magistrates, etc.)

- 📊 Identify states or courts with significantly long trial periods

- 🛠️ Help policymakers understand where delays are more severe and what types of cases experience long pendency

The dataset includes categories such as:
< 6 months, 6–12 months, 1–3 years, 3–5 years, 5–10 years, and >10 years case pendency.

- 🧱 Tech Stack

- 🐍 Python

- 📓 Jupyter Notebook

- 📊 Pandas, NumPy — data cleaning & preparation

- 📈 Matplotlib, Seaborn — data visualisation

- 🔍 EDA techniques — descriptive analysis & insights

All analysis and visualisations are inside the notebook.

**📂 Dataset Description**

The dataset contains trial duration statistics for courts in India, with columns:

**🗺️ State Information**

- Area_Name — State / Union Territory

- Year — Data year

**🏛️ Court Details**

- Group_Name — Court category (e.g., District/Session Judge)

- Sub_Group_Name — Subcategory of court

**⏳ Trial Duration Categories**

These columns represent number of cases pending for:

- PT_Less_than_6_Months

- PT_1_3_Years

- PT_3_5_Years

- PT_5_10_Years

- PT_Over_10_Years

- PT_Total — Total pending cases

This helps analyse how long cases stay unresolved and where delays are concentrated.

**🔎 Approach**

**1️⃣ Data Cleaning & Preparation**

- 🧹 Checked for missing or incorrect values

- 🏷️ Standardised court categories and state names

- 🔢 Converted duration columns into numeric format

- 📊 Verified total counts (PT_Total) vs sum of all duration categories

- 📆 Filtered records by court types and years where needed

**2️⃣ Exploratory Data Analysis**

The EDA focuses on understanding delay patterns:

**📈 State-wise pendency**

- Distribution of trial duration across each state

- Identifying states with high counts of >5 years and >10 years pendency

**🏛️ Court-type analysis**

- Comparing pendency across:

- District/Session Judge

- Judicial Magistrate

- Executive Magistrate

**⏳ Duration-based insights**

- % of cases resolved within 1 year

- % of long-pending cases (5–10 years, >10 years)

- Where majority of delays occur

**🧩 Key patterns identified:**

- Certain states have a high concentration of long-pending cases

- District courts show larger backlogs than magistrate courts

- Some states resolve most cases within a year

- Long pendency directly increases overall backlog

- All charts, heatmaps, and comparison plots are included in the notebook.

**3️⃣ Feature Engineering (if applicable)**

Created additional fields such as:

- Long_Pending = PT_5_10_Years + PT_Over_10_Years

- Short_Pending = PT_Less_than_6_Months + PT_6_12_Months

- Pendency_Ratio = Long_Pending / PT_Total

- State_Ranking by delay severity

These help identify:

- Courts with high delay intensity

- States with worst backlog ratio

**📊 Results & Insights**

**High-level findings:**

- ⚠️ Some states have very high long-pending cases (>5 years)

- 🏛️ District/Session courts contribute significantly to overall backlog

- ⏳ A large share of cases in some states remain unresolved for over 3 years

- 📉 States with better short-term pendency also show lower overall backlog

**Key observations:**

- States like [You will insert from your EDA results] show consistently high trial durations

- Courts with heavier caseloads have larger fractions of long-pending trials

- Early-stage resolution (<1 year) significantly reduces long-term backlog

These insights can help policymakers:

- Allocate judges and resources where delays are highest

- Improve case management and digital tracking

- Introduce reforms for fast-track disposal of older cases

**📁 Project Structure**

**📦 period-of-trials-eda**    
│
├── 📄 README.md  
├── 📓 Period_of_trials_by_courts.ipynb    
├── 📂 data    
   └── 29_Period_of_trials_by_courts.csv    
