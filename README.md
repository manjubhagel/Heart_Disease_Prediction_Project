# Heart Disease Prediction

## Major Project - Machine Learning

This project develops a machine learning model to predict whether a patient is likely to have heart disease based on clinical and health-related features.

## Objective

The main objective is to develop a complete machine learning pipeline including:

- Data cleaning
- Handling missing values
- Feature encoding
- Feature scaling
- Model training
- Model evaluation
- Confusion matrix visualization
- ROC curve visualization
- Heart disease prediction

## Dataset

The project uses the Heart Disease UCI dataset obtained from Kaggle.

The original dataset contains the following columns:

- `id` - Patient identifier
- `age` - Age of the patient
- `sex` - Sex of the patient
- `dataset` - Dataset/source category
- `cp` - Chest pain type
- `trestbps` - Resting blood pressure
- `chol` - Serum cholesterol
- `fbs` - Fasting blood sugar
- `restecg` - Resting electrocardiographic results
- `thalch` - Maximum heart rate achieved
- `exang` - Exercise-induced angina
- `oldpeak` - ST depression induced by exercise
- `slope` - Slope of the peak exercise ST segment
- `ca` - Number of major vessels
- `thal` - Thalassemia
- `num` - Heart disease diagnosis/target variable

Here, `num` is the target variable used for heart disease prediction.
  
## Data Preprocessing

The following preprocessing steps were performed:

1. Removed unnecessary `id` and `dataset` columns.
2. Handled missing numerical values using median imputation.
3. Handled missing categorical values using mode imputation.
4. Retained the `ca` feature and handled its missing values using median imputation.
5. Converted the target variable `num` into binary classification:
   - `0` = No Heart Disease
   - `1` = Heart Disease
6. Applied one-hot encoding to categorical features.
7. Split the data into training and testing sets.
8. Applied StandardScaler for feature scaling.

## Dataset Summary

- Total records: 920
- Original columns: 16
- Features used after preprocessing: 18
- Target variable: `num`
- Training/testing split: 80% / 20%

## Machine Learning Models

Two classification algorithms were trained:

### 1. Logistic Regression

### 2. Decision Tree

## Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- Confusion Matrix
- ROC Curve
- ROC-AUC Score

## Results

| Model | Accuracy | Precision | Recall |
|---|---:|---:|---:|
| Logistic Regression | 84.24% | 84.11% | 88.24% |
| Decision Tree | 78.26% | 80.39% | 80.39% |

### Logistic Regression ROC-AUC

**ROC-AUC Score: 90.32%**

Logistic Regression performed better than the Decision Tree on the evaluated test set and was selected as the final model.

## Visualizations

The project includes:

- Model performance comparison
- Confusion matrix
- ROC curve

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Files

- `Heart_Disease_Prediction_Project.ipynb` - Complete machine learning notebook
- `heart_disease_uci.csv` - Original dataset
- `heart_disease_predictions.csv` - Actual and predicted results

## Conclusion

A complete machine learning pipeline was developed for heart disease prediction.

Logistic Regression achieved an accuracy of 84.24%, precision of 84.11%, recall of 88.24%, and a ROC-AUC score of 0.9032 on the test set.

The results demonstrate that the model was able to distinguish between the two target classes reasonably well on this dataset.

This project is intended for educational purposes and should not be considered a medical diagnostic system.
