# Project_Phase_3

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


4. **Metrics for Success**
   - **Accuracy**: The proportion of correct predictions for vaccination status.
   - **Precision**: The ability to correctly identify vaccinated individuals.
   - **Recall (Sensitivity)**: The model’s ability to identify all vaccinated individuals.
   - **F1 Score**: A balance between precision and recall, useful in the case of imbalanced datasets.
   - **Area Under the ROC Curve (AUC-ROC)**: The model's overall ability to differentiate between vaccinated and unvaccinated individuals.
  
   - This project explores predictive modeling using logistic regression and decision tree classifiers. The goal is to predict vaccination status effectively, using key evaluation metrics like accuracy, precision, recall, F1 score, and AUC-ROC. Here is a summary of the findings:

Model Evaluation
Logistic Regression:

Accuracy: 75.49% (Good but not optimal for imbalanced data).
Precision: 0.74 (class 0), 0.77 (class 1) – below the target of 80%.
Recall: 0.78 (class 0), 0.73 (class 1) – misses some true positive cases.
F1 Score: 0.76 for both classes – moderate balance between precision and recall.
AUC-ROC: 0.828 – performs reasonably well in distinguishing between classes.
Decision Tree:

Accuracy: 82.84% (Excellent performance).
Precision: 0.79 (class 0), 0.87 (class 1) – surpasses the target for class 1.
Recall: 0.89 (class 0), 0.77 (class 1) – strong overall but slightly below target for class 1.
F1 Score: 0.84 (class 0), 0.82 (class 1) – good balance and exceeds target.
AUC-ROC: 0.896 – outstanding ability to distinguish between classes.
Conclusion
The decision tree outperforms logistic regression across all evaluation metrics, making it the preferred model for this dataset. Further optimization of logistic regression could improve its performance, especially for imbalanced datasets.
