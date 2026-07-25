#  World Capitals Weather Lookup

This project retrieves current weather information for **world capitals** using two public APIs:
- **REST Countries API** – to get capital names and country codes.  
- **OpenWeather API** – to fetch live weather data (temperature, humidity, pressure, wind, etc.).

All data are stored in a CSV file (`world_capitals_weather.csv`),  
and the user can simply type the name of any capital to view its weather information.

---

##  Features

- Retrieves all world capitals automatically.  
- Collects real-time weather data for each capital.  
- Saves the data in CSV format.  
- Lets the user search for any specific capital’s weather.  
- Organized notebook structure with clear step-by-step cells.

---

##  Project Structure

```

world-capitals-weather/
│
├── world_capitals_weather.ipynb   # Main Google Colab notebook
├── world_capitals_weather.csv     # Output data file
├── README.md                      # Project documentation
└── .gitignore                     # Ignored files and temp data

````

---

##  How It Works

1. **Step 1:** Retrieve all world capitals using the REST Countries API (or fallback CSV).  
2. **Step 2:** Fetch live weather data using the OpenWeather API.  
3. **Step 3:** Save results to a CSV file.  
4. **Step 4:** Let the user enter a capital name to display its current weather only.

---

##  Requirements

- Python 3.x  
- Required libraries:
  ```bash
  pip install requests pandas
````

* An active API key from [OpenWeather](https://home.openweathermap.org/users/sign_up)

---

##  API Setup

Store your API key directly in the notebook (for local use)
or safely using environment variables if you publish the project.

Example:

```python
api_key = "your_api_key_here"
```

---

##  How to Run in Google Colab

1. Open the `.ipynb` notebook in Colab.
2. Run each cell sequentially (1 → 4).
3. When prompted, enter a **capital name** (e.g., `Paris`, `Tokyo`, `Riyadh`).
4. The program will print only the weather for that capital.

---

##  Example Output

```
  Weather data has been saved to 'world_capitals_weather.csv'
  Number of capitals successfully fetched: 48

Enter the capital name to view its weather data: Riyadh

  Weather data for Riyadh:
Date        Time      City   Country  Temperature (°C)  Humidity (%)  Pressure (hPa)  Wind (m/s)  Weather
2025-10-10  21:45:12  Riyadh  SA           33.6              19              1011           3.4      Clear
```


## Future Enhancements

* Add simple data visualization for temperature and humidity.
* Include error correction for misspelled city names.
* Support scheduled automatic updates.

---

## Author

Abdulaziz Bantan
Data Science Student — Umm Al-Qura University
[GitHub: c6uvl](https://github.com/c6uvl)
---

## License

This project is released under the **MIT License** – free for personal and educational use.
