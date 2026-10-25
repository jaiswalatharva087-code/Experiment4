🌤️ Weather Application — Experiment 4 (SDC Lab)

A lightweight web application built with Node.js, Express, and Axios that fetches live weather data for any requested city using the OpenWeatherMap API.

This repository serves as a hands-on lab experiment demonstrating asynchronous JavaScript operations, RESTful routing, third-party API integration, and static file serving.

📑 Table of Contents

Features

Project Architecture & Directory Structure

Prerequisites

Installation & Setup

API Endpoints

Usage & Examples

Troubleshooting & FAQs

Learning Outcomes

License

✨ Features

Asynchronous Data Fetching: Utilizes async/await syntax with axios to interact cleanly with third-party HTTP endpoints.

RESTful Architecture: Offers clean URL parameter routing (/weather/:city) to retrieve location-based data.

Static Asset Middleware: Configured to serve frontend user interface files (HTML, CSS, client-side JS) via Express.

Error Handling: Handles invalid city queries or upstream network errors with appropriate HTTP status codes and standard JSON error responses.

📁 Project Architecture & Directory Structure

sdc-lab/
├── images/                   # Screenshots and graphical assets
├── public/                   # Static client-side assets (HTML, CSS, JS)
│   └── index.html            # Main User Interface entry point
├── .gitignore                # Specifies intentionally untracked files
├── approachofexperiment.md   # Beginner's execution & concept guide
├── package.json              # Project manifest and dependency registry
├── package-lock.json         # Dependency tree lockfile
├── README.md                 # Primary project documentation
└── server.js                 # Main Express server and API route handlers


⚙️ Prerequisites

Ensure you have the following installed on your local development machine:

Node.js (v14.x or higher)

npm (Node Package Manager, included with Node.js)

OpenWeatherMap API Key (Free account registration required)

🚀 Installation & Setup

Follow these steps to clone and run the project locally:

1. Clone the Repository

git clone https://github.com/your-username/sdc-lab.git
cd sdc-lab


2. Install Dependencies

Run npm install to download all necessary packages defined in package.json:

npm install


3. Configure API Key

Open server.js and update the API_KEY variable with your valid OpenWeatherMap API key:

const API_KEY = 'YOUR_ACTUAL_OPENWEATHER_API_KEY';


4. Run the Server

Start the Express backend server:

node server.js


Upon success, your terminal will log:

Server running at http://localhost:3000


🔌 API Endpoints

1. Live Weather Query Endpoint

URL Path: /weather/:city

Method: GET

URL Params: city (String) — The name of the target city (e.g., Chennai, London, Tokyo).

Success Response (200 OK):

{
  "temperature": 31.2
}


Error Response (500 Internal Server Error):

{
  "error": "Error fetching weather data!"
}


💡 Usage & Examples

Testing in Browser

Open your browser and visit http://localhost:3000 to interact with the static frontend UI.

Direct API request for Chennai:

http://localhost:3000/weather/Chennai


Testing via cURL

curl http://localhost:3000/weather/London


🛠 Troubleshooting & FAQs

Issue

Cause

Solution

Error: Cannot find module 'express'

Dependencies not installed.

Run npm install inside the project root directory.

Error fetching weather data! (500)

Invalid or expired API Key / City not found.

Verify your OpenWeatherMap API key in server.js and check city spelling.

EADDRINUSE: address already in use :::3000

Port 3000 is occupied by another process.

Kill existing process on port 3000 using npx kill-port 3000 or change PORT in server.js.

🧠 Learning Outcomes

Completing and reviewing this experiment builds proficiency in:

Express Server Architecture: Structuring a basic Node server, mounting middleware (express.static, express.json), and defining URL parameters.

Third-Party Integration: Utilizing HTTP clients (axios) to proxy requests to external third-party services safely.

Async Operations in JavaScript: Mastering async/await patterns and try/catch error management.

📜 License

