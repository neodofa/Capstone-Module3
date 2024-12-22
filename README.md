# Daegu Apartment Price Prediction

## Overview
This project is part of the Module 3 Capstone assignment, focused on predicting apartment prices in Daegu using data analysis and machine learning. The goal is to assist sellers and real estate professionals in setting competitive prices based on factors like size, location, and amenities.

## Objectives
- Analyze and preprocess the dataset to ensure it is clean and ready for modeling.
- Engineer relevant features, such as `Age`, to enhance the dataset.
- Build a machine learning model to predict apartment prices accurately.
- Evaluate the model's performance using metrics like R-squared and Root Mean Squared Error.

## Project Structure
The repository contains the following files:
- `capstone3.ipynb`: Jupyter Notebook containing all steps from data preprocessing to model evaluation.
- `cleaned_daegu_apartment.csv`: Cleaned and processed dataset used for modeling.
- `daegu_apartment_model.pkl`: Trained Random Forest Regressor model saved for future use.
- `video_link.txt`: A text file containing the link to the project presentation video.

## Key Features of the Dataset
- **Size(sqft)**: Total area of the apartment.
- **YearBuilt**: The year the apartment was constructed.
- **N_FacilitiesInApt**: Number of facilities in the apartment.
- **SubwayDist**: Distance to the nearest subway station.
- **SalePrice**: Target variable representing the price of the apartment.

## Workflow
1. **Data Preprocessing**:
   - Missing values were handled by replacing them with the median.
   - Categorical features were encoded using one-hot encoding.

2. **Feature Engineering**:
   - Created a new feature `Age` by subtracting `YearBuilt` from the current year (2024).
   - Dropped `YearBuilt` as it was redundant after creating `Age`.

3. **Modeling**:
   - Built a Random Forest Regressor to predict apartment prices.
   - Split the dataset into training (80%) and testing (20%) sets.

4. **Evaluation**:
   - The model achieved an R-squared value of **0.84**, indicating that it explains 84% of the variance in apartment prices.
   - Other metrics include:
     - Mean Absolute Error (MAE): [Insert value from notebook]
     - Root Mean Squared Error (RMSE): [Insert value from notebook]

5. **Feature Importance**:
   - The top features influencing apartment prices were `Size(sqft)`, `Age`, and `N_FacilitiesInApt`.

## Tools and Libraries
- **Python**: Programming language used for analysis and modeling.
- **Libraries**:
  - `pandas`: For data manipulation.
  - `numpy`: For numerical operations.
  - `seaborn` and `matplotlib`: For visualization.
  - `scikit-learn`: For machine learning modeling and evaluation.

## Future Improvements
- Include additional features, such as neighborhood quality or proximity to parks and schools.
- Experiment with advanced models like Gradient Boosting Machines (e.g., XGBoost) or Neural Networks.
- Perform hyperparameter tuning to optimize the Random Forest model further.
