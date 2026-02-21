The Snowflake Hotel Booking Analysis project is an end-to-end data engineering and analytics solution built on Snowflake using a Medallion Architecture (Bronze, Silver, Gold layers).
The goal of this project is to ingest raw hotel booking data, clean and transform it, and generate business-ready insights through KPI calculations and dashboard reporting.

🎯 **Project Objective**

To design a scalable data pipeline in Snowflake that:

Loads raw booking data from CSV files

Cleans and validates the data

Transforms it into analytics-ready tables

Generates key business metrics for decision-making

**Silver Layer – Data Cleaning & Transformation**

The SILVER_HOTEL_BOOKINGS table was created with proper data types and cleaned data.

Key transformations:

Converted string dates into DATE format

Converted total_amount to FLOAT

Removed invalid emails

Standardized city and customer names using INITCAP()

Corrected booking status typos (e.g., confirmeeed → Confirmed)

Ensured check-out date ≥ check-in date

Converted negative amounts to positive values

This layer ensures high data quality and consistency.


**Gold Layer – Business Aggregations**

Created analytics-ready tables:

GOLD_AGG_DAILY_BOOKING

Daily total bookings

Daily total revenue

GOLD_AGG_HOTEL_CITY_SALES

Revenue aggregated by city

GOLD_BOOKING_CLEAN

The following business metrics were developed:

🔹 KPIs

Average Booking Value

Total Guests

Total Bookings

Total Revenue

🔹 Visual Insights

📈 Line Chart – Daily/Monthly Revenue

📈 Line Chart – Daily/Monthly Bookings

📊 Bar Chart – Top 5 Cities by Revenue

📊 Bar Chart – Bookings by Status

📊 Bar Chart – Room Type Distribution

Final clean dataset for KPI reporting

The Gold layer supports BI dashboards and reporting.

**Technical Skills Demonstrated**

Snowflake Database & Warehousing

File Formats & Stages

Data Ingestion using COPY INTO

Data Cleaning & Validation using SQL

Medallion Architecture (Bronze → Silver → Gold)

Data Aggregation & KPI Development

Dashboard-Oriented Data Modeling
