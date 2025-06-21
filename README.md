# Automated ELT Pipeline with Airflow, dbt, and PostgreSQL

This project demonstrates how to build a modern data pipeline using **Apache Airflow**, **dbt**, **PostgreSQL**, and **Docker**. The pipeline extracts data from an external API, loads it into a Postgres database, transforms it using dbt, and orchestrates everything through Airflow.

> 🎥 **Based on tutorial by Data Engineer One**  
> [How to build an automated data pipeline using Airflow, dbt, Postgres](https://www.youtube.com/watch?v=vMgFadPxOLk)

---

## 🚀 Tech Stack

| Tool           | Description                                           |
|----------------|-------------------------------------------------------|
| **Apache Airflow** | Manages and schedules the ETL workflow              |
| **PostgreSQL**     | Relational database for storing raw and processed data |
| **dbt**            | Transforms data within Postgres using SQL and manages data models |
| **Docker**         | Containers for Airflow, dbt, Postgres, etc.        |
| **Python + Pandas**| Extracts data from API and stages to Postgres      |

---

## 📁 Project Structure

├── dags/ # Airflow DAGs for orchestrating the pipeline
├── dbt/ # dbt project directory (models, tests, etc.)
├── scripts/ # Python scripts for data extraction
├── Dockerfile # Docker image with necessary dependencies
├── docker-compose.yml # Orchestrates containers for Airflow, dbt, Postgres
├── requirements.txt # Python dependencies
└── README.md # Project documentation
