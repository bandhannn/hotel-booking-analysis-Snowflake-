# hotel-booking-analysis-Snowflake

🧠 Project Overview

This project demonstrates a production-style, Snowflake-native data platform built to ingest, clean, transform, and analyze raw hotel booking data using Medallion Architecture (Bronze → Silver → Gold).

The entire pipeline is implemented inside Snowflake using SQL, from raw ingestion to analytics and dashboarding—without relying on external ETL or BI tools.

🏗️ Architecture Overview

(Insert Medallion Architecture image here)

Data Flow:

Raw CSV files → Snowflake Stage (Bronze)

Cleaned & standardized data → Silver layer

Business-ready aggregates → Gold layer

Analytics & insights → Snowsight dashboards

🧰 Tech Stack

Snowflake

Snowflake SQL

Snowsight Dashboards

Stages, File Formats & COPY INTO

Medallion Architecture (Bronze, Silver, Gold)

🔄 Data Pipeline Design
Bronze Layer (Raw Ingestion)

Loaded raw hotel booking CSV files into Snowflake using Stages and COPY INTO

Preserved raw data structure for traceability and reprocessing

Handled schema inference and file format configuration

Silver Layer (Data Cleaning & Validation)

Applied data quality checks and transformations, including:

Handling missing and null values

Validating and cleaning email fields

Removing or correcting negative pricing values

Fixing invalid date ranges (check-in/check-out)

Standardizing booking status values and correcting typos

Ensured consistent data types and formats across fields

Gold Layer (Analytics & Business Logic)

Built analytics-ready tables using pure SQL

Created business-level metrics such as:

Total bookings

Revenue trends

Booking status distribution

Time-based aggregations

Optimized tables for dashboard consumption

📊 Analytics & Dashboards

Developed interactive Snowsight dashboards directly inside Snowflake

Enabled real-time insights without exporting data to external BI tools

Dashboards designed to support business questions and operational monitoring

