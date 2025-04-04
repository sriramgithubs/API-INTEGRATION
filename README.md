# API-INTEGRATION

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: SRIRAM P

*INTERN ID*: CT12TDV

*DOMAIN*: FULL STACK WEB DEVELOPMENT

*DURATION*: 8 WEEKS

*MENTOR*: NEELA SANTOSH

# DESCRIPTION FOR TASK
          Introduction to API Integration
API integration is crucial in modern web applications, enabling real-time data retrieval from external services. This Weather Dashboard demonstrates API integration using OpenWeatherMap, fetching live weather data based on user input or geolocation.

Understanding API Calls
APIs (Application Programming Interfaces) allow applications to communicate with external services. Here, we use OpenWeatherMap's API to fetch weather details dynamically.

Fetching Weather by City Name:
The user enters a city name in the input field.
JavaScript constructs an API URL containing the city name and API key.
The browser sends a request to OpenWeatherMap.
The API responds with weather data, which is then displayed.

Fetching Weather by Geolocation:
The browser requests the user's location using the navigator.geolocation API.
If permission is granted, JavaScript extracts latitude and longitude.
The coordinates are sent to OpenWeatherMap to fetch weather details for the exact location.

Step-by-Step Breakdown of API Integration
Setting Up API Key:
The API key (apiKey) is a unique identifier that authenticates requests to OpenWeatherMap.

Handling User Input & Button Clicks:
The Search button retrieves the city name and passes it to the fetchWeather(city) function.
The Use My Location button triggers fetchWeatherByLocation(lat, lon), which retrieves data based on geolocation.

Fetching Data from the API:
The fetch() function sends an HTTP request to OpenWeatherMap and receives a JSON response. The key endpoints used:
https://api.openweathermap.org/data/2.5/weather?q=city&appid=API_KEY&units=metric (City-based search)
https://api.openweathermap.org/data/2.5/weather?lat=lat&lon=lon&appid=API_KEY&units=metric (Location-based search)

Handling API Responses:
If the response is valid (data.cod === 200), the weather data is displayed.
If the city is not found, an error message is shown.

UI and Responsive Design
The CSS file enhances the user experience by:
Using a dark theme (--bg-color1 and --bg-color2).
Making the layout responsive so that it adapts to different screen sizes.
Styling buttons for better usability.

Error Handling & Edge Cases
A good API integration must handle errors efficiently:
Invalid City Name: If the city does not exist, an error message appears.
API Connectivity Issues: If there’s a network problem, an error message is logged.
Geolocation Denied: If the user denies location access, an alert is triggered.
