# campus-energy-dashboard-akshit-rajput

# 📊 Campus Energy Dashboard
**Course:** Programming for Problem Solving using Python  
**Assignment:** Capstone Project – Energy Consumption Analysis  
**Student Name:** <YOUR NAME>  
**Date:** <DATE>

---

## 📁 Project Overview
This project provides a complete end-to-end pipeline to analyze campus electricity consumption across multiple buildings.  
It reads raw CSV meter files, cleans them, aggregates daily/weekly usage, models buildings using OOP, and finally generates a dashboard visualization and summary report.

---

## 🎯 Objectives
- Ingest and validate multiple CSV files.
- Aggregate electricity consumption (daily, weekly, building-wise).
- Use Object-Oriented Programming (OOP) for structured modelling.
- Create visual dashboards using Matplotlib.
- Export cleaned datasets and an automated summary report.
- Provide a GitHub-ready, reproducible pipeline.

---

## 🗂️ Project Structure
campus-energy-dashboard/
├── data/ # Input CSV files (one per building)
├── output/ # Auto-generated dashboard + reports
│ ├── cleaned_energy_data.csv
│ ├── building_summary.csv
│ ├── summary.txt
│ └── dashboard.png
├── analysis.py # Data ingestion + aggregation logic
├── models.py # Building & MeterReading OOP classes
├── visualization.py # Dashboard plot creation
├── main.py # Runs the entire pipeline
├── sample_data_generator.py # Optional: generate sample CSV data
├── requirements.txt # Required Python libraries
└── README.md # Project documentation


Dashboard Visualizations:

The dashboard image contains:
Daily consumption trend line
Weekly average usage by building (bar chart)
Top 100 peak readings scatter plot by timestamp
This provides a quick overview of:
High-consuming buildings
Peak electricity usage times
Weekly trends
Consumption spikes


Methodology Summary:

✔ Data Ingestion
Reads all .csv files from /data.
Cleans corrupt rows, missing timestamps, and invalid kWh values.
Merges all buildings into a single dataframe.

✔ Aggregation Logic
Daily totals using resample('D')
Weekly totals using resample('W')
Building-wise summary using groupby()

✔ OOP Structure
Building class stores readings.
MeterReading class holds timestamp + kWh.
BuildingManager class manages multiple buildings.

✔ Visualization
Built with Matplotlib subplots.
Saved as dashboard.png.

✔ Persistence
Saved files:
Clean data
Summary statistics
Dashboard image
Text summary report
