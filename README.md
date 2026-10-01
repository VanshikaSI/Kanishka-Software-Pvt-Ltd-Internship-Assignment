# Kanishka-Software-Pvt-Ltd-Internship-Assignment
# Cafeteria Order Data - Quick Analysis & Forecast Challenge
**Candidate Submission Report**

## 1. Approach & Data Ingestion
- **Challenge:** The SQL dump file was ~1.4 GB (5.7M+ rows), which exceeded standard SQL engine memory limits in a cloud notebook environment.
- **Solution:** Implemented a custom, high-performance in-memory streaming parser in Python to selectively target and extract transaction rows from the `orders` table without memory overhead, successfully capturing all **5,773,679 rows**.

## 2. Exploratory Data Analysis (EDA) & Insights
- **Data Cleaning:** Parsed timestamps, handled missing values, and standardized date-time indices.
- **Branch Analysis:** Evaluated order volumes across all operating branches. 
- **Key Insight:** **Branch 2** emerged as the highest-volume operational center, recording **2,487,949 orders** over the historical period (April 2024 – April 2025).

## 3. 7-Day Order Forecast (Branch 2)
- **Model Design:** Developed a robust rolling-average baseline model capturing recent weekly seasonality and trends.
- **Projections:** Generated actionable daily order volume forecasts for the upcoming week, saved to `branch_2_7day_order_forecast.csv`.

## 4. Deliverables Checklist
- Python Colab Notebook containing full ingestion, cleaning, EDA, and forecasting code.
- Visualization charts embedded in the notebook.
