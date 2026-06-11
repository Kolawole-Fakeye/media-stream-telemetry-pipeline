# 📊 Automated Media Intelligence & Telemetry Pipeline
### Enterprise Multi-Source Content Analytics & Infrastructure Monitoring Engine

A production-grade, full-stack data pipeline engineered to ingest real-time media streams, execute custom Natural Language Processing (NLP) text analytics, track historical trends using SQL persistence, and monitor system performance via dynamic telemetry tracking. The entire ecosystem is fully containerized using multi-service Docker orchestration.

---

## 🚀 Live Production & Infrastructure Gateways
* **Interactive Frontend Dashboard:** [https://media-stream-telemetry-pipeline-abbudw395xgzappvxiaklh.streamlit.app/]
* **Backend REST API Documentation:** `http://localhost:8000/docs` (Local Swagger UI Gateway)

---

## 🛠️ System Architecture & Core Engineering Features

* **Custom Tokenization & NLP Ingestion Engine:** Features a text-processing pipeline that ingests multi-source articles, programmatically scrubs noise stop-words via optimized set comparisons, strips typographical punctuation (`.strip(",.()")`), and maps real-time linguistic frequencies.
* **Relational Persistence Layer (SQLite):** Implements automated database schema initialization (`trend_logs`) with parameterized SQL insertion queries to securely log keyword metrics, processing timestamps, and dominant corporate keywords.
* **High-Yield SQL Analytics Aggregations:** Utilizes downstream database computing rules (`SUM`, `COUNT`, `GROUP BY`) to query historical trend cycles and surface platform volume metrics with zero in-memory performance penalties.
* **Isolated Multi-Container Docker Orchestration:** Decoupled into two dedicated, containerized environments running on an internal virtual network via `docker-compose`. This completely eliminates cross-environment dependency conflicts and simplifies deployment down to a single terminal command.
* **Infrastructure Telemetry Stream:** Simulates enterprise-grade operational telemetry variables including network throughput (Mbps), system memory utilization, and backend latency metrics (ms) to mimic standard IT infrastructure health monitoring.

---

## 🏗️ Technical Stack & Dependencies

* **Core Backend Engine:** FastAPI (0.110.0), Uvicorn (0.28.0), Pydantic (2.6.4)
* **Data Persistence & Analytics:** SQLite3, Pandas (2.2.1), PyArrow (15.0.0)
* **Presentation & Visualization Layer:** Streamlit (1.32.0), Plotly (5.19.0), Requests (2.31.0)
* **DevOps Container Runtime:** Docker Engine, Docker Compose Architecture (Python 3.11-slim)

---

### Method A: Production Deployment via Docker Compose (Recommended)
Ensure you have Docker Desktop installed, navigate to the root directory of the project in your terminal workspace, and execute the following command:
```bash
docker-compose up --build

* Backend API Gateway Available at: http://localhost:8000
* Frontend Analytics Interface Available at: http://localhost:8501

### Method B: Traditional Python Local Environment Setup
If executing without a container engine, install the requirements directly into your local virtual environment:
pip install -r requirements.txt

1. Initialize the Backend REST Service:
   uvicorn main:app --reload --port 8000

2. Initialize the Frontend Dashboard (Separate Terminal):
   streamlit run ui.py

---

## 📋 Database & API Transaction Schema

The internal SQLite database engine preserves processing histories according to the following relational parameters:

| Table Column Header | Field Data Type | System Mapping Description |
| :--- | :--- | :--- |
| id | Integer | Primary Key (Autoincrementing unique row identifier) |
| source | Text / String | Monitored media publication source (e.g., Techpoint Africa) |
| extracted_at | Text / Datetime | System runtime timestamp matrix (%Y-%m-%d %H:%M:%S) |
| total_keywords | Integer | Volume count of non-noise keywords successfully analyzed |
| top_keyword | Text / String | The highest-occurring word isolated during that specific execution |
