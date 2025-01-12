# Lyft_Uber_Price_Prediction
# Optimizing Ride-Sharing Pricing with Predictive Analytics

## **Project Overview**  
The aim of this project is to understand and optimize pricing strategies for ride-sharing services such as Uber and Lyft by identifying key factors affecting price variations and demand patterns. By leveraging data science techniques, we aim to uncover temporal, geographic, and weather-related demand patterns and develop predictive models to enhance resource allocation and pricing.

---

## **Objective**
- To identify key factors influencing ride-sharing pricing and demand patterns.
- To build predictive models for optimizing pricing and resource allocation strategies.

---

## **Methodology**

### 1. Data Collection and Cleaning
- Datasets included historical ride data with variables such as distance, timestamp, weather conditions (pressure, temperature, wind), surge multiplier, and ride type.
- Performed data cleaning to handle missing values and normalize numerical features.

### 2. Exploratory Data Analysis (EDA)
- Generated heatmaps to explore correlations between features.
- Identified significant variables such as distance, time of day, and weather conditions (source/destination pressure and temperature) affecting ride prices.
- Conducted temporal analysis to detect trends across different times of the day, weekdays, and special events.

### 3. Feature Engineering
- Created new features, such as `hour_of_day`, `is_weekend`, and `weather_categories` (e.g., high pressure, wind).
- Grouped rides into peak and off-peak hours to observe demand fluctuations.

### 4. Model Development
- Built regression models (Linear Regression, Ridge, Lasso, Decision Tree, Random Forest, Neural Networks, and XGBoost) to predict ride prices.
- Evaluated models using R-squared, MAE, and RMSE scores.
- **Best Model:** Random Forest, achieving ~90% variance explanation due to its ability to handle non-linear relationships.

### 5. Insights Derived
#### Pricing Factors
- Distance is a primary factor affecting ride prices.
- Weather (e.g., pressure and wind) showed weak correlation but was included to capture potential outliers.

#### Temporal Patterns
- Surge pricing increases significantly during late evenings (especially between 10 PM and 2 AM).
- Mondays and Tuesdays had higher average ride prices, while weekends showed relatively lower surges.

#### Service Comparisons
- Lyft rides for shorter distances are cheaper compared to Uber.
- Uber offers competitive pricing for longer rides but spikes during peak hours.

#### Geographic Patterns
- Rides originating from financial districts and universities had higher average prices due to increased demand.

---

## **Key Visualizations**
- Correlation heatmaps identifying relationships between variables.
- Line charts showing average ride price variations with distance, time of day, and pressure.
- Bar charts comparing surge multipliers by cab type and time of day.
- Accuracy comparison of predictive models through R-squared visualizations.

---

## **Model Performance**
- **Random Forest:** R² = 0.90 (Best performing model due to robust handling of non-linearity).
- Neural Networks and XGBoost also performed well but required hyperparameter tuning.
- Linear and Lasso regressions showed lower accuracy due to linear assumptions.

---

## **Recommendations and Business Implications**

### 1. Pricing Strategy
- Implement dynamic pricing that adjusts based on predicted demand surges during late-night hours and weekday commutes.
- Introduce distance-based fare reductions to remain competitive for longer rides.

### 2. Resource Allocation
- Increase driver availability in high-demand zones (e.g., universities, financial districts) during peak times to reduce wait times and surge.

### 3. Promotions
- Provide promotional discounts during non-peak hours to balance demand throughout the day.

### 4. Event Planning
- Monitor and prepare for increased demand during local events (e.g., sports matches, concerts).

---

## **Next Steps**
1. **Integration of External Data:**
   - Incorporate real-time traffic and event data to improve prediction accuracy.
2. **Deploy Predictive Models:**
   - Implement the Random Forest model in a Streamlit application for interactive fare predictions.
3. **Monitoring and Feedback Loop:**
   - Continuously monitor model performance and retrain models with new data to improve accuracy.

---
