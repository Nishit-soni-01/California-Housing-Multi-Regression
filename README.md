# California Housing Price Prediction (Multiple Linear Regression)

## Project Overview
This project implements a **Multiple Linear Regression** model to predict the median house value in California districts using the 1990 U.S. Census data. By analyzing economic, demographic, and geographic factors, the model identifies key drivers of property values across the state.

## Dataset Characteristics
The dataset consists of **20,640 instances** with the following predictive attributes:
* **MedInc**: Median income in block group
* **HouseAge**: Median house age in block group
* **AveRooms**: Average number of rooms per household
* **AveBedrms**: Average number of bedrooms per household
* **Population**: Block group population
* **AveOccup**: Average number of household members
* **Latitude & Longitude**: Geographic coordinates

**Target Variable:**
* **Median House Value**: Expressed in units of $100,000.

## Exploratory Data Analysis (EDA)
### 1. Geospatial Distribution
By plotting Latitude and Longitude, we can see the geographic density and how pricing trends correlate with location (coastal vs. inland).

<img width="889" height="702" alt="Screenshot 2026-02-21 155556" src="https://github.com/user-attachments/assets/ca0425df-890e-4048-8d8b-4b0881524142" />


### 2. Correlation & Multicollinearity
I implemented a correlation heatmap to detect **Multicollinearity**. This ensures that independent variables like `AveRooms` and `AveBedrms` do not negatively impact model stability.

<img width="984" height="685" alt="Screenshot 2026-02-21 155626" src="https://github.com/user-attachments/assets/b64f2ade-bf84-408b-a48b-aa0dc9c6b176" />


### 3. Error Analysis (Residuals)
Checking the distribution of residuals helps confirm the model's assumptions. A normal distribution of errors indicates that the Linear Regression model is appropriate for this data.

<img width="493" height="492" alt="Screenshot 2026-02-21 155640" src="https://github.com/user-attachments/assets/a5d85556-aa13-48ef-81c2-1cb4139f74d5" />


## Data Cleaning & Preprocessing
* **Outlier Filtering**: Based on dataset documentation, extreme values in `AveRooms` and `AveOccup` (often caused by vacation resorts) were filtered to improve model accuracy.
* **Feature Scaling**: Applied `StandardScaler` to normalize features for consistent weight distribution.

## Model Performance
* **R-Squared**: ~0.60 (varies based on split)
* **Algorithm**: Multiple Linear Regression via `scikit-learn`.

## Technologies Used
* **Python** (Pandas, NumPy)
* **Visualization**: Matplotlib, Seaborn
* **Machine Learning**: Scikit-Learn
