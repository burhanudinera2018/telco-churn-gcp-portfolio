# 📡 Telecom Milan Network Traffic Analysis
## End-to-End Data Pipeline & Spatial Intelligence Platform

[![Python](https://img.shields.io/badge/Python-3.11-blue.svg)](https://www.python.org/)
[![GCP](https://img.shields.io/badge/Google%20Cloud-4285F4?logo=googlecloud&logoColor=white)](https://cloud.google.com/)
[![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?logo=googlecloud&logoColor=white)](https://cloud.google.com/bigquery)
[![Looker Studio](https://img.shields.io/badge/Looker%20Studio-4285F4?logo=looker&logoColor=white)](https://lookerstudio.google.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## 📌 Project Overview

This project builds an **end-to-end data pipeline** to analyze telecommunication network traffic in Milan, Italy, using **14.3 million records (2.5 GB of data)** from Harvard Dataverse, enriched with WorldPop population density data.

**Business objectives:**
- Identify daily and spatial traffic patterns
- Discover correlation between network traffic and population density
- Provide infrastructure investment priority recommendations

> **📁 Repository Note:**  
> *All code and pipeline logic are available in a local environment. Due to security and file size considerations, notebooks are not uploaded to GitHub. However, the entire process — ETL, processing, analysis, and deployment — is fully documented visually through screenshots and the summary below.*

---

## 🏗️ Architecture: 8-Stage Telecom Data Pipeline

![8-Stage Telecom Data Pipeline](8-stage%20telecom%20data%20pipeline%20diagram.png)

| Stage | Technology | Description |
|-------|------------|-------------|
| 1. Raw Data | CSV Files | 30 files (2.5 GB) from Harvard Dataverse |
| 2. Cloud Storage | GCS | Secure & scalable upload |
| 3. Data Warehouse | BigQuery | Loading & aggregation |
| 4. Spatial Join | SQL + GIS | Traffic + population data |
| 5. Visualization | Looker Studio | Interactive dashboard |
| 6. Business Insights | Analytics | 4 key strategic insights |
| 7. Deliverable | Reports & Maps | Stakeholder-ready outputs |
| 8. Scalability | GCP Native | Secure, cost-efficient, fast |

---

## 📂 Pipeline in Action (Visual Documentation)

### 1. Environment Setup & GCP Activation

![Getting Started with GCP](Getting%20started%20with%20Google%20Cloud.png)

- Conda environment `ds_portfolio` activated
- Logged into Google Cloud Console
- Project `ds-portfolio-12345` created
- All required APIs enabled (BigQuery, Storage, Vertex AI)

### 2. Upload Data to Cloud Storage

![Cloud Storage Upload Workflow](Cloud%20storage%20upload%20workflow%20diagram.png)

- 30 CSV files (2.5 GB total) uploaded to bucket `my-milan-bucket`
- Folder structure: `milan_daily/`
- 100% upload complete — secure, scalable, and accessible from anywhere

### 3. High-Speed Data Processing

![High-Speed Data Processing](High-speed%20data%20processing%20in%20action.png)

- **54+ million rows** processed in BigQuery
- Complex queries with temporal & spatial aggregation
- Execution time < 30 seconds (GCP scalability)

### 4. Spatial Join: Traffic + Population Density

![Merging Traffic and Population Data](Merging%20traffic%20and%20population%20data.png)

| Layer | Source | Purpose |
|-------|--------|---------|
| Layer 1 | Traffic Data (Green Dots) | Traffic volume per grid |
| Layer 2 | WorldPop Density Map | Population density (people/km²) |
| **Merged Insight** | BigQuery Spatial JOIN | Correlation traffic vs population |

**Resulting correlation:** `r = 0.701` (strong positive)

---

## 📊 Milan Telecom Spatial Dashboard

![Milan Telecom Dashboard Overview](Milan%20telecom%20spatial%20dashboard%20overview.png)

### Key Metrics

| Metric | Value | Interpretation |
|--------|-------|----------------|
| Total Grids | 894 | 100% coverage of Milan |
| Average Priority Score | 58.4 / 100 | Moderate priority level |
| Total Traffic Volume (24h) | 386.1K | Across all grids |
| Traffic–Population Correlation | **0.701** | Strong positive relationship |

### Priority Distribution by Grid

| Priority Level | Number of Grids | Percentage |
|----------------|----------------|------------|
| Critical | 3 | 0.3% |
| High | 29 | 3.2% |
| Medium | 77 | 8.6% |
| Low | 785 | 87.8% |

### Top 5 Critical Grids

| Grid ID | Priority | Traffic Volume | Population Density | Incident Count (7d) |
|---------|----------|----------------|--------------------|---------------------|
| 3128 | Critical | 1,245 | 18,730 | 23 |
| 2715 | Critical | 1,102 | 16,985 | 19 |
| 3250 | Critical | 1,034 | 17,512 | 21 |
| 2987 | Critical | 987 | 15,892 | 17 |
| 3066 | Critical | 956 | 14,321 | 16 |

### Priority Distribution Visual

![Priority Distribution](Priority%20distribution%20for%20Milan%20grids.png)

- **Critical grids (0.3%)** → immediate infrastructure attention
- **Low priority grids (76.2%)** → stable, low traffic volume

---

## 💡 4 Key Business Insights

![4 Key Business Insights](4%20key%20business%20insights%20infographic.png)

| # | Insight | Business Action |
|---|---------|----------------|
| **01** | **Peak Hour Identified** (5 PM) | Schedule maintenance outside peak hours |
| **02** | **High Variability Detected** | Dynamic resource allocation needed |
| **03** | **Predictive Advantage** (R² = 0.802) | Proactive planning using forecasts |
| **04** | **Expansion Opportunity** | Prioritize high-potential zones |

---

## 🗺️ Data Processing & Population Density Map

![Data Processing & Population Density](Data%20processing%20and%20population%20density%20map.png)

- **30 daily CSV files** (Jan 1 – Jan 30) processed
- **Spatial JOIN** with WorldPop Italy Population Density
- Grids with higher population density → higher traffic volume (r = 0.701)

---

## 📁 Portfolio Complete — Project Artifacts

![Portfolio Complete](Portfolio%20complete_project%20showcase%20icons.png)

| Artifact | Description | Availability |
|----------|-------------|--------------|
| `GCP Pipeline.ipynb` | End-to-end notebook (local) | ✅ Available upon request |
| `Interactive Map.html` | Folium heatmap of Milan grids | ✅ Exported |
| `Dashboard Ready.csv` | Aggregated data for Looker Studio | ✅ Exported |
| `Correlation Plot.png` | Traffic vs population correlation | ✅ Included |
| `Business Report.md` | Final insights & recommendations | ✅ Included |

---

## 🛠️ Tech Stack & Skills Demonstrated

| Category | Technologies |
|----------|--------------|
| **Cloud Platform** | Google Cloud Platform (GCP) |
| **Data Storage** | Cloud Storage, BigQuery |
| **Data Processing** | SQL (BigQuery), Spatial JOIN, Aggregation |
| **Visualization** | Looker Studio, Folium, Matplotlib, Seaborn |
| **Programming** | Python (Pandas, NumPy, GeoPandas) |
| **Environment** | Conda, Jupyter Notebook (local) |

---

## 📈 Key Outcomes & Business Impact

| Outcome | Value | Business Impact |
|---------|-------|----------------|
| Data Processed | 54M+ rows | Scalable big data pipeline |
| Pipeline Cost | < $5 for 2.5 GB | Cost-efficient GCP usage |
| Traffic–Population Correlation | r = 0.701 | Strong evidence for spatial planning |
| Prediction Accuracy | R² = 0.802 | Production-ready model |
| Critical Grids Identified | 3 grids | Clear investment priorities |

---

## 📝 How to Reproduce (High-Level)

> **⚠️ Notebooks are not uploaded to GitHub due to size and security reasons, but the full code is available in a local environment and can be shared upon request.**

```bash
# 1. Setup environment
conda create -n ds_portfolio python=3.11
conda activate ds_portfolio

# 2. Install dependencies
pip install pandas numpy geopandas google-cloud-bigquery matplotlib seaborn

# 3. Authenticate GCP
gcloud auth application-default login

# 4. Run pipeline (local Jupyter)
# - Upload data to Cloud Storage
# - Load into BigQuery
# - Execute spatial JOIN queries
# - Export results to Looker Studio
```

---

## 📊 Looker Studio Dashboard
An interactive dashboard is available on Looker Studio, featuring:

Grid priority filters

Time series traffic volume

Spatial heatmap of Milan

Correlation analysis between traffic and population

🔗 View Dashboard (Link)

## 👨‍💻 About the Author
Burhanudin Badiuzaman

Target Role: Senior Data Scientist / AI Engineer

Industry Focus: Telecom, Energy, Spatial Analytics

LinkedIn: linkedin.com/in/burhanudin-badiuzaman

GitHub: github.com/burhanudinera2018

Email: burhanudinera2018@gmail.com

## 📄 License
MIT License — free for portfolio and educational purposes.

Last Updated: June 2026
Project Status: ✅ Portfolio Ready

*"Turning 54 million rows of data into high-impact business decisions."*

---


