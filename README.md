# Global Weather Trend Forecasting - Tech Assessment (Advanced)

## 🎯 Corporate Mission Alignment
This engineering project has been developed in strict alignment with the official **PM Accelerator** mission statement:
> **"To empower the next generation of product leaders — impacting millions of lives through real-world innovation."**

---

## 📌 Project Overview
This repository delivers an end-to-end data science assessment analyzing the **Global Weather Repository** dataset. Moving from a robust baseline to advanced analytics, the project extracts meaningful spatial-temporal insights, correlates weather indices with global air pollution metrics, and implements a machine learning ensemble strategy to forecast daily global temperature trends.

---

## 🛠️ Project Architecture & Methodology

```text
├── notebooks/
│   └── weather_trend_forecasting.ipynb   # Complete verified workflow code
├── reports/
│   ├── figures/             # Exported analytical visualizations
│   └── final_presentation.pdf   # Summary Report Document
├── README.md                # Project documentation and pipeline explanation
└── requirements.txt         # Package dependency manifest
```

### 1. Data Cleaning & Preprocessing
*   **Temporal Formatting:** Converted the `last_updated` text attribute to a standardized Pandas `datetime64[ns]` object to establish structural chronology.
*   **Outlier Management:** Identified severe extreme tracking faults (e.g., historical maximum data spikes reaching 79.3°C / 174.7°F). Applied an explicit baseline operational filter between -50°C and 50°C.
*   **Advanced Statistical Anomaly Detection:** Implemented an **Interquartile Range (IQR)** scanning filter on raw input streams. Identified exactly **2,459 statistical anomalies** outside the strict globally calculated natural boundary of **-2.10°C to 45.90°C**.

### 2. Exploratory Data Analysis (EDA) & Unique Advanced Insights
*   **Environmental Impact Analysis:** Compiled a multi-variable Pearson correlation matrix mapping weather metrics directly against critical air contaminants. High-density `sns.heatmap` configurations revealed a positive correlation (`0.25`) between `temperature_celsius` and ground-level `air_quality_Ozone`.
*   **Spatial Analysis:** Processed global geographical coordinates. Engineered a grouped tracking pipeline evaluating average local distributions by country, displaying a regional climate peak across the Middle East and North Africa (MENA).
*   **Feature Importance Evaluation:** Trained a `DecisionTreeRegressor` directly targeting `feels_like_celsius`. Statistical weight parameters ranked barometric pressure (`pressure_mb`) and absolute humidity (`humidity`) as primary operational drivers, while cloud coverage (`cloud`) held minimal predictive weight.

### 3. Predictive Modeling & Ensemble Pipeline
*   **Chronological Split Data:** Enforced strict non-shuffled time-series slicing at the `"2026-01-01"` threshold to prevent historical data leakage.
*   **Model 1 (Baseline Regression):** Linear Regression leveraging a single historical lag-1 parameter (`temp_yesterday`). Baseline performance yielded a Mean Absolute Error (**MAE**) of **5.17°C** and a **RMSE** of **6.98°C**.
*   **Model 2 (Non-Linear Tree Regression):** Implemented a `DecisionTreeRegressor(max_depth=5)` structure to map complex seasonal adjustments.
*   **Advanced Ensemble Model:** Created a uniform Arithmetic Ensemble Averaging wrapper tracking both structural engines simultaneously. The ensemble system successfully minimized forecasting error variance, pushing the model error down to a final optimized **MAE of 5.08°C**.

---

## 🚀 Execution & Setup Instructions

### Prerequisites
*   Python 3.10 or higher installed locally.

### Installation
1.  **Clone this open-source repository:**
    ```bash
    git clone https://github.com/LouisPraise/PMA_assessment_DSintern.git
    cd PMA_assessment_DSintern
    ```
2.  **Install all required libraries:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Data Source Setup:**
    Download the dataset from the official [Kaggle Global Weather Repository Page](https://kaggle.com) and store the CSV file inside your local `data/external/` workspace directory.

---

## 🎥 Project Screen-Share Demo Video
A comprehensive 1-to-2 minute screen-sharing video walkthrough covering the modular codebase execution steps, local file architecture, and analytical output validations is available here:
👉 **[Watch the Submission Demo Video Here](https://drive.google.com/drive/folders/1O4W89GVl5LTzmV2hu8f9X0AfEanf1ag3?usp=sharing)**

---

## 📧 Code Evaluation Access Notes
As requested by the engineering review guidelines, this public open-source project repository allows full execution cloning and download access. For alternative verification checks, structural coordination access has been directly shared with the evaluating collaboration accounts:
*   `community@pmaccelerator.io`
*   `hr@pmaccelerator.io`
