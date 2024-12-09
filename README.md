### README: Exploring Determinants of H1N1 Vaccine Uptake - A Data-Driven Public Health Approach Using Classification Models

#### Overview

1. **Background Information**

   **1.1 What Happened in 2009 that Shook the World?**

In early 2009, the H1N1 virus, or Swine Flu, was detected in Mexico and spread globally due to international travel, prompting the World Health Organization (WHO) to declare it a pandemic. This strain, a unique mix of human, swine, and avian influenza A viruses, led to an estimated 284,400 deaths worldwide. While children and young adults were most affected, severe complications and fatalities were more common in vulnerable groups such as pregnant women, those with morbid obesity, and individuals with underlying health conditions.

   **1.2 What is H1N1 Flu?**

H1N1, or swine flu, is a strain of influenza A that causes symptoms like fever, muscle aches, cough, sore throat, and fatigue. Most people recover on their own, but complications can be severe and even fatal, particularly for high-risk individuals. Over time, H1N1 became a part of the seasonal flu, and the flu vaccine now protects against it and other flu strains.

2. **Problem Statement**

Immunization is a key tool in managing the spread of influenza, and as demonstrated during the COVID-19 pandemic, vaccination decisions are shaped by various factors such as personal background, health behaviors, and attitudes toward vaccines. The National 2009 H1N1 Flu Survey provides valuable data for understanding these influences and can guide public health experts in enhancing vaccination outreach and strategies.

3. ## 3. Objectives 

* Build a predictive model to accurately forecast H1N1 vaccination status based on various features like concerns, health behaviors, and demographics.
* Analyze factors influencing vaccination decisions using visualizations to understand behavior patterns.
* Evaluate the model and provide actionable insights to improve public health vaccination strategies.


### Model Evaluation and Recommendation

This document summarizes the evaluation of three machine learning models—**Logistic Regression**, **Decision Tree Classifier**, and **Random Forest Classifier**—for predicting vaccination status. The models were assessed using key metrics such as **accuracy**, **precision**, **recall**, **F1 score**, and **AUC-ROC**.

#### Model Performance Summary:

- **Logistic Regression:**
  - **Accuracy**: 0.75 (Within acceptable range but not exceptional)
  - **Precision**: 0.77 (Below target, indicating some false positives)
  - **Recall**: 0.73 (Indicating missed vaccinated individuals)
  - **F1 Score**: 0.75 (Balanced but can be improved)
  - **AUC-ROC Score**: 0.828 (Close to the benchmark but room for improvement)
  - **Conclusion**: Performs moderately well but struggles with class imbalance. Not the best option for high precision and recall.

- **Decision Tree Classifier:**
  - **Accuracy**: 0.83 (Above benchmark)
  - **Precision (Class 1)**: 0.87 (Strong precision for vaccinated individuals)
  - **Recall**: 0.83 (Good balance)
  - **F1 Score**: 0.83 (Good overall balance)
  - **AUC-ROC Score**: 0.896 (Exceeds 0.85 benchmark, strong separability between classes)
  - **Conclusion**: Strong performance with a good balance between precision, recall, and accuracy. The best model overall for identifying vaccinated individuals.

- **Random Forest Classifier:**
  - **Accuracy**: 0.83 (Solid performance)
  - **Precision (Class 1)**: 0.69 (Indicating many false positives for the vaccinated class)
  - **Recall**: 0.38 (Low recall for vaccinated individuals, critical issue)
  - **F1 Score**: 0.81 (Weighed down by low recall for Class 1)
  - **AUC-ROC Score**: 0.800 (Below the 0.85 benchmark)
  - **Conclusion**: While offering good precision for one class, Random Forest struggles with recall for the vaccinated class, leading to a significant number of false negatives.

#### Recommended Model:

- **Decision Tree Classifier** is the best choice. It provides a strong balance across key metrics and performs well in identifying vaccinated individuals while minimizing false positives and negatives. The AUC-ROC score of 0.896 is particularly notable, demonstrating excellent class separation.

#### Next Steps:
- **Hyperparameter tuning**: Further optimize the Decision Tree and Random Forest models for better performance.
- **Explore Gradient Boosting or XGBoost**: These models could potentially improve performance.
- **Feature Engineering**: Enhance model performance by creating or modifying features that better capture key relationships.
- **Model Interpretability**: Use tools like SHAP or LIME to understand feature importance.
- **Deployment and Monitoring**: Deploy the chosen model and continuously monitor and retrain to ensure its accuracy over time.
