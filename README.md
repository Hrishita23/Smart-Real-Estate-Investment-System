# 🏡 Smart Real Estate Investment & Risk Intelligence System

## 📌 Overview

The **Smart Real Estate Investment System** is a Big Data-driven analytics platform built using **Apache Spark on Databricks** to help users make **data-driven real estate investment decisions**.

Unlike traditional property platforms that only display listings, this system integrates:

* 📊 Real estate data
* 📉 Economic indicators
* 🤖 Machine learning models

to **predict property prices** and **classify investment zones**.

---

## 🚨 Problem Statement

Real estate investment decisions are often:

* Based on **limited or unreliable information**
* Lacking **predictive insights**
* Missing **risk evaluation tools**

This project solves these issues by building a **scalable Big Data system** that:

* Processes large datasets
* Uses ML for accurate forecasting
* Incorporates real-world economic conditions

---

## 🎯 Objectives

* Build a **Big Data-based analytics system**
* Perform **distributed data processing using Apache Spark**
* Predict property prices using ML models
* Classify investment zones (Low / Medium / High value)
* Integrate **economic indicators for realistic forecasting**
* Provide insights via dashboards (Power BI)

---

## 🏗️ System Architecture

The system follows this pipeline:

**Data Collection → Data Preprocessing → Feature Engineering → Model Training → Prediction → Classification → Visualization**

---

## ⚙️ Tech Stack

* **Platform:** Databricks (Apache Spark)
* **Language:** Python (PySpark)
* **Libraries:** PySpark MLlib, Pandas, NumPy
* **Visualization:** Power BI
* **Environment:** Databricks Community Edition

---

## 📂 Datasets Used

### 1️⃣ Real Estate Dataset

**Source:** India Housing Dataset (Delhi Housing Data)

**Features:**

* Property Price
* Location / Locality
* Area (sq. ft.)
* Number of Bedrooms (BHK)
* Amenities

Dataset Link : https://pypi.org/project/india-housing-datasets/

---

### 2️⃣ Economic Dataset

**Source:** Trading Economics (India CPI & Indicators)

**Features:**

* Inflation Rate
* Interest Rate
* Population Growth

Dataset Link 
Population Growth Rate : https://data.worldbank.org/indicator/SP.POP.GROW

Inflation Rate : https://data.worldbank.org/indicator/FP.CPI.TOTL.ZG?locations=IN

Interest Rate : https://data.worldbank.org/indicator/FR.INR.RINR?locations=IN

---

## 🔄 Data Processing Pipeline

### 1. Data Collection

* Imported housing dataset
* Imported economic indicators (inflation, interest, population)

---

### 2. Data Preprocessing

* Handled missing values
* Converted date → year format
* Aggregated economic data yearly
* Cleaned inconsistent values

---

### 3. Feature Engineering

* Created **Price per Sq Ft**
* Encoded locality using:

  * StringIndexer
  * OneHotEncoder
* Combined:
  **Property Features + Economic Features**

---

## 🤖 Machine Learning Models Used

### Regression Models (Price Prediction)

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* Gradient Boosted Trees (GBT)
* Generalized Linear Regression (GLR)

### Classification Models

* Decision Tree Classifier
* Random Forest Classifier
* Gradient Boosted Trees
* Logistic Regression

---

## 📊 Model Performance

| Model             | RMSE   | MAE   | R² Score |
| ----------------- | ------ | ----- | -------- |
| Linear Regression | 111.51 | 80.93 | 0.9819   |
| Decision Tree     | 291.75 | 73.83 | 0.8764   |
| Random Forest     | 253.85 | 61.07 | 0.9064   |
| GBT               | 323.72 | 57.23 | 0.8478   |
| GLR               | 111.51 | 80.93 | 0.9819   |

👉 **Best Model:** Linear Regression (highest R²)

---

## 📈 How Economic Data Improves Prediction (Important 🔥)

This is the **core strength of your project** 👇

Instead of predicting prices only using property features, you:

### ✔️ Step 1: Integrated Economic Indicators

* Inflation rate
* Interest rate
* Population growth

These were **merged with housing data (year-wise)**

---

### ✔️ Step 2: Created Derived Features

* Economic trends aligned with property timeline

---

### ✔️ Step 3: Used in Model Training

Final feature set included:

* Area
* BHK
* Price per sq ft
* Location encoding
* Economic indicators

---

### ✔️ Step 4: Impact on Predictions

* Inflation ↑ → property prices ↑
* Interest rate ↑ → demand ↓ → price growth slows
* Population growth ↑ → demand ↑ → price ↑

👉 This allowed the model to:

* Capture **real-world price fluctuations**
* Produce **more realistic future predictions (2025–2035)**

---

## 🔮 Future Prediction

* Generated synthetic future dataset (2025–2035)
* Applied economic growth assumptions
* Predicted future property prices

---

## 🏷️ Investment Classification

Predicted prices were categorized into:

* 🟢 LOW_VALUE
* 🟡 MEDIUM_VALUE
* 🔴 HIGH_VALUE

Using **quantile-based thresholds**

---

## 📤 Output

Final output includes:

* Year
* Locality
* Predicted Price
* Price per Sq Ft
* Investment Category

Exported as CSV for Power BI visualization

---

## 🚀 How to Run the Project

### Step 1: Setup

* Open **Databricks**
* Create a new notebook
* Upload datasets

---

### Step 2: Run Pipeline

1. Load datasets into Spark DataFrames
2. Perform preprocessing
3. Run feature engineering
4. Train ML models
5. Evaluate models
6. Generate future predictions
7. Classify investment zones

---

### Step 3: Output

* Export final dataset as CSV
* Use Power BI for dashboards

---

## ⚠️ Limitations

* Based on historical data
* Future predictions use assumptions
* Dataset limited to Delhi
* No real-time data integration

---

## 🔮 Future Scope

* Add real-time APIs (housing + economy)
* Use advanced models (XGBoost, Deep Learning)
* Include more features:

  * Crime rate
  * Connectivity
* Deploy as:

  * Web app
  * AI investment assistant

---

## 👩‍💻 Author

**Hrishita Saha**

---

## ⭐ Key Highlight

👉 The project uniquely combines **Big Data + Machine Learning + Economic Indicators** to create a **real-world investment intelligence system**, not just a price predictor.
