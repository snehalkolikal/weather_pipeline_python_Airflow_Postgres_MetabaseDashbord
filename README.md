# Weather Pipeline Project

This project implements an ETL (Extract, Transform, Load) pipeline for weather data using Apache Airflow, PostgreSQL, and Docker.

## Project Structure

- `docker-compose.yml`: Docker Compose configuration for running Airflow and PostgreSQL services.
- `dags/weather_etl.py`: Airflow DAG defining the weather data ETL pipeline.
- `postgres/init.sql`: SQL script to initialize the PostgreSQL database schema.
- `.env`: Environment variables for configuration.

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

## Usage

- The ETL pipeline extracts weather data from an external API, transforms it, and loads it into PostgreSQL.
- Monitor and trigger DAG runs through the Airflow web interface.

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Make your changes and test them.
4. Submit a pull request.

## License

This project is licensed under the MIT License.