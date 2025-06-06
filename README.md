## Weather Service API

A FastAPI-based application that provides weather information for a list of cities.

## Features

- Retrieve up-to-date weather data for various cities.
- Monitor task progress and fetch results when ready.
- Dockerized setup for smooth deployment.
- Error logs for easier debugging and monitoring.

## Installation

Follow these steps to set up and run the project:

```shell
# Clone the repository
git clone https://github.com/VasylKulak/test_weather_service

# Set up .env file
Create a .env file in the root directory based on .env.sample and configure the necessary environment variables.

# Build and run docker-compose container
docker compose up --build

# Check it out
http://127.0.0.1:8000/docs/
