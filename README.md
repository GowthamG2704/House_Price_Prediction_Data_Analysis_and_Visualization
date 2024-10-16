# House Price Prediction Project Report

## Project Overview

This project focuses on predicting house prices based on several features such as square footage, geographical location (represented by latitude, longitude, and pincode), the number of rooms, house age, and other relevant factors. The main goal is to develop a predictive model that can accurately estimate house prices and provide actionable insights through data analysis and visualizations.

---

## Key Objectives

1. **Predict House Prices**: Use historical house data to build a machine learning model that predicts house prices based on different features.
2. **Analyze Feature Impact**: Identify the most important factors influencing house prices, including size, age, and location.
3. **Handle Data Preprocessing**: Perform data cleaning, outlier detection, and feature engineering to prepare the dataset for analysis.
4. **Visualization & Insights**: Use Tableau to visualize the relationships between features and house prices, providing easy-to-understand insights.

---

## Dataset Details

The dataset used for this project includes the following key features:

- **Price**: The target variable representing the house price.
- **Gr_Liv_Area**: The above-ground living area in square feet.
- **Latitude & Longitude**: The geographical coordinates of the house.
- **Pincode**: The postal code of the house, used to categorize the location.
- **Year_Built**: The year the house was constructed.
- **Other Features**: Including the number of bedrooms, bathrooms, and additional house attributes like garage space.

---

## Project Workflow

### 1. **Data Collection**
The dataset was collected from a reliable source containing information on house prices and associated features. The dataset included **no null values**, ensuring clean data from the start.

### 2. **Feature Engineering**
- Created new features, such as `Price_per_sqft` to better understand the price dynamics in relation to the size of the house.
- Derived the `House_Age` feature from the `Year_Built` column to account for depreciation over time.

### 3. **Outlier Detection and Handling**
Outliers in the house price were detected and handled to improve model accuracy. By replacing extreme values with more representative ones (such as the mean or median), the dataset was normalized, ensuring a more robust predictive model.

### 4. **Model Development**
Several machine learning models were evaluated, including:
- **Linear Regression**
- **Ridge Regression**
- **Lasso Regression**
- **XGBoost Regression** (Best Performing Model)

Cross-validation was used to select the best model, and hyperparameter tuning was performed to improve the model's accuracy.

### 5. **Model Fine-Tuning**
The best model, **XGBoost**, was further fine-tuned to optimize its performance. The following metrics were used to evaluate the model:
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**

After tuning, the model's performance was significantly improved, achieving an RMSE of **30,385.26** on the test set.

### 6. **Feature Importance Analysis**
To understand the most important factors affecting house prices, **SHAP (SHapley Additive exPlanations)** was used to analyze feature importance. This analysis provided valuable insights into how different features impact the model's predictions, enabling better decision-making.

---

## Visualization and Insights

The project’s insights were visualized using **Tableau**. Key charts created for the dashboard include:

1. **Heatmap**: Showing price variations across different locations using latitude, longitude, and pincode data.
2. **Bar Plot**: Comparing average house prices across different pincode areas to highlight high and low-value neighborhoods.
3. **Scatter Plot**: Analyzing the relationship between house prices and key features such as living area (square footage) and the number of rooms.
4. **Line Chart**: Tracking price trends over time based on the house's age, providing a view of how house value changes as it ages.
5. **Box Plot**: Displaying price distribution across different house sizes and neighborhoods to identify any outliers or anomalies in pricing.

   **Tableau Dashboard Link** : https://public.tableau.com/app/profile/gowtham.g8004/viz/HousePricePrediction_17290590233840/Dashboard2#1

---

## Key Insights

- **Living Area Impact**: The size of the house (Gr_Liv_Area) was found to be one of the most significant features impacting house prices. Larger houses tended to have higher prices.
- **Geographical Location**: Location-based features (latitude, longitude, pincode) played a crucial role in predicting prices, with certain regions showing consistently higher prices.
- **House Age**: Older houses generally had lower prices, but in some areas, historical properties commanded higher prices depending on location.
- **Outlier Handling**: Removing or adjusting outliers significantly improved the predictive performance of the model.
  
---

## Future Predictions

The final model was used to predict future house prices based on current market trends and provided feature values (e.g., square footage, location). This predictive capability allows for strategic planning and better decision-making in property investment.

---

## Tools and Technologies

- **Python**: For data processing, model development, and analysis.
- **Scikit-learn**: For model training and evaluation.
- **XGBoost**: Used as the primary regression model.
- **SHAP**: For feature importance analysis.
- **Tableau**: For data visualization and dashboard creation.
- **Pandas and NumPy**: For data manipulation.
- **Matplotlib and Seaborn**: For creating exploratory visualizations.

---

## Conclusion

This project successfully developed a machine learning model to predict house prices with a high degree of accuracy. The insights gained from feature importance and visual analysis can aid stakeholders in making informed decisions on property pricing, investment opportunities, and market trends.

By combining predictive modeling and interactive visualizations, this project provides a comprehensive solution to understanding house price dynamics.

---

## Future Work

For further improvement:
- **Enhance Feature Set**: Incorporate additional location-based features such as neighborhood demographics or proximity to amenities.
- **Time Series Analysis**: Explore house price trends over time to capture temporal effects on pricing.
- **Expand Data**: Add more data points to improve the model’s generalizability across different regions.
