# Weather API Server

This is a simple **Node.js** and **Express** server that fetches weather data from the OpenWeatherMap API based on a city name.

## Features
- Fetch real-time weather data using **OpenWeatherMap API**.
- Supports **CORS** for cross-origin requests.
- Uses **dotenv** to manage API keys securely.
- Returns weather details such as:
  - Temperature (in Celsius)
  - Weather description
  - Humidity level
  - Wind speed

## Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v12 or later)
- [NPM](https://www.npmjs.com/) (or `yarn` as an alternative)

## Installation

1. **Clone the Repository:**
   ```sh
   git clone https://github.com/your-username/weather-api.git
   cd weather-api
   ```

2. **Install Dependencies:**
   ```sh
   npm install
   ```

3. **Set Up Environment Variables:**
   - Create a `.env` file in the root directory:
   ```sh
   touch .env
   ```
   - Add the following to `.env`:
   ```env
   WEATHER_API_KEY=your_openweathermap_api_key
   ```

## Running the Server

To start the server, run:
```sh
node server.js
```

For live reloading during development, install and use `nodemon`:
```sh
npm install -g nodemon
nodemon server.js
```

## Usage

Once the server is running, you can access the weather API endpoint:
```sh
http://localhost:3000/weather?city=London
```
"london" can be changed based on users input 

### Example Response:
```json
{
  "city": "London",
  "temperature": 15.3,
  "description": "clear sky",
  "humidity": 60,
  "wind_speed": 3.2
}
```

## Error Handling
- If the city parameter is missing:
  ```json
  { "error": "City parameter is required" }
  ```
- If the OpenWeatherMap API request fails:
  ```json
  { "error": "Unable to fetch weather data" }
  ```
- If the route does not exist:
  ```json
  { "error": "Route not found" }
  ```

## Technologies Used
- **Node.js** – JavaScript runtime
- **Express.js** – Web framework
- **Axios** – For making HTTP requests
- **dotenv** – To manage environment variables

## License
This project is open-source and available under the [MIT License](LICENSE).

