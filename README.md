# ETL Data Engineering Pipeline with Cloud Integration 

This project demonstrates how to build a simple **End-to-End Data Engineering System** using a combination of popular tools like Kafka, Airflow, Spark, PostgreSQL, and Docker. It provides a comprehensive solution for streaming, processing, and managing data pipelines.

---

## Overview

This system involves the following steps:

1. **Data Streaming**:
   - Data is streamed from an external API into a Kafka topic.

2. **Data Processing**:
   - A Spark job consumes the data from the Kafka topic and transfers it to a PostgreSQL database for storage and further analysis.

3. **Scheduling with Airflow**:
   - Airflow orchestrates the pipeline, scheduling the Kafka streaming task and the Spark job. For demonstration purposes, the Kafka producer is scheduled to run daily, simulating a real-world scenario of constant data ingestion.

4. **Containerization**:
   - All tools are built and run using Docker and Docker Compose, ensuring a seamless and portable deployment.

---

## Technologies Used

- **Apache Kafka**: For real-time data streaming.
- **Apache Spark**: For data processing and transformation.
- **Apache Airflow**: For pipeline orchestration and scheduling.
- **PostgreSQL**: For storing processed data.
- **Docker & Docker Compose**: For containerizing and managing the deployment of the system.

---

## System Architecture

The pipeline consists of the following components:

1. **Kafka Producer**:
   - Listens to an external API and streams data into a Kafka topic.

2. **Kafka Topic**:
   - Acts as a message queue to hold the streaming data.

3. **Spark Job**:
   - Consumes data from the Kafka topic, processes it, and writes it to PostgreSQL.

4. **PostgreSQL**:
   - Serves as the data warehouse for processed data.

5. **Airflow DAGs**:
   - Automate and schedule the Kafka producer and Spark job.
