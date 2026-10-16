hishing URL Detection Using Decision Tree
Project Overview
This project uses a Decision Tree Classifier to identify phishing URLs and distinguish them from legitimate URLs. The notebook uses numeric features from the PhiUSIIL Phishing URL Dataset to train and evaluate a machine learning model.
Objectives
- Load and inspect the phishing URL dataset.
- Prepare the target labels and numeric input features.
- Split the data into training and testing sets.
- Train a Decision Tree classification model.
- Visualize the decision tree and confusion matrix.
- Evaluate the model using classification metrics.
Dataset
- Dataset: PhiUSIIL Phishing URL Dataset
- Target column: label
- Original labels: 0 = phishing, 1 = legitimate
- Labels used by the model: 1 = phishing, 0 = legitimate
Update the CSV file path in the notebook to match the location where you store the dataset.
Technologies Used
- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook / Google Colab
Workflow
1. Import libraries for data handling, visualization, model training, and evaluation.
2. Load the dataset from a CSV file and inspect its shape and columns.
3. Check data quality by counting missing values and reviewing target-label counts.
4. Prepare the target variable by converting the original labels into phishing (1) and legitimate (0) classes.
5. Select numeric features and remove the label column from the input features.
6. Handle invalid and missing feature values by replacing infinite values with missing values and filling missing values with each column's median.
7. Split the dataset into 80% training data and 20% testing data, using stratification to preserve class proportions.
8. Train the Decision Tree Classifier with max_depth=5, class_weight='balanced', and random_state=42.
9. Visualize the trained tree to inspect the feature-based decision rules.
10. Generate predictions for the test set.
11. Evaluate performance with a confusion matrix, accuracy, precision, recall, F1-score, and specificity.
Model Configuration
- Algorithm: Decision Tree Classifier
- Maximum tree depth: 5
- Class weighting: Balanced
- Random state: 42
- Test size: 20%
Evaluation Metrics
- Accuracy: Overall proportion of correct predictions.
- Precision: Proportion of predicted phishing cases that are actually phishing.
- Recall: Proportion of actual phishing cases correctly detected.
- F1-score: Harmonic mean of precision and recall.
- Specificity: Proportion of legitimate URLs correctly identified.
The notebook prints the metric values when it is run. Actual performance values are not included here because they depend on the dataset and execution results.
How to Run
1. Download or obtain the PhiUSIIL Phishing URL Dataset CSV file.
2. Open the notebook in Google Colab or Jupyter Notebook.
3. Place the CSV file in the expected location or update the path in the pd.read_csv() statement.
4. Run the notebook cells in order.
5. Review the decision-tree plot, predictions, confusion matrix, and evaluation metrics.
Output
The notebook produces:
- Dataset shape, column names, missing-value count, and label counts.
- Training and testing record counts.
- A visualization of the trained decision tree.
- Actual and predicted labels for sample test records.
- A confusion matrix.
- Accuracy, precision, recall, F1-score, and specificity.
Conclusion
This project demonstrates a machine learning workflow for phishing URL detection using a Decision Tree Classifier. The model is trained on numeric dataset features and evaluated on a held-out test set. Its effectiveness should be judged using the reported metrics and, for real-world use, additional validation on unseen data.
