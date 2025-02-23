# PWP SPRING 2024

# PROJECT NAME

# Group information

| Name             |
| ---------------- |
| Janne Yrjänäinen |
| Joona Syrjäkoski |
| Joonas Ojanen    |
| Lasse Rapo       |

## Project Description

This project focuses on developing a comprehensive Weather and Biking Data API, inspired by the city of Oulu—a renowned cycling city where residents brave windy and snowy winters to commute by bike. The API is designed to provide real-time, reliable information about weather conditions and biking routes, serving as a crucial component in smart city infrastructures, mobile applications, and smart home systems.

### Overview
The primary goal of this project is to deliver an API that not only offers detailed weather forecasts and traffic data for specific routes. The API is built to integrate seamlessly into larger systems, enabling developers to include vital environmental and commuting information in various applications.

## Key Features:

### Weather Data Retrieval:
-Users can request current and forecasted weather information for specific locations. This includes temperature, precipitation, wind speed, and other relevant meteorological data.

### Traffic and Biking Data:
-The API provides detailed traffic data for particular routes, helping users plan their cycling trips by understanding current conditions and potential delays.

### User Profiles:
-Each user can create and manage a personal profile that stores basic information, activity logs (such as posted comments), and a list of favorite locations. This personalization ensures a more tailored experience.

### Favorite Locations:
-Users have the option to add specific locations to their favorites, making it easier to access frequently checked routes and destinations.
    
### System Architecture:
-The project is built around a RESTful API architecture, ensuring a scalable and maintainable system design. A dedicated database underpins the API, securely storing persistent data such as user profiles, favorite locations. This design facilitates efficient data retrieval and robust performance.


## Virtual environment
### Create virtual environment

```bash
python3 -m venv venv
```

### Activate virtual environment

Linux / macOS
```bash
source venv/bin/activate
```
or on Windows (CMD)
```bash
venv\Scripts\activate.bat
```
or on Windows (PowerShell)
```bash
venv\Scripts\Activate.ps1
```

### Deactivate virtual environment

```bash
deactivate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

## Database
We are using SQLite3 for our database. The database is created by running the command `flask init-db` and populated by running the command `flask populate-db`. The database is populated with some random data to make testing easier. The development database is located in the file `instance/development.db`.

### Create database

```bash
flask --app bikinghub init-db
```

### Populate database

```bash
flask --app bikinghub populate-db
```


## Run the Project

Add MML_API_KEY to .env file. MML_API_KEY is required to fetch the data from the Maanmittauslaitos API.

Run the project with the following command:

```bash
flask --app bikinghub run
```

or with docker

```bash
docker-compose up
```

## Testing

### Install the app for testing
```bash
pip install -e .
```

### Run tests

Run all tests

```bash
pytest
```

Run tests with coverage

```bash
pytest --cov-report term-missing --cov=bikinghub
```


## Development

### Linting

Using Pylint linter (With some disabled warnings per course instructions)

```bash
pylint bikinghub --disable=no-member,import-outside-toplevel,no-self-use
```

### Formatting

Using Black formatter

```bash
black .
```

### API Keys for different services

#### Creating and managing API keys for Maanmittauslaitos

Creating and managing API keys
You can create an API key in the Maanmittauslaitoksen OmaTili-service as follows:

1. Register for [OmaTili](https://omatili.maanmittauslaitos.fi/user/new/avoimet-rajapintapalvelut).
2. Log in with the user name you have registered.

After registering and logging in, you can:
- create an API key by registering with your personal account.
- edit your details or delete your username.
