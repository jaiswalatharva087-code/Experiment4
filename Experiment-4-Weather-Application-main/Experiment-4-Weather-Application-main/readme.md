# Experiment 4 - Weather Application

## Overview
This project is a simple web application that fetches current weather information for a city using the OpenWeatherMap API. It demonstrates how to build a backend service with Node.js and Express and how to work with asynchronous JavaScript using promises and async/await.

The experiment focuses on:
- Creating a backend server with Express
- Requesting live weather data from a third-party API
- Handling API responses asynchronously
- Returning JSON data to the client
- Serving static files for a frontend interface

## Objective
The main aim of this experiment is to understand how a web app can communicate with an external API and display live data. In this case, the app fetches weather details such as temperature for a selected city.

## Technologies Used
- Node.js
- Express.js
- Axios
- OpenWeatherMap API
- JavaScript (ES6+)

## Project Structure
- `server.js` - Main backend server file
- `package.json` - Dependencies and project configuration
- `images/` - Project images
- `readmeindexhtml.md` - Additional documentation related to the project
- `approachofexperiment.md` - Explanation of the experiment approach

## How the Application Works
The server starts on port 3000 and exposes a route:

`GET /weather/:city`

Example:
- `/weather/Chennai`
- `/weather/London`
- `/weather/New York`

When a request is sent, the backend builds a URL to the OpenWeatherMap API using:
- the city name
- the API key
- metric units

Then it fetches the data using async/await and returns the temperature in JSON format.

## Example Response
```json
{
  "temperature": 31.2
}
```

## Setup Instructions
1. Open the project folder in the terminal.
2. Install dependencies:

```bash
npm install
```

3. Start the server:

```bash
node server.js
```

4. Open the browser and visit:

```text
http://localhost:3000
```

5. To test the API directly, open:

```text
http://localhost:3000/weather/Chennai
```

## Important Note
The application uses an API key from OpenWeatherMap. For the app to work correctly, the key should be valid and kept private. If the key is invalid or expired, the weather request will fail.

## Learning Outcome
This experiment helps in understanding:
- how servers handle requests
- how frontend/backend communication works
- how asynchronous JavaScript improves API handling
- how real-time data is fetched from external services

## Conclusion
Experiment 4 demonstrates a basic but practical real-world example of using APIs in a web application. It is a good introduction to backend development, API integration, and data fetching using modern JavaScript practices.
