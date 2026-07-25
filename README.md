# Streaming Content Strategy: IMDb Ratings vs. Viewership 🎬

## 📌 Project Overview
This project analyzes streaming movie catalogs to understand what drives content success across two key dimensions: **Perceived Quality** (IMDb Ratings) and **Commercial Scale** (Watch Hours). Using an end-to-end Data Science pipeline, the project extracts actionable catalog insights to guide content acquisition and optimization.

## 🛠️ Data Pipeline & Workflow

* **ETL & Data Cleaning:** Focused the analysis on Feature Films (removing incomplete TV show records), binned 18 languages into 4 key geographical regions, applied One-Hot Encoding for categorical variables, and handled missing values using median imputation.
* **Exploratory Data Analysis (EDA):** Identified key distribution patterns—IMDb ratings follow a normal distribution, while watch hours exhibit a heavy right-skew (viral hit pattern). Correlation analysis revealed a surprisingly weak relationship between budget and user ratings.
* **Predictive Modeling:** Built a standardized ML pipeline (60/20/20 split) using **Multiple Linear Regression** to extract interpretable rating factors, and **Random Forest Regressors** (with log transformation) to model viewership volume and non-linear feature interactions.

## 💡 Key Takeaways & Strategic Insights

* **The "Streaming Paradox" (Quality vs. Viewership):** Comparing interpretable Linear Models against Random Forest Regressors mathematically proved that IMDb ratings and Watch Hours are driven by completely decoupled factors. A high rating does not guarantee viral scale.
* **Budget & Geography as Statistical Noise:** Feature importance and weight analysis revealed near-zero correlation between production budget/runtime and IMDb ratings. Production origin matters far less for quality than distributor prestige (e.g., HBO Max, Apple TV+).
* **Capturing Viral Scale (Power-Law Viewership):** Log-transformed Tree models successfully captured non-linear viewership spikes, identifying high-performing regional drivers (e.g., Turkish releases) that generate extreme engagement despite making up under 3% of catalog inventory.
* **Data-Driven Acquisition ROI:** Streamers can maximize acquisition ROI by shifting budget away from high-cost, saturated generic genres toward underserved, high-demand regional categories.

## 💻 Tools & Technologies

* **Language:** Python
* **Data Processing & EDA:** Pandas, NumPy, Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Linear Regression, Random Forest, Feature Engineering, Metrics)
* **Environment:** Jupyter Notebooks, Git & GitHub

## 🚀 How to Run

1. Clone the repository.
2. Place the raw dataset CSV files inside the `data/` directory.
3. Run the Jupyter Notebooks sequentially:
   * `Final Project-ET&EDA.ipynb`
   * `Final Project-ML.ipynb`
