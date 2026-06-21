# Housing Price Data Analysis - AI/Python Minor Project

An exploratory data analysis (EDA) and visualization project focused on identifying key factors that influence house prices using a dataset of 546 properties.

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Dataset Characteristics](#-dataset-characteristics)
- [Key Analyses & Visualizations](#-key-analyses--visualizations)
  - [1. House Distribution by Price Ranges](#1-house-distribution-by-price-ranges)
  - [2. Price Impact of Air Conditioning](#2-price-impact-of-air-conditioning)
  - [3. Parking Spaces vs. House Prices](#3-parking-spaces-vs-house-prices)
  - [4. Premium & Area Price Gap Analysis](#4-premium--area-price-gap-analysis)
- [Project Structure](#-project-structure)
- [Getting Started & Installation](#-getting-started--installation)
- [Technology Stack](#-technology-stack)
- [Summary of Insights](#-summary-of-insights)

---

## 🔍 Project Overview

The objective of this project is to analyze house pricing dynamics based on physical features, utilities, and location advantages. Through categorical grouping, statistical summary, and visual plotting, this project explores how physical characteristics like area, parking spaces, and air conditioning drive premium pricing.

---

## 📊 Dataset Characteristics

The analysis uses the [Housing.csv](file:///c:/Users/priya/OneDrive/Desktop/Skills/Elewayte/AI%20Minor%20Project/Housing.csv) file, containing 546 records with the following attributes:

| Feature Name | Type | Description |
| :--- | :--- | :--- |
| **price** | Numeric | Absolute price of the house (Target variable) |
| **area** | Numeric | Total area of the house in square feet |
| **bedrooms** | Numeric | Number of bedrooms |
| **bathrooms** | Numeric | Number of bathrooms |
| **stories** | Numeric | Number of stories/floors |
| **mainroad** | Categorical | Whether the house is connected to the main road (yes/no) |
| **guestroom** | Categorical | Presence of a guestroom (yes/no) |
| **basement** | Categorical | Presence of a basement (yes/no) |
| **hotwaterheating** | Categorical | Presence of hot water heating (yes/no) |
| **airconditioning** | Categorical | Presence of air conditioning (yes/no) |
| **parking** | Numeric | Number of parking spaces available (0, 1, 2, 3) |
| **prefarea** | Categorical | Located in a preferred neighborhood/area (yes/no) |
| **furnishingstatus**| Categorical | Furnishing state (furnished, semi-furnished, unfurnished) |

---

## 📈 Key Analyses & Visualizations

All analysis is implemented in the [Minor.ipynb](file:///c:/Users/priya/OneDrive/Desktop/Skills/Elewayte/AI%20Minor%20Project/Minor.ipynb) notebook.

### 1. House Distribution by Price Ranges
Houses are categorized into distinct pricing bins to understand the market segment availability:
*   **0–25 Lakhs (0-25L):** 32 houses
*   **26–50 Lakhs (26-50L):** 318 houses (Majority segment)
*   **51–75 Lakhs (51-75L):** 148 houses
*   **76–100 Lakhs (76-100L):** 39 houses
*   **Over 100 Lakhs (>100L):** 8 houses

*Visualization:* A line chart showing the trend of house counts peaking in the mid-market range (26-50L) and tapering off for luxury units.

### 2. Price Impact of Air Conditioning
A comparative study of the mean pricing of air-conditioned vs. non-air-conditioned homes:
*   **Non-AC Average Price:** ~4.19 Million (41.9 Lakhs)
*   **AC Average Price:** ~6.01 Million (60.1 Lakhs)

*Visualization:* A bar plot depicting the premium pricing associated with air-conditioning utilities.

### 3. Parking Spaces vs. House Prices
Evaluating the relationship between parkings spaces (0 to 3) and market value. 

*Visualization:* A boxplot illustrating how price variance and median price scale upwards with the number of parking stalls.

### 4. Premium & Area Price Gap Analysis
A gap analysis comparing the price difference between typical standard homes and premium/larger properties:
*   **Group A (Standard):** Area < 5,000 sqft & No Preferred Area (`prefarea` = 'no')
    *   **Average Price:** **3,827,671.56**
*   **Group B (Premium):** Area > 5,000 sqft & Has Preferred Area (`prefarea` = 'yes')
    *   **Average Price:** **6,546,807.69**
*   **Price Gap:** **2,719,136.13** (An increase of ~71%)

---

## 📁 Project Structure

```
AI Minor Project/
│
├── Housing.csv               # Dataset containing raw housing properties
├── Minor.ipynb               # Jupyter notebook with analysis code & inline plots
├── README.md                 # Project documentation and summary
└── Major Project - python.docx # Accompanying project specification/report
```

---

## 🚀 Getting Started & Installation

### Prerequisites
Make sure you have the following packages installed:
*   Python 3.8+
*   Pandas
*   Matplotlib
*   Seaborn
*   Jupyter Notebook / JupyterLab

### Quick Start
1.  Clone or navigate to the project directory:
    ```bash
    cd "AI Minor Project"
    ```
2.  Install dependencies:
    ```bash
    pip install pandas matplotlib seaborn jupyter
    ```
3.  Launch Jupyter notebook:
    ```bash
    jupyter notebook Minor.ipynb
    ```
4.  Run all cells to execute the analysis and view generated plots.

---

## 🛠️ Technology Stack
*   **Language:** Python 3.13
*   **Data Manipulation:** Pandas
*   **Data Visualization:** Matplotlib & Seaborn
*   **Interactive Workspace:** Jupyter Notebook

---

## 💡 Summary of Insights
1.  **Affordable Segment Dominance:** The 26-50L segment accounts for **58.2%** of the housing options, highlighting that the dataset represents a primarily mid-tier housing market.
2.  **AC Utility Premium:** The inclusion of Air Conditioning is associated with an average price increase of **~43.4%** (~18.2 Lakhs).
3.  **Preferred Area Valuation:** Properties that are both spacious (>5000 sqft) and situated in preferred neighborhoods (Group B) command a substantial premium (~27.2 Lakhs more) compared to smaller, standard properties (Group A).
