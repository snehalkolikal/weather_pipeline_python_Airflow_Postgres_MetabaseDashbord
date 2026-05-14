<img width="1917" height="835" alt="Screenshot 2026-05-10 215436" src="https://github.com/user-attachments/assets/1c94037b-c2c1-4710-b2e2-5ebfb9e63c2f" /># Weather Pipeline Project

This project implements an ETL (Extract, Transform, Load) pipeline for weather data using Apache Airflow, PostgreSQL, and Docker.
A complete end-to-end Weather Data Engineering Project that fetches real-time weather data from the OpenWeather API, stores it in PostgreSQL using Apache Airflow ETL pipelines, and visualizes insights in Metabase dashboards.

## Project overview 
This project demonstrates a modern Data Engineering workflow using:

1. Apache Airflow for orchestration
2. PostgreSQL as the data warehouse
3. Docker Compose for containerization
4. pgAdmin for database management
5. Metabase for dashboard visualization
6. OpenWeather API for real-time weather data

The pipeline collects weather information for multiple UK cities daily and stores it inside PostgreSQL for analytics and visualization.

## Architecture
OpenWeather API
       ↓
Apache Airflow ETL DAG
       ↓
PostgreSQL Database
       ↓
Metabase Dashboard

## Project Structure
weather-etl-project/
│
├── dags/
│   └── weather_etl.py
│
├── postgres/
│   └── init.sql
│
├── .env
├── docker-compose.yml
├── README.md
│
└── screenshots/
    ├── airflow.png
    ├── metabase_dashboard.png
    ├── postgres_table.png

## Setup and Running

1. Ensure Docker and Docker Compose are installed on your system.

2. Clone this repository and navigate to the project directory.

3. Copy `.env.example` to `.env` and configure your environment variables (if applicable).

4. Run the following command to start the services:

   ```bash
   docker-compose up -d
   ```

5. Access the Airflow web UI at `http://localhost:8080` (default credentials: admin/admin).

6. The pipeline will run according to the schedule defined in the DAG.

## Metabase Dashboard
Metabase Dashboard
<img width="1899" height="742" alt="Screenshot 2026-05-10 214206" src="https://github.com/user-attachments/assets/a684d402-3ee3-4e85-b7a0-68c37aad5e5b" />
Weather Table in Metabase
<img width="1153" height="767" alt="Screenshot 2026-05-10 214309" src="https://github.com/user-attachments/assets/85fe42cf-6246-455d-bb71-2085c9b04102" />
PostgreSQL Data in pgAdmin
<img width="1917" height="835" alt="Screenshot 2026-05-10 215436" src="https://github.com/user-attachments/assets/eb9db8f4-f303-41eb-8b3e-3b048ce9b508" />

## Usage

- The ETL pipeline extracts weather data from an external API, transforms it, and loads it into PostgreSQL.
- Monitor and trigger DAG runs through the Airflow web interface.

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Make your changes and test them.
4. Submit a pull request.

