# Diabetes Prediction

## Project Overview
This project predicts whether a person has diabetes using machine learning models. The dataset contains numerical medical attributes, and we apply various classification algorithms to compare their performance.

## Dataset
- The dataset includes features like:
  - **Glucose level**
  - **Pregnancy**
  - **SkinThickness**
  - **Diabetes Pedigree Function**
  - **Blood pressure**
  - **Insulin level**
  - **BMI (Body Mass Index)**
  - **Age**
- The target variable is **Diabetes Outcome** (0 = No, 1 = Yes).

## Data Preprocessing
1. **Handling Missing Values**
   - Filled missing values using the median.
2. **Feature Scaling**
   - Applied **StandardScaler** to normalize numerical features.

## Machine Learning Models Used
We trained and evaluated the following classifiers:
1. **Decision Tree Classifier**
2. **Logistic Regression**
3. **Support Vector Machine (SVM)**
4. **Random Forest Classifier**
5. **KNeighborsClassifier**

## Hyperparameter Tuning
- The best-performing model was **SVM**.
- We used **RandomizedSearchCV** for hyperparameter tuning:
  - `C`: [0.01, 0.1, 1, 10, 100]
  - `kernel`: [‘linear’, ‘poly’, ‘rbf’, ‘sigmoid’]
  - `gamma`: [0.1, 1, 0.001, 0.0001]

## Model Evaluation
- Models were assessed using:
  - **Accuracy**
  - **Classification Report**

## Installation & Usage
### Requirements
```bash
pip install numpy pandas scikit-learn
```

### Run the Project
```bash
python diabetes_prediction.py
```

## Results
| Model                  | Accuracy |
|------------------------|----------|
| Decision Tree          | 74.6%    |
| Logistic Regression    | 75.3%    |
| SVM                    | **75.9%**  |
| Random Forest         | 72%    |
| KNeighborsClassifier   | 69.5%    |

## Conclusion
- **SVM achieved the highest accuracy.**
- **Feature scaling improved model performance.**
- **RandomizedSearchCV optimized SVM hyperparameters for better results.**

## Future Improvements
- Experimenting with deep learning models like Neural Networks.
- Incorporating feature selection techniques to reduce dimensionality.

---
🚀 *Happy Coding!*
