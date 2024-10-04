
# Thyroid Cancer Recurrence Prediction

## Project Overview

This project is focused on predicting the recurrence of thyroid cancer using machine learning models. The target variable for prediction is **"Recurred"**, which indicates whether a patient’s thyroid tumor has recurred.

## Dataset Information

The dataset consists of patient information and medical records, including clinical, pathological, and response-related data. Below is a summary of the columns:

### Columns

1. **Age**: Age of the patient in years.
2. **Gender**: Gender of the patient (F for female, M for male).
3. **Smoking**: Indicates if the patient is currently smoking (Yes/No).
4. **Hx Smoking**: Indicates if the patient has a history of smoking (Yes/No).
5. **Hx Radiotherapy**: Indicates if the patient has a history of radiotherapy (Yes/No).
6. **Thyroid Function**: The patient's thyroid function status (e.g., Euthyroid).
7. **Physical Examination**: Results from the physical examination of the thyroid (e.g., Single nodular goiter).
8. **Adenopathy**: Presence of adenopathy (Yes/No).
9. **Pathology**: The pathology result of the thyroid (e.g., Micropapillary).
10. **Focality**: Whether the tumor is Uni-Focal or Multi-Focal.
11. **Risk**: The risk category of the patient (Low, Intermediate, High).
12. **T**: Tumor stage based on the size and extent of the primary tumor (T1a, T1b, etc.).
13. **N**: Lymph node involvement (N0, N1, etc.).
14. **M**: Distant metastasis (M0, M1, etc.).
15. **Stage**: Overall cancer stage based on TNM classification (Stage I, II, etc.).
16. **Response**: Response to treatment, categorized as Biochemical Incomplete, Excellent, Indeterminate, or Structural Incomplete.
17. **Recurred**: The target variable, indicating whether the tumor has recurred (Yes/No).

## Project Structure

- **Data Preprocessing**: Includes data cleaning, one-hot encoding for categorical variables, and splitting the data into training and testing sets.
- **Feature Selection**: Lasso regression was used for selecting important features from the dataset.
- **Modeling**: The final model chosen for prediction is **Random Forest**, as it performs well on datasets with one-hot encoded variables due to its tree-based structure.
  
## Steps for Reproducing the Project

1. **Clone the repository**:
   ```bash
   git clone <repo-link>
   cd thyroid-cancer-prediction
   ```

2. **Install required libraries**:
   The project requires the following R packages:
   - `caret`
   - `glmnet`
   - `randomForest`
   - `ggplot2`
   - `dplyr`

   You can install them using:
   ```r
   install.packages(c("caret", "glmnet", "randomForest", "ggplot2", "dplyr"))
   ```

3. **Run the project**:
   Execute the R script to preprocess the data, perform feature selection, and train the Random Forest model.

4. **Evaluation**:
   The model is evaluated on several metrics including accuracy, precision, recall, and F1 score.

## Future Work

- Tune hyperparameters of the Random Forest model to improve accuracy.
- Explore other machine learning algorithms like Support Vector Machines or Gradient Boosting for better performance.
