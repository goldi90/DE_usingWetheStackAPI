# Automated ELT Pipeline with Airflow, dbt, and PostgreSQL

This project demonstrates how to build a modern data pipeline using **Apache Airflow**, **dbt**, **PostgreSQL**, and **Docker**. The pipeline extracts data from an external API, loads it into a Postgres database, transforms it using dbt, and orchestrates everything through Airflow.

> 🎥 **Based on tutorial by Data Engineer One**  
> https://www.youtube.com/watch?v=vMgFadPxOLk

---

## 🚀 Tech Stack

| Tool             | Description                                                   |
|------------------|---------------------------------------------------------------|
| Apache Airflow   | Manages and schedules the ETL workflow                        |
| PostgreSQL       | Stores raw and processed data                                 |
| dbt              | SQL-based transformation layer inside the data warehouse      |
| Docker           | Containerizes the application for easy deployment             |
| Python + Pandas  | Extracts and stages data from APIs                            |

---

## 📁 Project Structure

    .
    ├── dags/                  # Airflow DAGs
    ├── dbt/                   # dbt project (models, profiles)
    ├── scripts/               # Python scripts for extraction
    ├── Dockerfile             # Docker image with dependencies
    ├── docker-compose.yml     # Service orchestration
    ├── requirements.txt       # Python dependencies
    └── README.md              # Project documentation

---

## 🛠️ Setup Instructions

1. Clone the repository

       git clone https://github.com/your-username/your-repo.git
       cd your-repo

2. Build and start services

       docker-compose up --build

3. Access Airflow UI

    - URL: http://localhost:8080
    - Username: airflow
    - Password: airflow

4. Configure Airflow Connections in Admin → Connections:

    - ID: postgres_default
    - Conn Type: Postgres
    - Host: postgres
    - Schema: airflow
    - Login: airflow
    - Password: airflow
    - Port: 5432

5. Trigger the DAG (`elt_pipeline`) from the Airflow UI

---

## ✅ dbt Usage

Run the following inside the dbt container:

    dbt run
    dbt test
    dbt docs generate
    dbt docs serve

Directory structure:

    dbt/
    ├── models/
    │   ├── staging/
    │   └── marts/
    ├── dbt_project.yml
    └── profiles.yml

---

## 🔍 Monitoring & Testing

- Airflow handles scheduling and retries.
- dbt provides:
  - Data tests (`not_null`, `unique`, `relationships`)
  - Lineage and documentation via dbt docs

---

## 📚 References

- [YouTube Tutorial](https://www.youtube.com/watch?v=vMgFadPxOLk)
- [dbt Documentation](https://docs.getdbt.com/)
- [Airflow Documentation](https://airflow.apache.org/docs/)
- [Docker Documentation](https://docs.docker.com/)

---

## 🙌 Author & Credits

- Based on the tutorial by **Data Engineer One**
- README improvements by the community

---

## 📄 License

This project is licensed under the MIT License.
