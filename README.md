# 🚖 Uber Data Analytics — Modern Data Engineering Project (GCP + Mage + BigQuery)

## 📌 Project Overview
This project demonstrates an **end‑to‑end modern data engineering pipeline** that ingests, transforms, models, and analyzes Uber trip data using Google Cloud Platform and a production‑style orchestration workflow.

It showcases how raw transportation data can be converted into a structured **analytics‑ready data warehouse** using dimensional modeling and automated pipelines.

---

## 🎯 Objectives
- Build a scalable ETL/ELT pipeline
- Transform raw trip records into a star schema
- Store processed data in a cloud warehouse
- Enable business intelligence dashboards
- Demonstrate modern data stack architecture

---

## 🏗️ Architecture
![Architecture](architecture.jpg)

**Pipeline Flow**

Raw CSV → Cloud Storage → Mage Pipeline → Transformations → BigQuery → Looker Dashboard

---

## 🧰 Tech Stack

### Programming
- Python (Data processing + transformations)

### Cloud Platform — Google Cloud
- Cloud Storage → Data Lake
- Compute Engine → Processing runtime
- BigQuery → Data warehouse
- Looker Studio → Analytics dashboards

### Pipeline Orchestration
- Mage AI → Workflow automation  
  https://www.mage.ai/

---

## 📊 Dataset
**NYC TLC Trip Record Data**

Trip records include:

- Pickup & dropoff timestamps
- Coordinates
- Distance traveled
- Fare breakdown
- Payment type
- Passenger count
- Rate codes


## 🧱 Data Model
The warehouse uses a **Star Schema** optimized for analytics queries.

![Data Model](etl-uber-pipeline/data_model.jpeg)

### Dimension Tables
- datetime_dim
- passenger_count_dim
- trip_distance_dim
- rate_code_dim
- pickup_location_dim
- dropoff_location_dim
- payment_type_dim

### Fact Table
- fact_table → transactional trip metrics

---

## ⚙️ Pipeline Components

| Stage | Description |
|------|-------------|
| Extract | Load CSV from storage |
| Transform | Clean + create dimensions |
| Model | Build fact table |
| Load | Push tables to BigQuery |
| Visualize | Build dashboard |

---

## 📈 Example Analytics Questions
This dataset can answer:

- What time of day generates highest revenue?
- Which locations have most pickups?
- What payment types dominate?
- Average trip distance by weekday?
- Revenue trend over time?

---

## 🚀 How to Run Locally

```bash
git clone <repo>
cd project
pip install -r requirements.txt
python pipeline.py
```

---

## 📦 Project Structure

```
project/
│
├── data/
│   └── uber_data.csv
│
├── pipeline/
│   ├── load.py
│   ├── transform.py
│   └── export.py
│
├── notebooks/
├── architecture.jpg
├── data_model.jpeg
└── README.md
```

---

## 📊 Dashboard
Dashboards are built in **Looker Studio** connected directly to BigQuery tables for real‑time analytics.

---

## 🎓 Learning Outcomes
This project demonstrates practical skills in:

- Cloud data engineering
- Data modeling
- ETL design
- Pipeline orchestration
- Analytics engineering
- Production‑style architecture

---

## 🤝 Contributing
Contributions are welcome.

Steps:
1. Fork repo
2. Create feature branch
3. Commit changes
4. Open pull request

---

## 📜 License
This project is open‑source and free to use for learning and educational purposes.

