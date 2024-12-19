
# California Housing Dataset: Linear Regression Analysis  

## **Overview**  
This project involves building predictive models for California housing prices using the **California Housing Dataset**. The primary goal was to explore the performance of linear regression models with original features, higher-order variables, and feature extraction using **Principal Component Analysis (PCA)**.  

The analysis demonstrates the impact of dimensionality reduction and feature selection on the model's accuracy and generalization.  

---

## **Dataset Description**  
The dataset consists of 20,640 rows, with each row representing a district in California. Key features include housing-related metrics, demographic details, and geographic information. The target variable is `median_house_value`.  

### Features  
The dataset includes:  
- **Numerical Features**:  
  `longitude`, `latitude`, `housing_median_age`, `total_rooms`, `total_bedrooms`, `population`, `households`, `median_income`  
- **Categorical Feature**:  
  `ocean_proximity`  
- **Target Variable**:  
  `median_house_value`  

---

## **Objective**  
The project aims to:  
1. Build a baseline linear regression model with the original dataset.  
2. Evaluate the impact of adding higher-order variables on model performance.  
3. Use **PCA** for feature extraction to reduce dimensionality while retaining key information.  
4. Compare model performance before and after feature extraction.  

---

## **Results and Analysis**  

### **Baseline Model (Before Feature Extraction)**  
- **Train Data**:  
  - RMSE: **69,270.86**  
  - R²: **0.6396**  
- **Test Data**:  
  - RMSE: **73,644.83**  
  - R²: **0.5933**  

### **After Feature Extraction (8 Features)**  
- **Train Data**:  
  - RMSE: **69,378.25**  
  - R²: **0.6385**  
- **Test Data**:  
  - RMSE: **72,326.46**  
  - R²: **0.6077**  

**Observations:**  
- Dimensionality reduction to 8 features improved the test RMSE by approximately **1.8%**.  
- The test R² improved from **0.5933** to **0.6077**, indicating better generalization.  

### **After Feature Extraction (6 Features)**  
- **Train Data**:  
  - RMSE: **77,932.93**  
  - R²: **0.5438**  
- **Test Data**:  
  - RMSE: **80,440.56**  
  - R²: **0.5148**  

**Observations:**  
- Reducing to 6 features resulted in underfitting.  
- The test RMSE increased significantly, and R² dropped to **0.5148**, suggesting a loss of essential information.

---

## **Conclusion**  
1. **Feature extraction using PCA with 8 features** provided the best balance of dimensionality reduction and performance.  
2. Reducing to 6 features led to a significant performance drop due to underfitting.  
3. The best-performing model achieved:  
   - RMSE: **72,326.46**  
   - R²: **0.6077** on test data.  

---

## **Recommendations**  
- Retain the model with **8 features** for optimal performance.  
- Consider exploring other feature selection techniques.  
- Perform further analysis on PCA components to interpret which features are most influential.  

---

## **How to Use This Project**  
1. **Dataset**: Download the California Housing Dataset from [Scikit-learn's datasets module](https://scikit-learn.org/stable/datasets/real_world.html#california-housing-dataset).  
2. **Model Implementation**: The analysis was performed using Python and libraries like `scikit-learn`, `numpy`, and `pandas`.  
3. **Code**: Clone this repository and run the provided Jupyter Notebook to reproduce the results.  

---

## **Future Work**  
- Explore non-linear models like Decision Trees, Random Forests, or Gradient Boosting for comparison.  
- Investigate the effect of hyperparameter tuning on model performance.  
- Analyze feature importance to determine key drivers of housing prices.  
