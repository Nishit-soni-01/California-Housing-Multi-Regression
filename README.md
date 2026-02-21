# California Housing Price Prediction (Multiple Linear Regression)

## Project Overview
This project implements a **Multiple Linear Regression** model to predict the median house value in California districts. Utilizing the 1990 U.S. Census data, the model analyzes how economic factors, household characteristics, and geographic location influence property values.

## Dataset Characteristics
The dataset consists of **20,640 instances** with 8 numeric predictive attributes:
- **MedInc**: Median income in block group.
- **HouseAge**: Median house age in block group.
- **AveRooms**: Average number of rooms per household.
- **AveBedrms**: Average number of bedrooms per household.
- **Population**: Block group population.
- **AveOccup**: Average number of household members.
- **Latitude**: Block group latitude.
- **Longitude**: Block group longitude.

**Target Variable:**
- **Median House Value**: Expressed in hundreds of thousands of dollars ($100,000).

## Technical Implementation
- **Data Source**: Obtained from the StatLib repository via `sklearn.datasets`.
- **Exploratory Data Analysis (EDA)**: Investigated the surprising variance in average rooms/bedrooms and geographic clusters.
- **Feature Scaling**: Applied normalization to ensure features like `Population` do not disproportionately influence the model compared to `MedInc`.
- **Modeling**: Implemented a Multiple Linear Regression model using `scikit-learn`.



## Key Insights & Performance
- **Primary Driver**: Median Income (`MedInc`) shows the strongest positive correlation with house value.
- **Geospatial Impact**: The inclusion of `Latitude` and `Longitude` allows the model to account for location-based pricing trends (e.g., coastal vs. inland).
- **Evaluation**: The model was evaluated using R-Squared and RMSE to measure prediction accuracy against actual census values.

## Technologies Used
- **Python** (Pandas, NumPy)
- **Scikit-Learn** (Regression & Datasets)
- **Matplotlib/Seaborn** (Visualizing spatial and statistical distributions)
