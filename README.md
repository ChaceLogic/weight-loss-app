# 🏋️‍♂️ Weight Loss Tracker - Flask App with Forecasting 📉

This is a Flask-based web application for tracking weight, calories, and BMR over time. It includes a forecasting chart using linear regression to predict future weight based on historical data. The app runs inside a Docker container and includes a dynamic 30-day forecast feature.

## 🚀 Features

- 📅 Log daily weight, calories, and BMR
- 📊 Interactive chart with Plotly showing:
  - Logged weight
  - Linear regression model
  - Forecasted weight
- 📈 Automatically forecasts weight 30 days into the future (or user-specified)
- 🐳 Runs as a Docker container for easy deployment

## 🧱 Tech Stack

- **Backend**: Flask (Python)
- **Database**: MySQL
- **Charting**: Plotly
- **Containerization**: Docker


## 🐳 How to Run with Docker

```bash
# Clone the repo
git clone https://github.com/TheGib123/weight-loss-app
cd weight-loss-tracker

# Config ENV file
cp env_example .env
nano .env

# Build the Docker image
docker-compose build --no-cache

# Run the container
docker-compose up -d
```


## 🐳 Restart with ENV changes

```bash
# Remove containers
docker compose down

# Remove database volume
rm -rf mysql_database

# Build the Docker image
docker-compose build --no-cache

# Run the container
docker-compose up -d
```

## First import from loseit

Use loseit's API below and upload the files through the Data Import tool

|             |               |                                                                     |
| :---        | :---          | :---                                                                |
| Weight      | API           | https://www.loseit.com/export/details/weight?days={DAY_VAR}         |
|             | API Example   | https://www.loseit.com/export/details/weight?days=168               |
| Calories    | API           | https://www.loseit.com/export/details/foodcalories?days={DAY_VAR}   |
|             | API Example   | https://www.loseit.com/export/details/foodcalories?days=168         |