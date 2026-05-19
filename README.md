<div align="center">
  <img src="data_engineering_banner.svg" alt="Data Engineering Banner" width="100%"/>
</div>


# Hi, I'm Prasun Dutta 👋

**Data Engineer** · MSc Computer Science @ University of Bonn 🇩🇪

Learning to design and build end-to-end data pipelines - Spark processing, Airflow orchestration and Snowflake warehousing across Azure, Microsoft Fabric & AWS. On top of that, I am exploring building LLM agents with LangGraph, RAG systems, and MCP integrations. Currently deepening my expertise in Data Engineering and Applied AI at Masters level.

---

## 🔧 Tech Stack

**Data Engineering**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache%20Spark-E25A1C?style=flat-square&logo=apachespark&logoColor=white)
![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)
![MinIO](https://img.shields.io/badge/MinIO-C72E49?style=flat-square&logo=minio&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white)

**AI & LLM**

![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![Claude](https://img.shields.io/badge/Anthropic%20Claude-D97757?style=flat-square&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-Model%20Context%20Protocol-6B48FF?style=flat-square&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![RAG](https://img.shields.io/badge/RAG-Retrieval%20Augmented%20Gen-00C853?style=flat-square&logoColor=white)

**Cloud**

![Azure](https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Microsoft Fabric](https://img.shields.io/badge/Microsoft%20Fabric-742774?style=flat-square&logo=microsoft&logoColor=white)
![AWS](https://img.shields.io/badge/Amazon%20AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)


**Languages & Tools**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)

---

## 🚀 Featured Projects

### 🎵 [Spotify Data Pipeline v1 (Azure)](https://github.com/PrasunDutta007/Spotify-Datapipeline-Azure)
> End-to-end cloud data pipeline ingesting Spotify streaming data from SQL into a Bronze→Silver→Gold medallion architecture on Azure, with Databricks AutoLoader, Delta Live Tables, and SCD Type 1 & 2 served via Unity Catalog.

- **Ingestion**: SQL DB → Azure Data Factory (incremental CDC load) → Azure Data Lake (Bronze, Parquet)
- **Silver**: Databricks AutoLoader (Spark Structured Streaming) → cleansed Delta tables (dedup, transformations, duration flags)
- **Gold**: Delta Live Tables (DLT) → SCD Type 1 & 2 CDC flows → Unity Catalog gold layer (star schema)
- Built with: `Azure Data Factory` `Azure Data Lake` `Databricks` `Apache Spark` `Delta Live Tables` `Azure Key Vault` `Logic Apps`

---

### 🎧 [Spotify Data Pipeline v2 (AWS)](https://github.com/PrasunDutta007/Spotify-Datapipeline-AWS)
> End-to-end pipeline extracting Spotify playlist data via AWS Lambda, transforming it with AWS Glue (PySpark), auto-ingesting into Snowflake via Snowpipe, and orchestrating the full flow with Apache Airflow on Docker.

- **Extraction**: Spotify API → AWS Lambda (+ Spotipy Layer) → S3 raw JSON
- **Transformation**: AWS Glue (PySpark) → albums / artists / songs CSVs → S3 transformed
- **Loading**: Snowpipe (auto-ingest via SQS) → Snowflake tables
- **Orchestration**: Apache Airflow (Docker Compose, CeleryExecutor) → daily DAG
- Built with: `AWS Lambda` `AWS Glue` `Amazon S3` `Snowflake` `Apache Airflow` `Docker`

---

### 📈 [Stock Market Data Pipeline](https://github.com/PrasunDutta007/Stock-Market-Datapipeline)
> End-to-end production-grade pipeline ingesting real-time and historical stock data via AlphaVantage through dual batch and streaming architectures.

- **Batch**: AlphaVantage → Kafka → MinIO → Spark → Snowflake (Airflow orchestrated, daily schedule)
- **Streaming**: AlphaVantage → Kafka → MinIO → Spark Structured Streaming (15-min / 1-hr rolling windows)
- Built with: `Apache Kafka` `Apache Spark` `Apache Airflow` `Snowflake` `MinIO` `Docker Compose`

---

### 🏠 [Airbnb Data Pipeline (dbt)](https://github.com/PrasunDutta007/Airbnb-Datapipeline-dbt)
> Airbnb data pipeline using AWS S3, Snowflake, and dbt-core. Raw CSVs are staged into Snowflake and transformed through a Bronze→Silver→Gold medallion architecture with incremental loads, Jinja-driven OBT, SCD Type 2 snapshots, star schema, custom macros, and data quality tests.
 
- **Ingestion**: AWS S3 (CSV) → Snowflake External Stage → `COPY INTO` Staging
- **Transformation**: Bronze (raw incremental) → Silver (cleansed + macros) → Gold (OBT + Ephemeral + Snapshots + Fact)
- Built with: `dbt-core` `Snowflake` `AWS S3` `Python 3.12` `uv`
  
---

### 🎓 [Learning Management System (LMS) Data Pipeline (Microsoft Fabric)](https://github.com/PrasunDutta007/Learning-Management-System-Datapipeline-Fabric)
> End-to-end LMS data pipeline built on Microsoft Fabric. Daily CSV files flow through a Medallion Architecture (Raw → Landing → Bronze → Silver → Gold) via Fabric Pipelines and PySpark notebooks, building a star schema with incremental MERGE logic, and surfacing student performance analytics in a live Power BI dashboard.

- **Ingestion**: ADLS Gen2 (CSV) → Fabric Pipeline (GetMetadata + ForEach, daily schedule) → Date-partitioned Landing zone
- **Transformation**: Bronze (incremental Delta load) → Silver (dedup, null handling, business KPIs via MERGE) → Gold (Dim_student, Dim_course, Fact_student_performance)
- **Analytics**: Gold Lakehouse → Fabric Semantic Model → Power BI dashboard (grades, completion rates, performance scores)
- Built with: `Microsoft Fabric` `Azure Data Lake` `Apache Spark` `Delta Lake` `PySpark` `Power BI`

---

### 🤖 [Proxy-Meet: Intelligent Meeting Automation](https://github.com/PrasunDutta007/Proxy-Meet)
> Intelligent meeting automation system that acts as your proxy in Zoom - joining via a streamed OBS avatar, detecting your name and responding via voice and chat, recording the full session, and running a seven-agent CrewAI pipeline to push structured notes to Notion and a Minutes of Meeting draft to Gmail.
 
- **Meeting Bot**: Selenium-driven Zoom join → OBS virtual camera avatar → name detection → voice & chat auto-response → FFmpeg + VB-CABLE audio recording
- **Post-Processing**: AssemblyAI + Gemini 2.5 Pro transcription (speaker diarization) → 7-agent CrewAI pipeline (analysis, action items, formatting, QA, strategy, curation, email composition)
- **Delivery**: Dual-format structured notes → Notion database + Minutes of Meeting draft → Gmail | Streamlit post-meeting review dashboard
- Built with: `CrewAI` `Google Gemini 2.5 Pro` `AssemblyAI` `Selenium` `OBS Studio` `Notion API` `Gmail API` `Streamlit`
---

## 📊 GitHub Activity

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/PrasunDutta007/PrasunDutta007/output/github-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/PrasunDutta007/PrasunDutta007/output/github-snake.svg"/>
  <img alt="github-snake" src="https://raw.githubusercontent.com/PrasunDutta007/PrasunDutta007/output/github-snake.svg"/>
</picture>

---

## 📬 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/prasun-dutta-a35a32150/)
[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=flat-square&logo=telegram&logoColor=white)](https://t.me/PrasunJeetDutta)
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/channel/UCy5QJ0BLGOPfFxtgvg10MrQ)

---

<p align="left">
  <img src="https://komarev.com/ghpvc/?username=PrasunDutta007&style=flat-square&color=blue" alt="profile views"/>
</p>
