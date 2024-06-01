# Automobile Sales Analysis During Recession Periods

<img src='https://github.com/Shishir1265/Automobile-Sales-Statistics-Dashboard/blob/main/dash-ss2-recession%20statistics.png' alt='Interactive Dashboard' />
<img src='https://github.com/Shishir1265/Automobile-Sales-Statistics-Dashboard/blob/main/dash-ss2-yearly%20statistics.png' alt='Interactive Dashboard' />

## Table of Contents

- [Introduction](#introduction)
- [Objectives](#objectives)
- [Data Description](#data-description)
- [Technologies Used](#technologies-used)
- [Dashboard Link](#dashboard-link)
- [Visualizations and Insights - Part 1](#visualizations-and-insights---part-1)
- [Visualizations and Insights - Part 2](#visualizations-and-insights---part-2)
- [Conclusion](#conclusion)
- [Acknowledgments](#acknowledgments)

## Introduction

This project analyzes the historical trends in automobile sales during various recession periods. By examining various factors such as GDP, Unemployment Rate, Consumer Confidence, and more, we aim to gain insights into how recessions impacted automobile sales.

## Objectives

- Create informative and visually appealing plots with Matplotlib, Seaborn, and Dash.
- Analyze data to uncover insights on the impact of recessions on automobile sales.
- Understand the correlation between different economic indicators and their effect on sales.

## Data Description

The dataset contains historical automobile sales data, representing sales and related variables during recession and non-recession periods. The key columns include:

- **Date**: The date of the observation.
- **Recession**: Indicates recession period (1 means it was a recession, 0 means it was normal).
- **Automobile_Sales**: The number of vehicles sold.
- **GDP**: The per capita GDP value in USD.
- **Unemployment_Rate**: The monthly unemployment rate.
- **Consumer_Confidence**: Represents consumer confidence.
- **Seasonality_Weight**: Represents the seasonality effect on automobile sales.
- **Price**: The average vehicle price.
- **Advertising_Expenditure**: The advertising expenditure of the company.
- **Vehicle_Type**: The type of vehicles sold.
- **Competition**: The measure of competition in the market.
- **Month & Year**: Extracted from Date.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Dash (for interactive visualizations)
- Folium (for mapping)

## Dashboard Link

Explore the interactive dashboard: [Automobile Sales Analysis Dashboard](https://engmlubbad-8050.theianext-1-labs-prod-misc-tools-us-east-0.proxy.cognitiveclass.ai/)

## Visualizations and Insights - Part 1

1. **Yearly Sales Trend**: Analyzed how automobile sales fluctuated yearly.
2. **Sales Trend by Vehicle Type**: Observed variations in sales trends between different vehicle types during recession periods.
3. **Sales during Recession vs. Non-Recession**: Compare the sales trend per vehicle type for a recession period with a non-recession period.
4. **Effect of GDP on Sales**: Examined the variations in GDP during recession and non-recession periods.
5. **Seasonality Impact**: Analyzed the effect of seasonality on automobile sales.
6. **Correlation Analysis**: Studied the correlation between consumer confidence, average vehicle price, and automobile sales during recession periods.
7. **Advertising Expenditure Analysis**: Explored how the advertising expenditure changed during recession and non-recession periods.

## Visualizations and Insights - Part 2

- **Interactive Dashboard with Dash**: Developed a comprehensive dashboard for users to select and visualize various aspects of the data dynamically.
- **Recession vs. Yearly Data Analysis**: Users can select between analyzing data for recession periods or yearly sales statistics.
- **Year Selection for Analysis**: Enhanced the dashboard to allow users to select a specific year and gather insights from that year's data.
- **Detailed Recession Analysis**: The dashboard provides visualizations such as line charts, bar graphs, and pie charts, offering insights into the automobile sales trend, average number of vehicles sold by type, expenditure share by vehicle type, and the effect of unemployment during recessions.
- **Yearly Sales Analysis**: Similar to the recession analysis but focuses on data from a selected year, allowing users to see trends and patterns specific to that year.

## Conclusion

This project provided valuable insights into the behavior of automobile sales during recession periods. GDP, consumer confidence, and unemployment rates significantly influence sales trends, especially during economic downturns.

## Acknowledgments

- Data provided by IBM Developer Skills Network.
- Special thanks to Dr. Pooja for guidance during the project.


# Create visualizations using Matplotib, Seaborn and Folium

## Table of Contents

- [Objectives](#objectives)
- [Setup](#setup)
- [Installing Required Libraries](#installing-required-libraries)
- [Importing Required Libraries](#importing-required-libraries)
- [Scenario](#scenario)
- [Data Description](#data-description)
- [Importing data](#importing-data)

## Objectives

  After completing this lab you will be able to:
- Create informative and visually appealing plots with Matplotlib and Seaborn.
- Apply visualization to communicate insights from the data.
- Analyze data through using visualizations.
- Customize visualizations

## Setup

  For this lab, we will be using the following libraries:
- [`pandas`](https://pandas.pydata.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for managing the data.
- [`numpy`](https://numpy.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for mathematical operations.
- [`matplotlib`](https://matplotlib.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for plotting.
- [`seaborn`](https://seaborn.pydata.org/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for plotting.
- [`Folium`](https://python-visualization.github.io/folium/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMML0187ENSkillsNetwork31430127-2021-01-01) for plotting.

## Installing Required Libraries

  The following required libraries are pre-installed in the Skills Network Labs environment. However, if you run these notebook commands in a different Jupyter environment (e.g. Watson    Studio or Ananconda), you will need to install these libraries by removing the # sign before %pip in the code cell below.

  %pip install seaborn
  %pip install folium

## Importing Required Libraries

  import numpy as np
  import pandas as pd
  %matplotlib inline
  import matplotlib as mpl
  import matplotlib.pyplot as plt
  import seaborn as sns
  import folium

## Scenario

  In this assignment you will be tasked with creating plots which answer questions for analysing "historical_automobile_sales" data to understand the historical trends in automobile       sales during recession periods.
  recession period 1 - year 1980
  recession period 2 - year 1981 to 1982
  recession period 3 - year 1991
  recession period 4 - year 2000 to 2001
  recession period 5 - year end 2007 to mid 2009
  recession period 6 - year 2020 -Feb to April (Covid-19 Impact)

## Data Description

  The dataset used for this visualization assignment contains historical_automobile_sales data representing automobile sales and related variables during recession and non-recession       period.

  The dataset includes the following variables:
1. Date: The date of the observation.
2. Recession: A binary variable indicating recession perion; 1 means it was recession, 0 means it was normal.
3. Automobile_Sales: The number of vehicles sold during the period.
4. GDP: The per capita GDP value in USD.
5. Unemployment_Rate: The monthly unemployment rate.
6. Consumer_Confidence: A synthetic index representing consumer confidence, which can impact consumer spending and automobile purchases.
7. Seasonality_Weight: The weight representing the seasonality effect on automobile sales during the period.
8. Price: The average vehicle price during the period.
9. Advertising_Expenditure: The advertising expenditure of the company.
10.Vehicle_Type: The type of vehicles sold; Supperminicar, Smallfamiliycar, Mediumfamilycar, Executivecar, Sports.
11.Competition: The measure of competition in the market, such as the number of competitors or market share of major manufacturers.
12.Month: Month of the observation extracted from Date..
13.Year: Year of the observation extracted from Date.
By examining various factors mentioned above from the dataset, you aim to gain insights into how recessions impacted automobile sales for your company.

## Importing Data

  from js import fetch
  import io
  URL = "https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-DV0101EN-SkillsNetwork/Data%20Files/historical_automobile_sales.csv"
  resp = await fetch(URL)
  text = io.BytesIO((await resp.arrayBuffer()).to_py())
  import pandas as pd
  df = pd.read_csv(text)
  print('Data downloaded and read into a dataframe!')
