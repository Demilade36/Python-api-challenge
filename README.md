# Python API Challenge — Module 6

## Overview

This repository contains my solution to the Module 6 Challenge for the Data Analytics Bootcamp:

**Analyzing and Visualizing Global Weather Data (WeatherPy & VacationPy)**

---

## Challenge Breakdown

- **WeatherPy:**  
  Collects weather data for 500+ cities worldwide using the OpenWeatherMap API, and analyzes the relationships between weather variables (temperature, humidity, cloudiness, wind speed) and latitude.

- **VacationPy:**  
  Visualizes optimal vacation cities on an interactive map and finds nearby hotels using the Geoapify API.

---

## Directory Structure

```

python-api-challenge/
│
├── WeatherPy/
│   ├── WeatherPy.ipynb
│   ├── VacationPy.ipynb
│   ├── api\_keys.py         # (NOT INCLUDED IN REPO)
├── .gitignore
├── README.md

````

---

## How to Run

### 1. Requirements

- Python 3.x
- Jupyter Notebook/Lab
- Packages: `requests`, `pandas`, `matplotlib`, `hvplot`, `geoviews`, `citipy`, `scipy`, `cartopy`

Install any missing packages by running this in a Jupyter cell or your terminal:
```python
!pip install requests pandas matplotlib hvplot geoviews citipy scipy cartopy
````

### 2. API Keys Setup

Obtain API keys from:

* [OpenWeatherMap](https://openweathermap.org/api)
* [Geoapify](https://www.geoapify.com/)

Create a file named `api_keys.py` in the same folder as notebooks and paste in:

```python
weather_api_key = "YOUR_OPENWEATHERMAP_API_KEY"
geoapify_key = "YOUR_GEOAPIFY_API_KEY"
```


### 3. Running the Notebooks

* **WeatherPy.ipynb:**
  Collects and analyzes weather data, creates scatter plots, and runs regression analysis on variables versus latitude.

* **VacationPy.ipynb:**
  Visualizes cities on an interactive map, filters for ideal vacation weather, and finds hotels using Geoapify.

---

## Plot & Analysis Explanations

### R² Value Interpretation

* **High r² value** (close to 1):
  Indicates a strong relationship between latitude and the weather variable (e.g., temperature). Most of the variation can be explained by latitude.

* **Moderate r² value** (\~0.5):
  Indicates a moderate relationship. Latitude explains some, but not all, of the variation; other factors matter too.

* **Low r² value** (<0.3):
  Indicates a weak or no linear relationship. Latitude is not a good predictor for this variable.

#### Example Analysis Markdown

* **Temperature:**
  “The high r² value indicates a strong correlation between latitude and max temperature, meaning most temperature variation is explained by distance from the equator.”

* **Humidity:**
  “Low r² values indicate a weak to nonexistent relationship between humidity and latitude. Other factors have a greater influence on humidity.”

* **Cloudiness:**
  “Low r² values indicate a weak relationship between latitude and cloudiness. This suggests that latitude is not a strong predictor of cloud cover.”

* **Wind Speed:**
  “Low r² values indicate that there is no real relationship between wind speed and latitude. The difference between hemispheres is negligible.”
