# 🌲 Forest Cover Type Classification

## 📝 **Project Overview**
This project predicts the **type of forest cover** (tree type) based on various geographical and environmental factors using **supervised machine learning models**.  
It compares the performance of three classifiers:  
- Logistic Regression  
- Decision Tree  
- Random Forest  

The goal is to find the most accurate model for classifying forest cover types using real-world forest data.

---

## 🎯 **Objectives**
- Load and clean the **Forest Types Dataset**.  
- Split the data into training and testing sets.  
- Train and evaluate multiple classification algorithms.  
- Compare models using **accuracy** and **confusion matrix**.  

---

## 🌍 **Dataset Information**
**Dataset:** `Forest Types Dataset.csv`  

Each row represents a geographical observation with environmental attributes and a target variable `Cover_Type` (the type of forest cover).  

| Feature | Description |
|----------|-------------|
| Elevation | Height above sea level |
| Aspect | Compass direction of slope |
| Slope | Degree of incline |
| Horizontal_Distance_To_Hydrology | Distance to nearest water body |
| Vertical_Distance_To_Hydrology | Height difference from water source |
| Horizontal_Distance_To_Roadways | Distance to nearest road |
| Hillshade_9am / Noon / 3pm | Amount of sunlight at specific times |
| Soil_Type | Type of soil |
| Wilderness_Area | Wilderness zone type |
| Cover_Type | **Target variable** (forest type to predict) |

---

## 🧰 **Libraries Used**
- **Pandas** → Data handling  
- **Scikit-learn (sklearn)** → ML algorithms & metrics  

---

## ⚙️ **Steps in the Project**

1. **Data Loading & Inspection**
   - Read the dataset using `pandas`.
   - Checked for missing values using `df.isnull().sum()`.

2. **Feature Preparation**
   - Dropped the target column `Cover_Type` from feature matrix `x`.  
   - Adjusted labels by subtracting 1 to start class indices from zero.  
   - Split data into training and testing sets (70% / 30%).

3. **Model Training & Evaluation**
   - **Logistic Regression**: Trained with `max_iter=1000`.  
   - **Decision Tree**: Used default parameters with a fixed random state.  
   - **Random Forest**: Combined multiple decision trees for better accuracy.  

4. **Model Comparison**
   - Printed **accuracy scores** for each model.  
   - Generated **confusion matrices** using `confusion_matrix()` for visual evaluation.

---

## 📈 **Results Example**
| Model | Accuracy | Notes |
|--------|-----------|-------|
| Logistic Regression | ~70–80% | Works well but limited with complex patterns |
| Decision Tree | ~85–90% | Handles non-linear features well |
| Random Forest | **90%+** | Best performance due to ensemble learning |

*(Actual results depend on dataset distribution.)*

---

## 🚀 **Future Improvements**
- Perform **hyperparameter tuning** using GridSearchCV.  
- Add **feature importance analysis** to understand key predictors.  
- Include **XGBoost** for performance comparison.  



 

---
