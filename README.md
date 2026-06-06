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

![8-Stage Telecom Data Pipeline](screenshots/8-stage%20telecom%20data%20pipeline%20diagram.png)

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

![Getting Started with GCP](screenshots/Getting%20started%20with%20Google%20Cloud.png)

- Conda environment `ds_portfolio` activated
- Logged into Google Cloud Console
- Project created with billing enabled
- All required APIs enabled

### 2. Upload Data to Cloud Storage

![Cloud Storage Upload Workflow](screenshots/Cloud%20storage%20upload%20workflow%20diagram.png)

- 30 CSV files (2.5 GB total) uploaded to bucket
- Secure, scalable, and accessible from anywhere

### 3. High-Speed Data Processing

![High-Speed Data Processing](screenshots/High-speed%20data%20processing%20in%20action.png)

- **54+ million rows** processed in BigQuery
- Complex queries with temporal & spatial aggregation
- Execution time < 30 seconds

### 4. Spatial Join: Traffic + Population Density

![Merging Traffic and Population Data](screenshots/Merging%20traffic%20and%20population%20data.png)

| Layer | Source | Purpose |
|-------|--------|---------|
| Layer 1 | Traffic Data | Traffic volume per grid |
| Layer 2 | WorldPop Density Map | Population density |
| **Merged Insight** | BigQuery Spatial JOIN | Correlation traffic vs population |

**Resulting correlation:** `r = 0.701` (strong positive)

---

## 📊 Milan Telecom Spatial Dashboard

![Milan Telecom Dashboard Overview](screenshots/Milan%20telecom%20spatial%20dashboard%20overview.png)

### Key Metrics

| Metric | Value |
|--------|-------|
| Total Grids | 894 |
| Average Priority Score | 58.4 / 100 |
| Total Traffic Volume (24h) | 386.1K |
| Traffic–Population Correlation | **0.701** |

### Priority Distribution

![Priority Distribution](screenshots/Priority%20distribution%20for%20Milan%20grids.png)

| Priority Level | Number of Grids | Percentage |
|----------------|----------------|------------|
| Critical | 3 | 0.3% |
| High | 29 | 3.2% |
| Medium | 77 | 8.6% |
| Low | 785 | 87.8% |

---

## 💡 4 Key Business Insights

![4 Key Business Insights](screenshots/4%20key%20business%20insights%20infographic.png)

| # | Insight | Business Action |
|---|---------|----------------|
| **01** | **Peak Hour Identified** (5 PM) | Schedule maintenance outside peak hours |
| **02** | **High Variability Detected** | Dynamic resource allocation needed |
| **03** | **Predictive Advantage** | Proactive planning using forecasts |
| **04** | **Expansion Opportunity** | Prioritize high-potential zones |

---

## 📁 Portfolio Complete — Project Artifacts

![Portfolio Complete](screenshots/Portfolio%20complete_project%20showcase%20icons.png)

| Artifact | Availability |
|----------|--------------|
| GCP Pipeline Notebook | ✅ Available upon request |
| Interactive Map | ✅ Exported |
| Dashboard Data | ✅ Exported |
| Correlation Plot | ✅ Included |
| Business Report | ✅ Included |

---

## 🛠️ Tech Stack

| Category | Technologies |
|----------|--------------|
| **Cloud** | GCP (Cloud Storage, BigQuery) |
| **Data Processing** | SQL, Spatial JOIN |
| **Visualization** | Looker Studio, Folium |
| **Programming** | Python (Pandas, GeoPandas) |

---

## 📈 Key Outcomes

| Outcome | Value |
|---------|-------|
| Data Processed | 54M+ rows |
| Pipeline Cost | < $5 |
| Correlation | r = 0.701 |
| Critical Grids Identified | 3 grids |

---

## 📝 How to Reproduce

```bash
# 1. Setup environment
conda create -n ds_portfolio python=3.11
conda activate ds_portfolio

# 2. Install dependencies
pip install pandas numpy geopandas google-cloud-bigquery

# 3. Authenticate GCP
gcloud auth application-default login

# 4. Run pipeline (local Jupyter)
jupyter notebook

# 5. Run    
```
---

## 👨‍💻 About the Author
Burhanudin Badiuzaman

Target Role: Senior Data Scientist / AI Engineer

LinkedIn: [linkedin.com/in/burhanudin-badiuzaman](https://www.linkedin.com/in/burhanudin-badiuzaman4a9204161/)

GitHub: [github.com/burhanudinera2018](https://github.com/burhanudinera2018/telco-churn-gcp-portfolio)

Email: burhanudinera2018@gmail.com

## 📄 License
MIT License — free for portfolio and educational purposes.

Last Updated: June 2026
Project Status: ✅ Portfolio Ready

*"Turning 54 million rows of data into high-impact business decisions."*

