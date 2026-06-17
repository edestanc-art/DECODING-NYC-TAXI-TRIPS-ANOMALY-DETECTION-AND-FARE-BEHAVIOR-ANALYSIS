## DECODING NYC TAXI TRIPS: ANOMALY DETECTION AND FARE BEHAVIOR ANALYSIS

## By Ede Stan.C.

## Overview 

This project explores the NYC Yellow Taxi Trip dataset to uncover patterns in fare behavior, assess data quality, and investigate anomalies within real-world transportation data. Using Python-based exploratory data analysis (EDA), the study examines trip characteristics, fare distributions, and operational trends while identifying unusual records that could impact analytical outcomes.
A key focus of the project was the detection and investigation of anomalies, including negative fare values, extreme outliers, and inconsistent trip records. Rather than removing these observations outright, the analysis explored their potential causes, such as refund transactions, trip cancellations, and data entry or system-related inconsistencies. This approach ensured that data-cleaning decisions were informed by business context rather than assumptions.
Through data cleaning, feature engineering, statistical analysis, and visualization, the project highlights the importance of understanding the story behind the data before drawing conclusions or building predictive models. The findings demonstrate how real-world datasets often contain complexities that require both technical and analytical reasoning to interpret correctly.

## Objectives

* Detect anomalies in taxi trip records
* Analyze fare distribution and behavior
* Identify outliers affecting data quality
* Understand relationship between distance and fare

## Project Link

## Tools Used

* Python-Core programming language for data analysis 
* Pandas- Data Cleaning, manipulation and exploration
* Numpy- Numeric computation and array operations
* Matplotlib- Creating charts and visualizations
* Seaborn- Statistical and enhanced data visualizations
* Jupyter Notebook/Google colab - Interactive environment for coding and analysis

## Dataset

* Dataset: 2017 Yellow Taxi Trip Data
Source: Google Data Analytics Professional Certificate Capstone Resources
* Original Data Provider: New York City Taxi and Limousine Commission (NYC TLC)
* Description:
The dataset contains trip-level records from NYC Yellow Taxi operations, including pickup and dropoff timestamps, trip distance, passenger count, fare amount, payment type, and location identifiers. It was used to perform exploratory data analysis, anomaly detection, and fare behavior investigation.

## Key Insights
1. Trip Distance Pattern
Most trips are short-distance rides (around 1–3 miles median range).
Long-distance trips exist but are rare outliers (airport runs like JFK/LGA dominate them).
This confirms taxis are mainly used for short urban mobility, not long travel.
2. Fare Structure Behavior
Fare increases strongly with distance but not perfectly linear.
Traffic and time-based charges cause fare variation even for similar distances.
Outliers exist (very high fares), usually due to:
Data errors
Extreme long trips
Surge/traffic conditions
3. Time-Based Demand Pattern
Clear rush-hour peaks:
Morning commute (≈ 7–10 AM)
Evening commute (≈ 5–9 PM)
Very low activity around late night to early morning (≈ 3–5 AM).
Demand is strongly tied to workday movement patterns.
4. Spatial Demand (Pickup Hotspots)
Highest pickup activity concentrated in:
Manhattan (Midtown & Downtown)
Business districts and tourist zones
Lower demand in outer boroughs compared to Manhattan core.
Confirms NYC taxi system is center-heavy (hub demand structure).
5. Passenger Behavior
Majority of trips have 1–2 passengers.
Shared rides are relatively rare.
Indicates taxis are mostly used for:
Individual commuting
Business travel
Quick personal transport
6. Payment / Fare Distribution Pattern
Most fares fall within a moderate range ($5–$25 typical trips).
High fare trips are uncommon but heavily skew averages upward.
Distribution is right-skewed (many small fares, few large ones).

## 📊 Additional Insights (Deeper Analysis)
7. Demand is Highly Time-Sensitive
Taxi demand behaves like a cyclical system (daily + weekly cycles).
Weekdays show stronger commuting peaks than weekends.
Weekend trips are more evenly spread across the day.
8. Short Trips Dominate Revenue Volume
Even though long trips generate higher fare per ride, short trips dominate total ride count and system usage.
This means NYC taxi revenue depends on:
High volume + medium fares, not long trips.
9. Inefficiency Windows Exist
Certain hours show:
High demand but fewer available taxis (e.g., 4–6 PM peak congestion)
Other hours show:
Oversupply of taxis but low demand (late night hours)
👉 This imbalance is key for:
Fleet optimization
Dynamic pricing strategies
10. Fare vs Distance Relationship is Noisy
Strong positive correlation exists between fare and distance.
But deviation is caused by:
Traffic congestion
Time-based charges
Route inefficiencies
This makes NYC taxi pricing a multi-factor system, not purely distance-based.
11. Geographic Inequality in Taxi Usage
Manhattan dominates usage, while outer boroughs have lower density.
Suggests:
Unequal taxi availability
Economic + tourism concentration effect
12. Operational Insight
From a systems perspective:
NYC taxi demand is:
Spatio-temporal (space + time dependent)
Highly clustered (Manhattan-heavy)
Predictable in cycles (rush hours + weekends)