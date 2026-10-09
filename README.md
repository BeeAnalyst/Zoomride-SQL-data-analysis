# ZoomRide SQL Data Analysis Project

## Project Overview

This project analyses ZoomRide's ride hailing data using SQL to understand trip activity, revenue performance, customer behavior, and vehicle performance.

The project also focuses on identifying and correcting data quality issues that could affect business reporting and decision-making.

## Business Questions

The analysis explores questions such as:

* How many trips were recorded?
* Which cities generated the highest revenue?
* Which month recorded the highest revenue?
* How revenue differ across vehicle types?
* Which customers contributed the most recorded spending?
* Which customers have never booked a trip?
* What data quality issues need to be addressed?

## Tools Used

* **MySQL** — data cleaning, querying, aggregation, and analysis
* **GitHub** — project documentation and version control

## Dataset

The project uses three tables:

## Table and Description
*Customers : Customer_id, customer_name, home_city, signup_date, and signup_channels

*Drivers : Driver_name, city, vehicle_types, ratings, and joined_date

*Trips : Trip_id, customer_id, driver_id, city, trip_date, distances, fares, statuses, and payment methods

The original trip dataset contains 300 records.

## Process

### 1. Data exploration

I explored the available tables and examined the trip, customer, and driver records to understand the dataset and prepare for analysis.

### 2. Data cleaning

I identified inconsistent city names, duplicate trip records, and completed trips with missing fares.

The cleaning process included:

* Standardising inconsistent city names and labels.
* Identifying completed trips with missing fare values.
* Checking trip counts after cleaning.

Nine completed trips had missing fare values. These fares were not invented or replaced with assumptions.

### 3. SQL Analysis

I used SQL queries to investigate trip activity, city revenue, monthly performance, vehicle type performance, and customer spending.

The analysis included grouping, filtering, aggregate functions, date formatting, and sorting.

### 4. Business recommendations

I interpreted the results to identify the strongest recorded revenue performing city and highlight data quality issues that management should consider before making business decisions.

## Key findings

### City revenue performance

Lagos recorded the highest revenue among the cities analysed.

| City          | Completed Trips with Recorded Fares | Recorded Revenue |
| ------------- | ----------------------------------: | ---------------: |
| Lagos         |                                  93 |         ₦218,890 |
| Accra         |                                  37 |          ₦92,640 |
| Abuja         |                                  36 |          ₦88,720 |
| Port Harcourt |                                  31 |          ₦71,240 |
| Nairobi       |                                  32 |          ₦58,960 |
| Kampala       |                                  19 |          ₦38,020 |

Lagos generated the highest recorded revenue, while Kampala recorded the lowest revenue among the six cities.

### Monthly revenue performance

December 2025 recorded the highest monthly revenue, with ₦66,980 from 31 completed trips.

### Vehicle type performance

| Vehicle Type | Completed Trips with Recorded Fares | Recorded Revenue |
| ------------ | ----------------------------------: | ---------------: |
| Economy      |                                 121 |         ₦262,550 |
| Comfort      |                                  76 |         ₦239,050 |
| Bike         |                                  51 |          ₦66,870 |

Economy recorded the highest trip volume and revenue. Comfort also generated substantial revenue despite having fewer recorded trips.

### Customer analysis

The three customers with the highest recorded spending were:

* **Chioma Nwosu:** ₦38,950 across 21 completed trips.
* **Tunde Bakare:** ₦37,610 across 13 completed trips.
* **Zainab Garba:** ₦35,380 across 15 completed trips.

Four customers had no recorded bookings:

* Bisi Ogunleye
* Wanjiru Kamau
* Akinyi Ouma
* Nakato Namutebi

These customers could be investigated further to understand whether they need onboarding support or targeted engagement.

### Data quality findings

The original dataset contained inconsistent city labels, including variations such as `PH` and `Port-Harcourt`, as well as spelling errors and extra spaces.

Nine completed trips had missing fares, which limits the completeness of the revenue analysis.

Because operating costs and profit margins were not provided, the analysis measures recorded revenue rather than profits.

## Recommendation to management
Based on the cleaned data, I recommend that Zoomride consider prioritizing Lagos, which generated the highest recorded revenue at ₦218,890 across 93 completed trips with recorded fares. I found inconsistent city names and duplicate trip records, which could split city level reporting and inflate trip counts or revenue if left unresolved. I also identified nine completed trips with missing fares, so reported revenue may be understated. Before making a major investment decision, I would want to compare operating costs and profit margins across cities, alongside customer demand and growth trends.

## Skills demonstrated

* SQL querying and data aggregation
* Data cleaning and standardisation
* Duplicate identification
* Missing value investigation
* Revenue analysis
* Customer behaviour analysis
* Business interpretation and recommendations
* Data quality checks.

## How i ran the project
1. I opened the SQL script in a Onecompiler environment.
2. Reviewed the database and table creation statements.
3. Executed the setup script to create and populate the tables.
4. Ran the SQL queries to explore the data and reproduce the analysis.

## Conclusion

This project demonstrates how SQL can be used to transform raw trip records into useful business insights. It highlights the importance of data quality, revenue analysis, and customer understanding when supporting business decisions.

