# Starbucks Capstone Challenge

## Project Overview
This project aims to analyze customer behavior on the Starbucks rewards mobile app by combining transaction, demographic, and offer data to determine which demographic groups respond best to different types of offers. The goal is to develop a model to predict whether a customer will respond to an offer and to recommend the optimal offers based on customer demographics.

## Data Description
The dataset used for this project contains the following three key files:

- **portfolio.json**: Contains offer IDs and metadata about each offer, such as the offer type (BOGO, discount, informational), difficulty (minimum spend required), reward, duration, and the channels through which the offer is sent.
- **profile.json**: Contains demographic information for each customer, including age, gender, income, and membership information.
- **transcript.json**: Contains transactional records, including when a customer received an offer, viewed it, or completed it.

## Steps to Run the Analysis

**1. Setup**
To run the analysis, make sure you have the following libraries installed:

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- You can install the required libraries using:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

**2. Data Preprocessing**
- The data is loaded and cleaned by merging the three datasets: portfolio.json, profile.json, and transcript.json.
- Missing values in the demographic data are handled, and the data is processed for modeling.

**3. Exploratory Data Analysis (EDA)**
- Basic statistics are computed for the numerical features.
- The distribution of categorical variables (e.g., gender and offer completion status) is visualized.
- Relationships between key features (e.g., age vs income vs offer completion) are explored using scatter plots and heatmaps.

**4. Model Training and Evaluation**
- A Random Forest model is trained to predict whether a customer will complete an offer based on their demographic features.
- Hyperparameter tuning is performed using GridSearchCV to improve the model performance.
- The class imbalance issue is addressed by applying class weights to the Random Forest model.

**5. Future Improvements**
- Techniques like oversampling or undersampling could be used to further balance the dataset.
- Advanced models, such as XGBoost or Gradient Boosting, could be explored for better performance.
- Additional feature engineering could be done to improve the model's predictive power.

## Results and Conclusion
After performing the analysis, we found that while the Random Forest model helped identify patterns, it still struggled with predicting offer completions due to the class imbalance in the data. By using class weights and tuning the hyperparameters, we were able to improve performance, but there is still room for improvement.

The business implications suggest that targeting specific demographics who are more likely to complete offers can optimize marketing strategies. However, more work is needed to improve predictive accuracy, and further experimentation with model tuning and feature engineering will be essential.

## How to Use
1. Download the dataset and place the portfolio.json, profile.json, and transcript.json files in the working directory.
2. Run the notebook to preprocess the data, perform EDA, and train the model.
3. The model's performance will be evaluated, and you can view the classification reports and visualizations.
4. If the model results are unsatesfatory, resample the classes to solve for the imbalance
5. Apply Hyperparameter Tuning
