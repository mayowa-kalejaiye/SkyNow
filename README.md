# SkyNow - Your Personalized Weather Buddy

SkyNow is a weather application that provides personalized weather information based on your location. It offers:

- **Current Weather:** Displays temperature, wind speed, and a background image related to the current weather.
- **Weather Forecast:** Shows a 5-day forecast with maximum and minimum temperatures for each day.
- **Geolocation Support:** Automatically fetches weather data based on your current geolocation or allows you to input coordinates.

### Features

- **Dynamic Background Image:** The app changes its background based on the weather condition:
  - **Sunny Weather**: Clear skies and bright images.
  - **Cloudy Weather**: Overcast skies with soft lighting.
  - **Rainy Weather**: Images of rainy conditions.
  - **Snowy or Stormy Weather**: Darker, more intense weather visuals.

### Technologies Used

- **React.js** for building the user interface.
- **Open-Meteo API** for fetching weather data.
- **Tailwind CSS** for styling.
- **JavaScript (ES6+)** for the app logic.

### How It Works

1. **Weather Data Fetching:**
   - The app fetches weather data based on the user's geolocation or manually entered coordinates (latitude and longitude).
   - The data includes the current weather (`temperature`, `windspeed`, `weathercode`) and a 5-day forecast.

2. **Dynamic Background:** 
   - The `getBackgroundImage` function checks the `weathercode` from the API response and dynamically updates the background image to reflect the current weather.

   Example conditions:
   - **Clear Weather (weathercode <= 1):** Displays a bright, clear sky.
   - **Cloudy Weather (weathercode <= 3):** Displays a cloudy scene.
   - **Rainy Weather (weathercode between 51 and 65):** Shows rainy images.

3. **User Interface:**
   - The user sees the weather information and forecast, with a dynamic background based on the weather.
   - There's a coordinate input field for manual location search and suggestions for popular locations.

4. **Styling:**
   - Tailwind CSS is used for responsive and modern design.
   - The background image transitions smoothly, enhancing the overall user experience.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/mayowa-kalejaiye/SkyNow.git
   cd skynow
2. Install dependencies:
   ```bash
   npm install
3. Run the development server:
   ```bash
   npm start
---

Open your browser and navigate to http://localhost:3000 to view the app.

### Environment Variables
Ensure you have an .env file for sensitive data (like API keys), if necessary.

### Contributing
If you'd like to contribute, please feel free to fork the repository and submit a pull request. All contributions are welcome!

### License
This project is licensed under the MIT License - see the LICENSE file for details.
