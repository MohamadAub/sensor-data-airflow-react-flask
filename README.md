# Sensor Data Test - Airflow/React/Flask App

## Overview

This project is a proof-of-concept for using Apache Airflow to process
sensor data from an external source. It also uses Flask for the backend
and React for the frontend. Everything runs in a Docker Compose
environment to show how these technologies can work together for data
processing and visualization.

## Components

-   **Apache Airflow**: Runs workflows and processes the external
    dataset.
-   **Flask**: Backend API that interacts with Airflow and the database.
-   **React**: Frontend user interface for triggering DAGs and viewing
    data.

## Data Source

The project uses a dataset from data.world. It contains air pollutant
readings gathered from an electric vehicle equipped with sensors.

## Setup Instructions

1.  Install Docker and Docker Compose.

2.  Create an account on data.world and generate an API token.

3.  Place the token inside the Airflow config file.

4.  Initialize Airflow:

        docker compose up airflow-init

5.  Start all services:

        docker compose up

## URLs

-   Airflow: http://localhost:8080\
-   Flask API: http://localhost:8000\
-   React frontend: http://localhost:3000

## Usage

1.  Log in to Airflow with default credentials: `airflow` / `airflow`.
2.  Trigger the DAG from the React interface.
3.  Once the DAG finishes, refresh the data from the React frontend to
    display results.

## Notes

-   This project is intended for local development and learning.
-   You can extend or deploy each component separately to cloud
    services.
