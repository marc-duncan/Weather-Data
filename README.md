# Weather Data Visualization

The script:

- Reads and cleans daily weather data from `WeatherDataCLL.csv`
- Handles missing values safely
- Organizes measurements by day and by month
- Produces four different plots to explore temperature, pressure, wind, humidity, and precipitation patterns

---

## Files

- `weather_data_analysis.py`  
  Main Python script that loads the dataset, processes it, and generates the plots.

- `WeatherDataCLL.csv`  
  Input dataset (not included here). The script expects a CSV with at least the following columns in this order:

  1. Date (`MM/DD/YYYY`)
  2. Dew point
  3. Pressure
  4. Wet bulb temperature
  5. Wind speed
  6. Precipitation
  7. Relative humidity
  8. Average temperature
  9. High temperature
  10. Low temperature

---

## Visualizations

The script generates four figures:

### 1. Average Wet Bulb Temperature vs Pressure

- **Type**: Dual-axis line plot  
- **X-axis**: Day index (order of entries in the dataset)  
- **Left Y-axis**: Average wet bulb temperature (°F)  
- **Right Y-axis**: Average pressure (inHg)  

This plot helps visualize how wet bulb temperature and pressure change over time and whether they appear to move together or independently.

---

### 2. Histogram of Average Wind Speed

- **Type**: Histogram  
- **X-axis**: Average wind speed (mph)  
- **Y-axis**: Number of days  

This shows how wind speeds are distributed across the dataset, highlighting typical ranges and any outliers.

---

### 3. Average Relative Humidity vs Dew Point

- **Type**: Scatter plot  
- **X-axis**: Average relative humidity (%)  
- **Y-axis**: Average dew point (°F)  

Each point represents one day with valid humidity and dew point data. This plot explores the relationship between how “humid” the air feels and the dew point temperature.

---

### 4. Temperature and Precipitation by Month

- **Type**: Combined bar and line chart with a secondary Y-axis  
- **X-axis**: Month (1–12)  
- **Primary Y-axis (left)**:
  - Bar: Mean average temperature for the month (°F)  
  - Line: Highest daily high temperature in that month (°F)  
  - Line: Lowest daily low temperature in that month (°F)  
- **Secondary Y-axis (right)**:
  - Line: Mean monthly precipitation  

This summarizes seasonal trends: how temperatures and precipitation change throughout the year.

---

## Requirements

- Python 3.x
- [NumPy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)

You can install the dependencies with:

```bash
pip install numpy matplotlib
