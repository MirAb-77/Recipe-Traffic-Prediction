# 🍽️ **Recipe Traffic Prediction Using Machine Learning**

## 📊 **Project Overview**
This project leverages **machine learning** to predict whether a recipe will receive high or low traffic based on its nutritional and categorical features. Our aim is to assist businesses in identifying recipes that will attract more visitors and engagement, helping them make data-driven decisions. 

### 🔍 **Problem Statement**
The challenge is to predict high-traffic recipes with an accuracy of **80% or above**. Given the recipe’s characteristics such as calories, carbohydrates, sugar, protein, and category, can we accurately predict its traffic?

---

## 📝 **Dataset Details**

| Column Name    | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `recipe`       | Numeric, unique identifier of the recipe                                    |
| `calories`     | Numeric, number of calories per serving                                     |
| `carbohydrate` | Numeric, grams of carbohydrates                                             |
| `sugar`        | Numeric, grams of sugar                                                     |
| `protein`      | Numeric, grams of protein                                                   |
| `category`     | Categorical, one of 10 recipe categories (e.g., 'Lunch/Snacks', 'Dessert')   |
| `servings`     | Numeric, number of servings per recipe                                      |
| `high_traffic` | Categorical, whether the traffic for the recipe was "High" or not           |

---

## 🌐 **Live Demo & Webpage**

Explore the interactive **Recipe Traffic Prediction Tool** on the live webpage:

**[🔗 Recipe Prediction App]()**

This webpage allows users to input their own recipe details and get predictions on whether their recipe will generate high or low traffic based on the trained model. 🎯

### 1. Descriptive Portion
<img width="954" alt="Description_Page" src="https://github.com/user-attachments/assets/bff04ffa-b8dc-4eff-b4ff-2feaec5d5122">

### 2. Login portion
<img width="958" alt="Login_Page" src="https://github.com/user-attachments/assets/170edacd-e63d-4c31-86d1-96fbb5d0f950">

### 3. Prediction Portion
<img width="949" alt="Prediction_Page" src="https://github.com/user-attachments/assets/1bfa5006-cdcf-43d0-83e5-bbeeaeab31f0">

---

## 🚀 **Project Pipeline**

1. **Data Validation & Cleaning**
   - Ensured all columns, such as `calories`, `carbohydrates`, `sugar`, `protein`, `category`, and `high_traffic`, were validated for consistency and missing values were handled appropriately.
   - **Categorical Encoding**: The recipe categories (e.g., 'Lunch/Snacks', 'Beverages', etc.) were transformed using Label encoding to be fed into machine learning models.
   
2. **Exploratory Data Analysis (EDA)**
   - **Single Variable Analysis**: 
     - A histogram of calorie distribution to understand the spread.
     - A bar plot showcasing the frequency of each recipe category.
   - **Multivariable Analysis**: A scatter plot of calories vs. sugar, colored by high traffic, revealing potential patterns in high-traffic recipes.

3. **Model Development**
   - **Problem Type**: This is a **classification problem**, predicting high vs. low traffic.
   - **Chosen Models**:
     - **Decision Tree Classifier**: Selected for its interpretability and ease of visualizing decision-making steps.
     - **Random Forest Classifier**: Chosen for its higher accuracy, ensemble approach, and robustness in handling outliers and complex patterns.
   
4. **Model Evaluation**
   - **Decision Tree**: Provided insights but overfit to the data, limiting its generalization.
   - **Random Forest**: Outperformed the Decision Tree by aggregating predictions from multiple trees, achieving **82% accuracy**.
   - The chosen metric for evaluation: **Accuracy** and **Precision** to measure how well the model predicts high traffic.

5. **Business Metric**
   - We aimed to align our model performance with the business goal of correctly predicting high-traffic recipes **80% of the time**. Random Forest met this threshold, offering reliable predictions for future recipe selections.

---

## 🏆 **Key Findings & Recommendations**

- **Random Forest Classifier** emerged as the best model with **82% accuracy**, surpassing the Decision Tree in terms of stability and performance.
- **Important Features**: The most influential features for predicting high traffic were:
  1. **Calories**
  2. **Sugar**
  3. **Category** (specifically, `Dessert` and `Breakfast` showed strong correlations with high traffic).

### 📌 **Business Recommendations**:
- Focus on promoting **Dessert** and **Breakfast** recipes, as they tend to generate higher traffic.
- Recipes with moderate **calories** and **sugar** are more likely to attract users.

---

## 🛠️ **Technologies Used**

- **Python**: For data manipulation, analysis, and machine learning.
- **Pandas**: For data cleaning and processing.
- **Matplotlib & Seaborn**: For creating visualizations.
- **Scikit-learn**: For model building and evaluation.
- **Random Forest & Decision Tree**: Machine learning models.

---

## 📂 **Project Structure**

```bash
.
├── data
│   └── recipe_traffic.csv   # Dataset used in the project
├── scripts
│   ├── data_validation.ipynb  # Data cleaning and validation steps
│   ├── EDA.ipynb              # Exploratory Data Analysis
│   └── model_development.ipynb # Model building and evaluation
├── visuals
│   └── calorie_distribution.png
└── README.md                 # Project documentation
