# Marketplace Delivery SLA Analysis

 ## Project Overview
This project analyzes marketplace delivery data to evaluate courier performance and calculate on-time delivery rates for orders delivered in May 2026.

## Objective
To calculate the courier-wise on-time delivery rate using actual transit days and promised delivery days.

## Tools & Technologies
- Python
- Pandas
- Matplotlib
- Google Colab
- GitHub

## Data Cleaning
- Checked missing values.
- Converted date columns into datetime format.
- Identified and removed duplicate orders.
- Standardized courier names.
- Excluded test orders and non-eligible orders.

## Analysis
Actual transit days were calculated using:

`Actual Transit Days = Delivered At - Shipped At`

An order was classified as:
- **On Time:** Actual transit days <= Promised days
- **Late:** Actual transit days > Promised days

## Results

| Courier | Eligible Orders | On-Time Orders | On-Time Rate |
|---|---:|---:|---:|
| Blue Dart | 1 | 1 | 100% |
| FastBee | 2 | 1 | 50% |
| ShipQuick | 2 | 1 | 50% |

## Visualizations
Two charts were created:
1. On-Time Delivery Rate by Courier
2. Eligible Orders vs On-Time Orders by Courier

## Data Quality Observation
Order O1008 has a negative promised delivery value (-2 days). It was retained and classified according to the assessment rule.

## Conclusion
Blue Dart recorded a 100% on-time delivery rate, while FastBee and ShipQuick each recorded 50%. Since the analysis contains only five eligible orders, the results should be interpreted cautiously.

## Project Notebook
See `Marketplace_Delivery_SLA_Analysis.ipynb` for the complete Python analysis.
