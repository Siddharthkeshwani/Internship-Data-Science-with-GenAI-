Here is a comprehensive `README.md` file formatted for GitHub, documenting the analysis performed on the Diminos Pizza dataset.

---

```markdown
# 🍕 Diminos Pizza Delivery Analysis

## 📌 Project Overview
This project conducts a thorough statistical analysis of the **Diminos Pizza** delivery dataset. The primary objective is to evaluate delivery performance, understand demand patterns, and statistically validate operational efficiency against service level agreements (e.g., the "30-minute delivery promise").

The analysis covers the entire data pipeline, from **data cleaning** and **feature engineering** to **multivariate analysis** and **hypothesis testing**.

---

## 📂 Dataset
The dataset (`diminos_data.csv`) contains **15,000 records** of pizza orders with the following columns:
- `order_id`: Unique identifier for the order.
- `order_placed_at`: Timestamp when the order was placed.
- `order_delivered_at`: Timestamp when the order was delivered.

---

## ⚙️ Installation & Requirements
To run the analysis locally, ensure you have **Python 3.x** installed along with the following libraries:

```bash
pip install pandas numpy matplotlib seaborn scipy

```

---

## 📊 Analysis Workflow

### 1. Data Cleaning & Feature Engineering

* **DateTime Conversion**: Converted string timestamps to datetime objects.
* **Feature Extraction**:
* `delivery_minutes`: Calculated time difference between placement and delivery.
* `order_hour`: Hour of the day (0-23).
* `day_of_week`: Monday - Sunday.
* `is_weekend`: Boolean flag for weekends.


* **Outlier Handling**: Removed extreme outliers (delivery times > 120 minutes) representing < 0.5% of data, likely due to system logging errors.

### 2. Exploratory Data Analysis (EDA)

The analysis includes three layers of exploration:

* **Univariate Analysis**:
* Distribution of delivery times (Right-skewed, Mean ~17.7 mins).
* Order volume analysis showing a significant demand spike between **Midnight and 2 AM**.


* **Bivariate Analysis**:
* **Delivery vs. Hour**: Boxplots reveal consistent delivery speeds even during high-volume hours.
* **Delivery vs. Day**: Visuals confirm no degradation in service on weekends.


* **Multivariate Analysis**:
* **Heatmap**: A Grid view of *Day vs. Hour* showing uniform performance across the entire week.



### 3. Hypothesis Testing

Statistical verification (T-tests) was performed to validate observations:

| Hypothesis | Test Type | P-Value | Result |
| --- | --- | --- | --- |
| **Mean Delivery Time > 30 mins** | 1-Sample T-Test | `1.0` | **Fail to Reject Null** (Mean is < 30m) |
| **Weekend vs. Weekday Performance** | 2-Sample T-Test | `0.80` | **No Significant Difference** |
| **Peak vs. Off-Peak Performance** | 2-Sample T-Test | `0.81` | **No Significant Difference** |

---

## 🔑 Key Findings

1. **High Efficiency**: The operations are highly efficient. The vast majority (~96%) of orders are delivered within 30 minutes.
2. **Robust Operations**: There is **no statistical difference** in delivery times during peak hours (Lunch/Dinner) or weekends, suggesting effective staffing and capacity planning.
3. **Night Owl Demand**: A unique insight is the heavy order volume late at night (00:00 - 02:00), which is handled just as efficiently as daytime orders.
4. **Data Quality**: Approximately 0.5% of records contained extreme outliers (e.g., delivery taking days), which were treated as data artifacts.

---

## 🚀 Usage

1. Clone this repository.
2. Place `diminos_data.csv` in the root directory.
3. Run the analysis script:
```bash
python analysis_script.py

```


4. The script will generate console output for statistical tests and save visualization images (e.g., `univariate_delivery_dist.png`, `multivariate_heatmap.png`) in the local folder.

---

## 📜 License

This project is open-source and available for educational and analytical purposes.

```

```
