## Overview

The Weather Dashboard is a Python application that fetches real-time weather data for specified cities using the OpenWeather API and stores the data in an AWS S3 bucket. It provides a simple interface to retrieve and log weather information such as temperature, humidity, and conditions.

## Features

- Fetches current weather data from the OpenWeather API.
- Logs weather data for multiple cities.
- Saves weather data as JSON files in an AWS S3 bucket.
- Automatically creates the S3 bucket if it doesn't exist.

## Prerequisites

Before running the application, ensure the following:

- Python 3.8 or higher is installed.
- An OpenWeather API key.
- AWS credentials configured with access to manage S3 buckets.
- Required Python libraries installed (see Installation).

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/christiancarl1224/weather-dashboard.git
    cd weather-dashboard
    ```
2. Set up environment variables: Create a `.env` file in the project root with the following content:
    ```env
    OPENWEATHER_API_KEY=your_openweather_api_key
    AWS_BUCKET_NAME=your_s3_bucket_name
    ```
3. Install dependencies: Run the following command to install required Python libraries:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Run the application:
    ```bash
    python weather_dashboard.py
    ```
2. Fetch weather for specified cities: The application will retrieve weather data for a predefined list of cities (Philadelphia, Seattle, New York) and display the following:
    - Current temperature
    - Feels-like temperature
    - Humidity
    - Weather conditions
3. Save data to AWS S3: Weather data is saved in the S3 bucket specified in the `.env` file under the `weather-data/` directory with timestamps.

## Dependencies

The project requires the following Python libraries:

- `boto3` (v1.26.137): AWS SDK for Python
- `python-dotenv` (v1.0.0): To manage environment variables
- `requests` (v2.28.2): To make HTTP requests to the OpenWeather API

Dependencies are specified in the `requirements.txt` file.

## File Structure

- `weather_dashboard.py`: Main application script.
- `requirements.txt`: List of dependencies.
- `.env`: File to store environment variables (not included, needs to be created by the user).

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m 'Add new feature'`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.

