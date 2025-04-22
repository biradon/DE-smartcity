# 🚦 Smart City Streaming Data Pipeline

A real-time data engineering project that simulates a Smart City traffic system using a modern streaming data pipeline. It leverages Kafka, Apache Spark, AWS S3, AWS Glue, and AWS Athena/Redshift to ingest, process, store, and query streaming vehicle data.
The project is following the video from CodeWithYu [link](https://youtu.be/Vv_fvwF41_0?si=qrQUbdzB7xjJ9aVm)

---

## 📌 Project Overview

This project demonstrates how to design and build a streaming pipeline for vehicle telemetry data in a smart city environment. Data is produced to Kafka, processed by PySpark in real-time, stored in AWS S3 as Parquet files, and made queryable using AWS Glue and Athena.

---

## ⚙️ Tech Stack

- **Apache Kafka** – Real-time data ingestion
- **Apache Spark (PySpark)** – Streaming data processing
- **AWS S3** – Storage layer for Parquet files
- **AWS Glue** – Schema discovery via Crawlers
- **AWS Athena** – Serverless querying (or optionally Redshift)
- **Docker Compose** – Local development for Kafka and Spark

---

## 🧪 How It Works

1. **Kafka** receives streaming vehicle data (simulated JSON).
2. **Spark** reads from Kafka in real-time using `readStream()`, parses the JSON schema, and writes the result to S3.
3. **AWS S3** stores the data in Parquet format with partitioning support.
4. **AWS Glue Crawler** crawls the S3 bucket to infer schema and create a metadata table in Glue Data Catalog.
5. **Redshift** queries the processed, structured data.
6. **DBeaver** visualize the data in local

