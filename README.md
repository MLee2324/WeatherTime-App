# Worldwide Weather & Clock

A simple web project that displays **real‑time weather information** and a **world clock** for selected cities around the globe. Users can choose a country and city to view the local time and (optionally) current weather conditions.

This project was built as a small frontend exercise using **HTML, CSS, and JavaScript**, focusing on API usage, date/time logic, and clean UI interaction.

---

## Features

* Country → City dropdown selection
* Live digital clock that updates every second
* Time‑zone aware clock using UTC offsets
* Weather display (temperature, humidity, wind)
* Dynamic weather icons
* Responsive and styled UI

---

## How the Clock Works

* The clock uses **UTC time** from the browser
* Each city has a predefined **UTC offset**
* Time is converted using minute‑based math
* Edge cases (negative time zones) are handled correctly

> Note: Daylight Saving Time (DST) is not included by design, since this is a small demo project.

---

## Weather API (Optional)

The weather section uses the **OpenWeatherMap API**.

To enable weather data:

1. Create a free account at [https://openweathermap.org/api](https://openweathermap.org/api)
2. Get your API key
3. Add it to the script section:

```js
const apiKey = "YOUR_API_KEY";
const apiUrl = "https://api.openweathermap.org/data/2.5/weather?units=metric&q=";
```

If no API key is provided, the clock will still work normally.

---

## Project Structure

```
project-root/
│
├── Background/
│   └── worldwide1.css
│
├── Images/
│   ├── clear.png
│   ├── clouds.png
│   ├── rain.png
│   ├── drizzle.png
│   ├── mist.png
│   ├── humidity.png
│   └── wind.png
│
├── Worldwide/
│   └── world.html
```

---

## How to Run

1. Download or clone the project
2. Open `world.html` in any modern browser
3. Select a country and city
4. (Optional) Add an API key to enable weather

No server or build tools required.

---

## Technologies Used

* HTML5
* CSS3
* JavaScript (ES6)
* OpenWeatherMap API (optional)

---

## Notes & Limitations

* Time zones are handled using fixed UTC offsets
* Daylight Saving Time is not automatically adjusted
* Weather requires a valid API key

---

## Author

Built as a small personal project to practice frontend development concepts.

---

## Future Improvements

* Automatic DST handling using IANA time zones
* 24‑hour / 12‑hour toggle
* Date and weekday display
* Auto‑select default city per country
* Better error handling and loading states
