# 🏥 Clinical-Lakehouse-DataOps

> ⚠️ **Status: Active Development / Work in Progress**

An enterprise-grade, event-driven Lakehouse architecture designed to ingest, process, and serve clinical and human-measurement data. This project implements a Medallion Architecture (Bronze, Silver, Gold layers) adhering to Kimball dimensional modeling principles to ensure data products are optimized for downstream Machine Learning models and practitioner dashboards.

## 🏗️ Architecture Overview

The pipeline is decoupled using an event-driven choreography pattern to ensure fault tolerance and high throughput:

1. **Bronze Layer (Raw Ingestion):** - Real-time streaming ingestion via **FastAPI** and **Redpanda (Kafka)**.
   - Asynchronous Edge Vision Workers (YOLOv8) for immediate sensor/image data processing.
2. **Silver Layer (Processing & Enrichment - *WIP*):** - **PySpark** batch/micro-batch processing for data cleansing, validation, and deduplication.
3. **Gold Layer (Serving & AI - *WIP*):** - Dimensional data models (Star Schema) utilizing **Databricks**.
   - **LLM Hub Gateway:** A centralized hybrid routing engine for secure, privacy-first clinical reasoning.

## 💻 Core Tech Stack
* **Data Engineering:** PySpark, Databricks, SQL
* **Streaming & API:** Redpanda (Kafka), FastAPI, WebSockets
* **Machine Learning:** PyTorch, YOLOv8, GenAI/LLMs (Local GGUF & Cloud APIs)
* **Infrastructure:** Docker, Linux, CI/CD

---
*Developed by Tristan Can.*
