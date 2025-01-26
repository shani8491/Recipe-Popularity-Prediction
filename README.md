# Recipe-Popularity-Prediction
This project predicts recipe popularity (`low`, `medium`, or `high`) based on user engagement metrics such as thumbs up, reply count, and user reputation using machine learning techniques.
Here’s a detailed description for your README file:

---

# **Recipe Popularity Predictor**

## **Project Overview**
The **Recipe Popularity Predictor** is a machine learning project aimed at classifying recipes into three categories—**low**, **medium**, or **high** popularity—based on user engagement metrics such as thumbs up, reply count, and user reputation. The project leverages advanced data preprocessing techniques and classification algorithms to analyze patterns and provide reliable predictions of recipe popularity.

---

## **Objective**
The primary objective of this project is to predict the popularity of recipes using user interaction data. By analyzing key engagement features, the model aims to:
1. Help recipe creators understand the factors that contribute to popularity.
2. Provide actionable insights to improve recipe engagement.
3. Offer a scalable solution to predict popularity for newly added recipes.

---

## **Dataset Description**
The dataset contains information about recipes and user interactions. Below is an overview of the dataset:
- **Source**: [Specify the source, if public or private]
- **Features**:
  - `recipe_number`: Unique identifier for each recipe.
  - `recipe_code`: Code categorizing the recipe.
  - `user_reputation`: Reputation score of the user posting the recipe.
  - `created_at`: Timestamp of when the recipe was created.
  - `reply_count`: Number of replies/comments received.
  - `thumbs_up`: Count of upvotes for the recipe.
  - `thumbs_down`: Count of downvotes for the recipe.
  - `stars`: Star rating for the recipe (0-5).
  - `best_score`: A calculated engagement metric.
- **Target Variable**:
  - `stars_category`: Categorizes recipes into **low**, **medium**, or **high** popularity based on the `stars` feature.

---

## **Key Steps**
1. **Data Preprocessing**:
   - Handled missing values and identified outliers.
   - Addressed skewness using transformations such as Winsorization.
   - Balanced the dataset using **SMOTE** to handle class imbalance.

2. **Feature Engineering**:
   - Encoded categorical variables using appropriate methods.
   - Generated new features such as `log-transformed` engagement metrics for better model performance.

3. **Model Selection**:
   - Evaluated multiple classification models:
     - Logistic Regression
     - Decision Tree Classifier
     - RandomForestClassifier
     - SVM
     - GradientBoostingClassifier
   - Selected **RandomForestClassifier** as the best-performing model due to its robustness and high accuracy.

4. **Evaluation**:
   - Assessed model performance using metrics such as accuracy, confusion matrix, and classification report.
   - Used 5-fold cross-validation to ensure reliability and prevent overfitting.

---

## **Results**
- The **RandomForestClassifier** achieved high accuracy, effectively predicting recipe popularity across all categories.
- Feature importance analysis revealed that `thumbs_up`, `reply_count`, and `user_reputation` were the most influential factors in predicting popularity.
- The application of **SMOTE** improved the model’s ability to classify minority categories (`medium` and `low`) effectively.

---

## **Limitations**
1. **Imbalanced Dataset**: The original dataset had a skewed class distribution, requiring oversampling techniques.
2. **Excluded Features**: Text-based features such as `recipe_name` and `text` were not utilized, potentially leaving out valuable information.
3. **Feature Skewness**: Some features, like `thumbs_up` and `thumbs_down`, exhibited high skewness despite preprocessing.

---

## **Future Enhancements**
1. **Incorporating NLP**: Leverage text features like `recipe_name` and `text` using Natural Language Processing (NLP) techniques for better predictions.
2. **Collect More Data**: Expand the dataset to reduce class imbalance and improve generalizability.
3. **Model Optimization**: Experiment with advanced algorithms or hyperparameter tuning to further boost performance.

---

## **How to Run the Project**
1. Clone the repository:
   ```bash
   git clone <repository_url>
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Load the dataset into the notebook or script.
4. Run the pipeline to preprocess data, train the model, and evaluate predictions.

---

## **Technologies Used**
- **Programming Language**: Python
- **Libraries**:
  - Data Analysis: Pandas, NumPy
  - Visualization: Matplotlib, Seaborn
  - Machine Learning: Scikit-learn, Imbalanced-learn
  - Preprocessing: StandardScaler, SMOTE

---

## **Conclusion**
The **Recipe Popularity Predictor** provides a reliable and efficient way to predict recipe popularity using engagement data. While the project achieved promising results, future iterations will focus on incorporating additional features and optimizing models to further enhance predictions.

---

Let me know if you’d like any adjustments or additional sections for your README! 😊
