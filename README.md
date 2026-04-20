# Random Forest Classification on Social Network Ads Dataset
This project implements a Random Forest Classifier to predict whether a customer will purchase a product based on their age and estimated salary. The model learns patterns in the data to classify new customers into "buy" or "not buy" categories.
# Project Overview
The objective of this project is to build a Random Forest model that can predict customer purchasing behavior using demographic features. Random Forest is praticularly useful for this type of classification problem beacuse they: 
- Handles non-linear relationships well
- Works great with mixed feature types
- Reduces overfitting
- Ignores irrelevant features
- Provides feature importance <br>

Dataset used is the "Social Network Ads" dataset, which includes information about users ages, estimated salaries and whether they purchased a product or not.
# Dataset
The dataset (Social_Network_Ads.csv) consists of the following columns:
- User ID: Unique identifier for each user
- Gender: Gender of the user (Male/Female)
- Age: Age of the user (numerical)
- EstimatedSalary: Estimated salary of the user in USD (numerical)
- Purchased: Target variable - whether the user purchased the product (1 for Yes, 0 for No)
 ### Dataset Statistics
- Total samples: 400 users
- Features: Age and Estimated Salary (primary predictors)
- Target classes: Binary classification (Purchased/Not Purchased)

# Installation
To run this project, ensure you have Python 3.7+ installed along with the following libraries:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```
### Required Libraries
- numpy: For numerical computations
- pandas: For data manipulation and analysis
- matplotlib: For data visualization
- seaborn: For statistical data visualization
- scikit-learn: For machine learning algorithms
- jupyter: For running the notebook

# Model Features
### Data Preprocessing
- Handling categorical variables (Gender encoding)
- Feature selection (Age and EstimatedSalary as primary predictors)
- Train-test split for model validation

### Random Forest Implementation
- Algorithm: Random Forest (Ensemble of Decision Trees)
- Number of Trees (n_estimators): 10
- Criterion: Entropy
- Random State: 0

### Evaluation Metrics
- Accuracy Score: Overall model performance
- Confusion Matrix: Detailed classification results
- Precision & Recall: Class-specific performance
- F1-Score: Harmonic mean of precision and recall

# Results
The Random Forest model achieves strong performance on the Social Network Ads dataset:
- Training Accuracy: ~95-98%
- Test Accuracy: ~90-93%
- Key Insights:
  - Age and salary are strong predictors of purchase behavior
  - Model captures more complex patterns compared to a single Decision Tree
  - Reduced overfitting due to ensemble averaging
  - Better generalization on unseen data

### Visualizations
- Decision boundary plots
- Feature importance analysis
- Confusion matrix heatmaps
- ROC curve analysis

# File Structure
```bash
random_forest_classification/
├── random_forest_classification.ipynb/      # Main Jupyter notebook with complete analysis
├── Social_Network_Ads.csv/                  # Dataset file
├── .ipnyb_checkpoints/                      # Jupyter checkpoint files
└── README.md                                # Project Documentation
```
# Key Learning Outcomes
This project demonstrates: 
- Data Science Pipeline: End-to-end workflow from preprocessing to model evaluation  
- Ensemble Learning: Leveraging Random Forest to improve accuracy and reduce overfitting  
- Classification Techniques: Binary classification using an ensemble of decision trees  
- Model Evaluation: Analysis using accuracy, confusion matrix, and ROC metrics  
- Data Visualization: Clear graphical representation of predictions and performance  
- Feature Importance Analysis: Understanding the impact of demographic features on outcomes

# Future Improvements
Potential enhancements for further improving the model:

- Hyperparameter Optimization: Fine-tune Random Forest parameters (n_estimators, max_depth, min_samples_split)  
- Advanced Ensemble Techniques: Experiment with Gradient Boosting and XGBoost  
- Cross-Validation: Implement k-fold validation for more reliable performance metrics  
- Feature Engineering: Introduce derived features such as age categories and salary ranges  
- Algorithm Comparison: Evaluate performance against SVM and Logistic Regression models  
