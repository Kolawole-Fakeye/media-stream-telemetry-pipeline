## 🦅 Automated Media Intelligence & Telemetry Pipeline
### Enterprise Multi-Source Content Analytics & Infrastructure Monitoring Engine

A decoupled, full-stack data pipeline engineered to ingest real-time textual data from global and regional media outlets, execute text analytics frequency mapping, and manage transactional historical logging using structured SQL persistence.

### 🚀 Live Production Instance
* **Interactive Analytics Interface:** [https://media-stream-telemetry-pipeline-abbudw395xgzappvxiaklh.streamlit.app/]

### 📊 System Architecture & Features

* **Dynamic Text Processing Engine:** Automatically ingests and combines live article matrices from 6 major media hubs (Reuters, Bloomberg Technology, TechCrunch, Wired, Techpoint Africa, and Business Day). It handles programmatic string manipulation, filters out linguistic noise words (stop words), and derives live keyword frequency trends.
* **Structured SQL Persistence Layer:** Features an integrated SQLite database (`pipeline_analytics.db`) that automatically initializes tables on startup and executes explicit transactional `INSERT` statements to log historical extraction vectors.
* **Advanced Metrics Aggregations:** Utilizes structured SQL analytical querying (`SUM`, `COUNT`, `GROUP BY`, and `ORDER BY`) to dynamically expose cumulative keyword volumes, the most active reporting sources, and dominant global trend topics.
* **Infrastructure Telemetry Monitor:** Simulates a live system monitoring infrastructure layer tracking network throughput (Mbps), server latency (ms), and concurrent session volume.

### 🏗️ Technical Engineering Stack

* **Backend Framework:** FastAPI REST API Engine (`main.py`) running decoupled data aggregation endpoints (`/api/trends`, `/api/history`, `/api/analytics`, `/api/telemetry`).
* **Frontend UI Engine:** Streamlit Framework running on a stable Python 3.11 container environment, designed with native web components for ultra-fast load times and zero compilation dependencies.
* **Database Engine:** SQLite3 relational persistence engine handling local transactional file logging.
* **Data Manipulation Layer:** Pandas and NumPy array modeling for high-performance frontend data alignment.

### 🛠️ Local Environment Execution

1. **Spin up the Backend API Gateway:**
   ```bash
   uvicorn main:app --reload
