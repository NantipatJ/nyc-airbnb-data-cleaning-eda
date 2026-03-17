# nyc-airbnb-data-cleaning-eda
End-to-end data cleaning and exploratory data analysis of the 2019 New York City Airbnb dataset.

# New York City Airbnb Data Cleaning & Exploratory Data Analysis

## 📌 Executive Summary
This project focuses on the end-to-end data cleaning process of the 2019 New York City Airbnb dataset. The primary objective was to transform "dirty" raw data into a reliable, analysis-ready format by handling missing values, correcting data types, and removing extreme outliers that could skew business insights.

---

## 🛠️ Technical Challenges & Solutions

* **Handling Missing Values:**
    * **Issue:** Identified over 10,000 missing values in `reviews_per_month` and `last_review`.
    * **Solution:** Imputed 0 for `reviews_per_month` (assuming no activity) and converted `last_review` to a proper datetime format, maintaining `NaT` for missing entries to ensure analytical integrity.
* **Outlier Detection & Mitigation:**
    * **Price:** Discovered listings with a price of $0 (data entry errors) and extreme values up to $10,000. Filtered the dataset to include listings between $10 - $1,000 to focus on the general market.
    * **Minimum Nights:** Found extreme outliers (up to 1,250 nights). Standardized the dataset to listings with a 30-night maximum to align with short-term rental trends.
* **Data Integrity & Consistency:**
    * Validated categorical columns (`neighbourhood_group`, `room_type`) to ensure no spelling inconsistencies or formatting issues existed.

---

## 📊 Key Results

1.  **Dataset Optimization:** Reduced the noise in the dataset while retaining 98% of the original data (47,924 high-quality rows).
2.  **Improved Accuracy:** Normalized the average price from a highly skewed figure to a more realistic market average of $141.31 per night.
3.  **Actionable Insight:** The cleaned data revealed that Manhattan remains the most expensive borough with an average price of $179.17, while the Bronx offers the most affordable stays at $85.56.

---

## 💻 Tools Used
* **Python:** Pandas for data manipulation.
* **Visualization:** Matplotlib and Seaborn for outlier detection (Boxplots).
* **Environment:** Google Colab.
