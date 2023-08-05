# Global_Corona_andemic_Analysis

This project focuses on visualizing COVID-19 vaccination data using Python's pandas, numpy, matplotlib, and folium libraries. The goal is to analyze and present vaccination doses per capita data on a world map.

## Table of Contents

- [Introduction](#introduction)
- [Setup](#setup)
- [Data Processing](#data-processing)
- [Data Visualization](#data-visualization)
- [Map Visualization](#map-visualization)
- [License](#license)

## Introduction

This project involves loading and processing COVID-19 vaccination data from a CSV file using pandas and numpy libraries. The data is then visualized using matplotlib to generate insights from the dataset. Furthermore, the processed data is plotted on a world map using the folium library to provide a geospatial perspective of vaccination progress.

## Setup

To run this project on your machine, you'll need Python installed along with the necessary libraries. You can install the required packages using the following command:

```bash
pip install pandas numpy matplotlib folium
```

## Data Processing

1. The project starts by importing necessary libraries: pandas, numpy, datetime, and matplotlib.
2. The CSV file `"covid-vaccination-doses-per-capita.csv"` is read into a pandas DataFrame.
3. The dataset is explored using the `info()` method to get an overview of the data's structure.
4. The 'Date' column is converted to a datetime format and set as the DataFrame's index.
5. The 'Day' column is dropped from the DataFrame.
6. The length of unique entities (countries/regions) is calculated.

## Data Visualization

1. The dataset is grouped by 'Entity' (countries/regions) using pandas' `groupby()` function.
2. For each group, the key (country/region name), number of records, and the first few records are printed.

## Map Visualization

1. The folium library is used to create a choropleth map to visualize the data geospatially.
2. The map is centered using latitude and longitude coordinates.
3. The geojson data for world countries is loaded from "World_Countries_Generalized.geojson".
4. A choropleth layer is added to the map using folium's `Choropleth` class.
5. The color of each country's region on the map corresponds to the total vaccinations per hundred people.
6. A layer control is added to the map to allow toggling the choropleth layer.
