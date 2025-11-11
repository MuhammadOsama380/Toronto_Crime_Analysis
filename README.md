# 🕵️ Toronto Police Crime Analysis (January–March 2025)

**Course:** Data Mining & Analysis  
**Authors:** Ahmed Al-Mahdi, Abdallah Seyam, Muhammad Osama  
**Tools Used:** Python (pandas, pycaret), Power BI, REST API, JSON  

---

## 📘 Project Overview
This project analyzes crime trends across the **City of Toronto** using the official **Toronto Police Major Crime Indicators (Open Data)** from 2014–2025.  
It focuses on the **first quarter of 2025 (January–March)**, with ~10,000 records cleaned and explored to identify **patterns, hotspots, and temporal trends**.

---

## 🎯 Objectives
- Retrieve and clean open data through REST API (JSON).  
- Explore **temporal (day/hour)** and **spatial (neighbourhood/premises)** patterns.  
- Apply **unsupervised learning (K-Means clustering)** with PyCaret to discover crime clusters.  
- Build an interactive **Power BI dashboard** to communicate key insights.

---

## 📊 Dataset
- **Source:** [Toronto Police Service – Major Crime Indicators](https://data.torontopolice.on.ca/datasets/TorontoPS::major-crime-indicators-open-data/about)  
- **Period:** January – March 2025  
- **Rows:** ~10,000  
- **Main columns:**  
  - `OCC_DATE` – date/time  
  - `OFFENCE` – offence description  
  - `MCI_CATEGORY` – major crime category  
  - `NEIGHBOURHOOD_140` – geographic area  
  - `OCC_DOW` – day of week  
  - `PREMISES_TYPE` – location type  
  - `CRIME_SEVERITY` – derived numeric feature (1–5 scale)

---

## 🧹 Data Preparation
1. Downloaded and filtered the dataset for Q1 2025.  
2. Removed unnecessary fields and handled missing values.  
3. Added a custom `CRIME_SEVERITY` metric based on offence type.  
4. Standardized data types and month/day formats for Power BI integration.  

---

## 🧠 Machine Learning Component
- **Algorithm:** K-Means Clustering (PyCaret unsupervised)  
- **Purpose:** Identify patterns and group neighbourhoods by crime type & severity.  
- **Outcome:** Four clusters representing distinct crime profiles and intensity zones.  

---

## 📈 Power BI Dashboards & Key Visuals
1. **Crimes by Month (Jan–Mar)** – Dip in Feb, rise in Mar.  
2. **Crimes by Day of Week** – Highest on Fri/Sat.  
3. **Crime Category vs Premises Type** – Outdoor and apartments dominate.  
4. **Heatmap (Hour × Day)** – Peak ≈ 22:00 Fridays.  
5. **Cluster Severity Charts** – Cluster 3 shows highest crime severity (≈ 2.7).  
6. **Pie & Donut Charts** – Transit and education premises rank most severe.

---

## 🔍 Insights & Findings
- Crime peaks evenings (18:00–00:00) and weekends.  
- **Outdoor and apartment zones** have highest incident density.  
- **Cluster 3** is most severe; **Cluster 0** shows high frequency but lower severity.  
- **Transit & educational areas** carry the highest average severity (> 2.9).  

---

## 🧭 Conclusion
The Q1 2025 Toronto crime data reveals strong temporal and spatial patterns that can guide law enforcement resource planning.  
Applying machine learning and interactive visual analytics exposes high-risk periods (evenings/weekends) and hotspot premises for targeted policy intervention.

---

## 🧩 Files Included
| File | Description |
|------|--------------|
| **`toronto_crime_jan_mar_2025_all.csv`** | Cleaned dataset (Jan–Mar 2025) |
| **`S25_Data_Mining_Project.pbix`** | Interactive Power BI Dashboard |
| **`Cumulative_Assignment_Report_Data_Mining.pdf`** | Full report with methodology & discussion |
| **`README.md`** | Project summary (this file) |

---

## 🧰 Tools & Frameworks
- Python (3.x) – pandas, pycaret, requests  
- Power BI Desktop  
- Scikit-learn (backend for PyCaret)  
- Matplotlib / Seaborn (for optional plots)

---

## 📂 Recommended Repo Structure
```
Toronto_Crime_Analysis/
├── data/
│   └── toronto_crime_jan_mar_2025_all.csv
├── dashboard/
│   └── S25_Data_Mining_Project.pbix
├── reports/
│   └── Cumulative_Assignment_Report_Data_Mining.pdf
├── README.md
└── requirements.txt
```

---

## 🪪 License
This project is for academic use (Fanshawe College – Data Mining 2025).  
Please cite the authors if you reuse this work for educational purposes.
