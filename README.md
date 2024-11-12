# **Chocolate and Magic Mushroom Consumption Prediction**

## **Overview**  
This project analyzes chocolate and magic mushroom consumption using the UCI 2018 drug consumption dataset. The original multi-class data was transformed into binary classification tasks for both substances, and six supervised learning models were trained for each dataset. The project also addresses class imbalance through various rebalancing techniques to improve model performance.

## **Models Used**  
- **Single Decision Tree (DT)**  
- **Random Forest (RF)**  
- **Support Vector Machine (SVM)**  
- **Gradient Boosting (GB)**  
- **Multi-Layer Perceptron (MLP)**  
- **K-Nearest Neighbors (k-NN)**  

## **Dataset**  
The UCI drug consumption dataset includes various demographic, psychological, and behavioral features. The following modifications were made:  
- **Features used:** Columns 2-13  
- **Labels:**  
  - *Chocolate Consumption (Feature 20)*  
  - *Magic Mushroom Consumption (Feature 29)*  
- **Binary Label Conversion:**  
  - *Non-user*: 'Never used' and 'Used over a decade ago'  
  - *User*: All other categories  

## **Evaluation Metrics**  
- **Confusion Matrix**  
- **Precision**  
- **Recall**  
- **ROC Curve** and **Area Under the Curve (AUC)**  

## **Rebalancing Techniques**  
- **Tomek Links (Undersampling):** Reduces the majority class by removing overlapping points.  
- **SMOTE (Oversampling):** Generates synthetic samples for the minority class.  
- **Hybrid Approach:** Combines Tomek Links and SMOTE for more balanced datasets.

## **Results Summary**  
- **Chocolate Dataset:**  
  - Models exhibited high recall but overfitting due to class imbalance.  
  - **SVM** achieved the highest AUC (0.64), though other models showed limited reliability (AUC ~ 0.5).  

- **Mushroom Dataset:**  
  - Models performed better due to the more balanced distribution.  
  - **SVM** achieved the best results with an **AUC of 0.8, precision of 0.65, and recall of 0.66**.  
  - **KNN** struggled with lower precision (0.581) and recall (0.593).  

## **Impact of Rebalancing**  
- **Tomek Links:** Minimal impact on chocolate dataset due to few removed points.  
- **SMOTE:** Improved recall and reduced overfitting, with KNN achieving the highest AUC of 0.64.  
- **Hybrid Approach:** Best results for chocolate dataset, especially with **Decision Trees** and **KNN**.  

For the mushroom dataset, rebalancing showed minimal changes, with **Gradient Boosting** and **Random Forest** achieving the best balance of precision and recall. 

## **Usage Instructions**  
1. Clone the repository or download the code files.  
2. Install the required packages using:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook or Python scripts to reproduce the results.  


