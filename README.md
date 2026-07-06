# Online Shoppers Customer Intention Prediction
![Python](https://img.shields.io/badge/Python-3.12-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green)
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

# 🛒 Online Shoppers Purchase Intention Prediction

Machine Learning project that predicts whether an online shopper will make a purchase based on browsing behavior using classification algorithms.

### About Dataset
This dataset was sourced from Kaggle. It contains 18 columns and 12,330 rows.

## Table of Contents

- About
- Project Overview
- Business Problem
- Dataset
- EDA
- Feature Engineering
- Models
- Results
- Recommendations
- Conclusion

### Project Overview

This project analyzes online shopping behavior and develops machine learning models to predict whether a visitor will make a purchase. Understanding purchase intent can help businesses improve marketing strategies, personalize user experiences, and increase conversion rates.

The goal of this project was to develop a predictive model that accurately identifies customers who are more likely to complete a purchase based on their browsing behavior.

### Business Problem

E-commerce platforms receive thousands of visitors daily, but only a small percentage complete a purchase. Businesses need a way to identify high-intent visitors in order to:

 - Improve targeted marketing
 - Optimize advertising spend
 - Personalize user experiences
 - Increase conversion rates

This project uses historical user session data to predict purchase behavior.

### Dataset

The dataset used is the  <a href=  "https://www.kaggle.com/datasets/imakash3011/online-shoppers-purchasing-intention-dataset">Online Shoppers Purchasing Intention Dataset</a> which contains session-based information about visitors on an e-commerce website.

Key features include:
 - Administrative pages visited
 - Product-related pages
 - Bounce rate
 - Exit rate
 - Page value
 - Traffic type
 - Visitor type
 - Month of visit


The target variable is:

### Revenue

 - 0 → No purchase

 - 1 → Purchase made


### Project Workflow
1. Data Cleaning

 - Loaded the dataset using Pandas
 - Checked for missing values
 - Converted categorical variables to numerical values
 - Encoded categorical columns

2. Exploratory Data Analysis
EDA was performed to understand user behavior patterns.

### Correlation Heatmap

<img width="846" height="621" alt="Screenshot (821)" src="https://github.com/user-attachments/assets/b03ddbc1-2db8-4554-829f-8db478b2289c" />

### Confusion Matrix

<img width="682" height="482" alt="Screenshot (855)" src="https://github.com/user-attachments/assets/c9a3b5c7-a220-46ed-a6d5-92d9e7d641ef" />

### XGB_Boost

<img width="626" height="469" alt="Screenshot (856)" src="https://github.com/user-attachments/assets/96c2a25f-6416-4afa-acf6-4cb315fe62c4" />

### Feature_Importance

<img width="1137" height="606" alt="Screenshot (860)" src="https://github.com/user-attachments/assets/dc2728e8-0e5f-46e6-b03b-0952c040e5f6" />


Using Seaborn and Matplotlib,

```bash
conda install seaborn
```

```bash
pip install matplotlib
```

  several visualizations were created to explore relationships between features and customer purchase behavior.:

 - Correlation heatmaps

 - Feature distribution analysis

 - Visitor behavior patterns

Customer-Purchase-Prediction/

│
├── data/
├── notebook/
├── images/
├── README.md
├── requirements.txt
└── customer_purchase_prediction.ipynb
3. Feature Engineering

 - Encoded categorical variables such as Month, VisitorType, and Weekend

 - Separated the dataset into features (X) and target variable (y)

 - Split the data into training and testing sets

4. Machine Learning Models

  - Several machine learning models were tested using Scikit-learn and XGBoost:

  - Logistic Regression

  - Linear Regression

  - XGBoost Classifier

Each model was evaluated using classification metrics.

### Model Performance

Best performing model: Logistic Regression

Accuracy: 89%

Classification report:

| Class | Precision | Recall | F1 Score |
|------|------|------|------|
| No Purchase | 0.91 | 0.96 | 0.94 |
| Purchase | 0.75 | 0.55 | 0.63 |

### Confusion Matrix:

 - True Negatives: 1978

 - False Positives: 77

 - False Negatives: 184

 - True Positives: 227
   
|     | Predicted No Purchase | Predicted Purchase |
|:------|:-------:|------:|
| Actual No Purchase | 1978 | 77 |
| Actual Purchase | 184 | 227 |

Logistic Regression generalized better on unseen data and achieved the best balance between precision and recall. Its simplicity also makes it easier to interpret and deploy compared with more complex ensemble models.

The model performs very well in identifying non-purchasing visitors, while performance on predicting purchasing visitors is moderate due to data imbalance.

## Future Work

- Hyperparameter tuning
- Cross-validation
- SMOTE for class imbalance
- Streamlit deployment
- Feature selection
- Model monitoring

### Tools & Technologies
 - Python
 - Pandas
 - NumPy
 - Matplotlib
 - Seaborn
 - Scikit-learn
 - XGBoost
 - Jupyter Notebook

## Installation

```bash
git clone https://github.com/Helen2000-analyst/Customer-Purchase-Prediction.git

cd Customer-Purchase-Prediction

pip install -r requirements.txt
```

python prediction.py

## License

This project is licensed under the MIT License.



### Key Insights

 - Visitors who view more product-related pages are more likely to make purchases.

 - Page value has strong influence on purchase behavior.

 - Returning visitors tend to have higher purchase probability.

 - Session behavior patterns can strongly indicate purchase intent.

### Results & Model Comparison

 Model Evaluation Overview

Four classification models were evaluated to predict customer purchase intent:

 - Logistic Regression

 - Random Forest Classifier

 - XGBoost Classifier

 - Random Forest Regression

Model performance was assessed using:

 - Accuracy

 - Precision

 - Recall

 - F1-Score

 - Confusion Matrix

Given the class imbalance in the dataset (fewer purchasing customers than non-purchasing customers), special attention was paid to recall and F1-score for the purchasing class.

### Logistic Regression Performance (Best Model)

Logistic Regression achieved the strongest overall performance.

Accuracy: 89.4%

Confusion Matrix:

 - True Negatives: 1978

 - False Positives: 77

 - False Negatives: 184

 - True Positives: 227

The model performs exceptionally well in identifying non-purchasing customers, achieving 96% recall. This makes it highly effective at reducing wasted marketing spend.

For purchasing customers, the model achieves 75% precision, meaning when it predicts a purchase, it is correct 75% of the time. However, recall for purchasers is 55%, indicating that some potential buyers remain undetected.

Despite this limitation, Logistic Regression delivered the most balanced and stable performance among all evaluated models.

### Random Forest & XGBoost Comparison

Although Random Forest and XGBoost are more complex ensemble models capable of capturing nonlinear relationships, they did not outperform Logistic Regression in overall predictive performance.

This suggests that customer purchase behavior in this dataset follows structured, linearly separable patterns rather than highly complex nonlinear interactions.

While ensemble models showed competitive accuracy, they did not significantly improve recall or F1-score for the purchasing class.

### Key Insights from Model Comparison

1. Simpler models can outperform complex models when data relationships are structured.

2. Logistic Regression provides better interpretability, which is valuable for business decision-making.

3. The primary performance limitation across models was moderate recall for purchasing customers.

4. The dataset is imbalanced, influencing predictive performance.

### Business Implications

The selected Logistic Regression model provides strong capability for:

 - Identifying high-probability buyers

 - Reducing unnecessary advertising spend

 - Supporting targeted marketing campaigns

 - Improving return on marketing investment

To further enhance revenue capture, future optimization could focus on increasing recall for the purchasing class by adjusting classification thresholds or applying class balancing techniques.

### Final Model Selection

Based on comparative evaluation, Logistic Regression was selected as the final model due to:

 - Highest overall predictive performance

 - Strong precision and stability

 - Simplicity and ease of deployment

 - High interpretability for stakeholders

This model provides a reliable foundation for implementing predictive marketing strategies in an e-commerce environment.

### Recommendations

Based on the analysis and model results, several strategic recommendations can help improve purchase conversion rates on e-commerce platforms.

1. Target High-Intent Visitors

Users who browse a higher number of product-related pages demonstrate stronger purchase intent. Businesses should implement personalized promotions or targeted ads for these users to encourage purchase completion.

2. Enhance Product Page Experience

Since product-related pages strongly influence purchase behavior, improving product page design, including clearer descriptions, high-quality images, and customer reviews, can help increase conversion rates.

3. Leverage Returning Visitors

The analysis indicates that returning visitors are more likely to make purchases than new visitors. Businesses should focus on retention strategies such as loyalty programs, email marketing campaigns, and personalized product recommendations.

4. Implement Real-Time Purchase Prediction

The developed model can be integrated into an e-commerce platform to identify high-purchase-intent users in real time. This allows businesses to dynamically display offers, discounts, or recommendations that increase the likelihood of purchase.

5. Improve Marketing Campaign Efficiency

By identifying users who are less likely to purchase, businesses can reduce unnecessary marketing spending and allocate advertising budgets toward high-potential customers.

6. Address Class Imbalance in Future Models

The dataset contains significantly more non-purchase sessions than purchase sessions. Future models could improve purchase prediction accuracy by applying techniques such as oversampling or class balancing methods.

### Conclusion

This project analyzed online shopper behavior to predict whether a visitor will complete a purchase. After performing exploratory data analysis and testing multiple machine learning models, Logistic Regression achieved the best performance with an accuracy of approximately 89%.

The analysis revealed that factors such as product page visits, page value, and visitor type significantly influence purchase decisions. These insights demonstrate how machine learning can help e-commerce businesses better understand customer behavior and improve marketing strategies.

Future improvements could include addressing class imbalance, tuning model parameters, and incorporating additional behavioral features to further enhance predictive performance.


## Author

Helen Ehinmisan

LinkedIn: www.linkedin.com/in/helen-ehinmisan-5b8b1b332

GitHub: https://github.com/Helen2000-analyst

Email: ehinmisanhelen2000@gmail.com
