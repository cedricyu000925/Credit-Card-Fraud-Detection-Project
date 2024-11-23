# Credit Card Fraud Detection Project

## Project Overview
This project addresses the critical need for detecting fraudulent credit card transactions to protect customers from unauthorized charges. Using a publicly available dataset of credit card transactions from September 2013 by European cardholders, we aim to uncover patterns in fraudulent behavior and develop a machine learning model capable of detecting future fraud.

## Dataset Summary
The dataset comprises 284,807 transactions across two days, with 492 labeled as fraudulent, making up only 0.172% of all transactions. It includes:

- **Numerical Variables:** The dataset features 28 principal components (`V1` to `V28`) obtained through PCA (Principal Component Analysis). These anonymized features ensure data confidentiality.
- **Time:** The time elapsed (in seconds) between each transaction and the first transaction in the dataset.
- **Amount:** The transaction amount, which can influence cost-sensitive analyses.
- **Class:** The target variable, where `1` indicates fraud and `0` indicates a legitimate transaction.

## Challenges
- **Imbalanced Dataset:** Fraudulent transactions form a very small portion of the dataset, making it crucial to implement strategies that effectively handle class imbalance.
- **Confidentiality:** Limited background information due to PCA transformation of features.

## Process: Step-by-Step Approach
This project was conducted in two main phases: **Exploratory Data Analysis (EDA)** and **Machine Learning Model Development**. Below is the detailed process:

1. **Understanding the Dataset:**

- Loaded the dataset and reviewed its structure (columns, data types, and target variable).
- Identified the highly imbalanced nature of the data (0.172% fraud cases).
- 
2. **Exploratory Data Analysis (EDA):**

- **Summary Statistics:**
  - Examined the distribution of features like `Time`, `Amount`, and `Class`.
  - Checked for missing or inconsistent data (none were found in this dataset).
- **Visualizations:**
  - Created histograms and boxplots to identify patterns in transaction times and amounts.
  - Used scatter plots to explore relationships between features and fraud occurrences.
- **Correlation Analysis:**
  - Investigated relationships between PCA features (`V1` to `V28`) and the likelihood of fraud.

3. **Data Preprocessing:**

- Standardized features such as `Time` and `Amount` to ensure they are on a similar scale.
- Addressed the imbalanced dataset using techniques like Synthetic Minority Oversampling Technique (SMOTE) to oversample fraud cases.

4. **Model Building:**

- **Model Selection:**
  - Experimented with multiple models, including Logistic Regression, Random Forest, and Gradient Boosting.
- **Training and Evaluation:**
  - Split the data into training and testing sets (80%-20%).
  - Used cross-validation to evaluate models and tune hyperparameters.
- **Metrics:**
  - Focused on precision, recall, and F1-score to assess model performance, given the imbalanced dataset.
  - 
5. **Findings and Insights:**

- Documented the distinct patterns of fraud occurrences and the performance of various models.
- Identified Random Forest as the best-performing model for fraud detection.

6. **Actionable Business Insights:**

- Derived insights to help businesses improve fraud detection and prevention strategies.

## Key Findings and Insights
**Fraud Detection and Correlation Analysis**
- **Fraud Timing Patterns:** Fraudulent transactions showed distinct timing patterns compared to non-fraudulent ones.
- **Transaction Amounts:** Fraudulent transactions tended to cluster within specific ranges, suggesting that transaction amount plays a significant role in identifying fraud.
- **Feature Correlations:** Analysis revealed certain features (`Vx`) with higher predictive power for detecting fraud.
**Model Building for Fraud Detection**
- **Machine Learning Approach:**
  - Techniques like Random Forest and Logistic Regression were employed.
  - Resampling strategies (e.g., SMOTE) were applied to address the class imbalance.
- **Model Performance:**
  - The best-performing model achieved high precision in identifying fraudulent transactions while minimizing false positives to avoid unnecessary disruptions for customers.

## Business Implications

The insights derived from this project can inform the following strategies:
1. **Real-Time Fraud Detection:** Deploying the developed machine learning model in a production environment can enable real-time monitoring and detection of fraudulent transactions.
2. **Enhanced Fraud Prevention:** By identifying patterns in fraudulent behavior, credit card companies can implement targeted prevention measures, such as stricter monitoring for transactions within high-risk time windows or specific transaction ranges.
3. **Customer Trust and Satisfaction:** Early detection and prevention of fraud can enhance customer confidence and reduce financial losses.

## Repository Structure
- `creditcard.csv`: The dataset used for analysis.
- `Credit Card Fraud - Fraud Detection & Correlation.py`: Python script detailing the exploratory analysis and key findings.
- `Credit Card Fraud - Model Building for Fraud Detection.py`: Python script focusing on building and evaluating machine learning models.

## Tools and Technologies
- **Python:** For data analysis and model building.
- **Libraries:** NumPy, pandas, scikit-learn, Matplotlib, and others for data processing and visualization.

## How to Use
1. Clone the repository to your local environment.
2. Install the required Python libraries by running:

`pip install -r requirements.txt`

3. Execute the scripts to explore the dataset and reproduce the findings or train the models.

## Acknowledgments
The dataset used in this project is provided by Kaggle and was anonymized using PCA for confidentiality.

