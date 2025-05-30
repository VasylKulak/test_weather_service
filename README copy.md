## Weather service API

A FastAPI-based application that provides weather information for a list of cities.

## Features

- Fetch real-time weather data for multiple cities.

- Track task status and retrieve results .

- Dockerized for easy deployment.

- Error logging for better debugging.

## Installation

Follow these steps to set up and run the project:

```shell
# Clone the repository
git clone https://github.com/b3v3kt0r/weather_service

# Set up .env file
Create a .env file in the root directory based on .env.sample and configure the necessary environment variables.

# Build and run docker-compose container
docker compose up --build   

# Check it out
http://127.0.0.1:8000/docs/
```

## Configuration

- .env: Stores API keys and configurations.

- Logs are stored in api_errors.log for debugging.

## API Endpoints

  - POST /weather/: Send list of cities.
    - Description: Submit a list of cities to retrieve their weather data.
    - Request Example:
      ```shell
      {
        "cities": ["Kyiv", "New York", "London"]
      }
      ```
    - Response Example:
      ```shell
      {
        "task_id": "a2b3a50c-c0a7-4a3a-9748-77dba7b43d65"
      }
      ```
  - GET /tasks/{task_id}: Retrieve details about specific task.
    - Description: Retrieve the status of a weather request.
    - Response Example:
      ```shell
      {
        "task_id": "636e23cf-630f-4712-83b9-02de4aad3273",
        "status": "SUCCESS",
        "result_urls": [
            "weather_data/Europe/task_636e23cf-630f-4712-83b9-02de4aad3273.json",
            "weather_data/America/task_636e23cf-630f-4712-83b9-02de4aad3273.json"
          ]
      }
      ```
  - GET /results/{region}/: Retrieve weather of a specific region.
    - Description: Fetch weather results for a specific region.
    - Response Example:
      ```shell
      {
        "region": "Europe",
        "results": [
            {
                "city": "Kyiv",
                "temperature": "-5.0",
                "description": "Clear"
            },
            {
                "city": "London",
                "temperature": "4.1",
                "description": "Overcast"
            }
        ]
      }
      ```

## Contact
For contact me:
* Fullname: Stanislav Sudakov
* Email: stanislav.v.sudakov@gmail.com
* Telegram: @sssvvvff
