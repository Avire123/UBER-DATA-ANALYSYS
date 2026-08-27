# 🚕 Uber Data Analysis

## 📌 Project Overview

This project analyzes **200,000 Uber trip records** to uncover patterns in ride demand, trip characteristics, pickup locations, and fare amounts.

The analysis uses Python-based exploratory data analysis to transform raw trip data into meaningful insights that can support operational planning, demand management, and pricing decisions.

---

## 🎯 Objectives

The project aims to answer the following questions:

- When is Uber demand highest?
- Which days and hours have the most trips?
- Where are Uber pickups most concentrated?
- How does trip distance relate to fare amount?
- What insights can be generated from trip-level data?
- What additional data would be required to analyze cancellations?

---

## 🛠️ Technologies Used

- **Python**
- **Pandas** – Data manipulation and analysis
- **NumPy** – Numerical calculations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Jupyter Notebook** – Analysis and documentation

---

## 🔍 Analysis Workflow

### 1. Data Cleaning
- Inspected dataset structure and data types
- Checked for missing values
- Identified duplicate records
- Converted timestamps into datetime format
- Removed invalid records and geographic outliers

### 2. Feature Engineering
Created additional analytical features including:

- Hour of day
- Day of week
- Year
- Trip distance in kilometres using the Haversine formula

### 3. Demand Analysis

Analyzed Uber trip volumes across:

- Hours of the day
- Days of the week
- Day-of-week and hourly combinations

### 4. Geographic Analysis

Analyzed the geographical distribution of pickup locations to identify areas with high concentrations of Uber activity.

### 5. Fare Analysis

Investigated the relationship between:

- Trip distance
- Fare amount

Pearson correlation was used to measure the strength of the relationship between distance and fare.

---

## 📊 Key Findings

### Peak Demand

The original analysis identified **7:00 PM as the highest-demand hour**, with **12,605 trips** recorded during that hour.

### Pickup Concentration

Uber pickups are heavily concentrated within the New York City area, with particularly dense activity around central/Manhattan locations.

### Distance & Fare

The analysis identified a **positive relationship between trip distance and fare amount**, indicating that longer trips generally correspond to higher fares.

### Cancellation Analysis

Cancellation behavior cannot be directly analyzed using this dataset because it does not contain cancellation status, cancellation reasons, driver response information, or rider wait-time data.

---

## 💡 Business Recommendations

Based on the analysis:

1. **Driver Allocation**  
   Increase driver availability during high-demand periods.

2. **Demand Forecasting**  
   Use historical hourly and daily patterns to improve demand forecasting.

3. **Geographic Positioning**  
   Position drivers strategically around high-demand pickup zones.

4. **Pricing Analysis**  
   Further investigate how distance, time, location, and other factors influence fares.

5. **Cancellation Analytics**  
   Collect cancellation, ETA, driver-response, and wait-time data to enable deeper cancellation analysis.

---

## 📁 Project Structure

```text
uber-data-analysis/
│
├── data/
│   └── uber.csv
│
├── notebooks/
│   └── uber_data_analysis_cleaned.ipynb
│
├── outputs/
│   ├── hourly_demand.png
│   ├── demand_heatmap.png
│   ├── pickup_density.png
│   └── distance_vs_fare.png
│
├── images/
│
├── README.md
├── requirements.txt
└── .gitignore
