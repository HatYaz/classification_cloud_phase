# classification_cloud_phase
Classify CL phase

This script is for training a Random Forest classifier using `scikit-learn` to predict cloud phases based on the provided dataset, followed by making predictions for new data. The process includes:

1. **Loading the Training Data**:
   - The data is loaded from a CSV file (`RandomForrest.csv`) into a `pandas` DataFrame.
   - Features (all columns except the last one) and the target (last column) are separated.

2. **Splitting the Data**:
   - The data is split into training (80%) and testing (20%) sets using `train_test_split` for model evaluation.

3. **Training the Model**:
   - A `RandomForestClassifier` is trained using the training set with 100 estimators.

4. **Evaluating the Model**:
   - The model is evaluated using the test set, and the classification report (precision, recall, F1-score) is printed.

5. **Saving the Trained Model**:
   - The trained model is saved as a `.pkl` file (`cloud_phase_model.pkl`) using `joblib`.

6. **Making Predictions for New Data**:
   - A new dataset (`RandomForrest_newData.csv`) is loaded.
   - The model makes predictions on this new data.

7. **Adding Predictions to New Dataset**:
   - The predictions are added to the new dataset in a new column (`Predicted_Cloud_Phase`).

8. **Saving Predictions**:
   - The updated dataset with predictions is saved to a new CSV file (`Predicted_Cloud_Phases.csv`).

### Key Features:
- **Model Training**: Trains a Random Forest model on the provided data.
- **Model Evaluation**: Provides a classification report for model performance.
- **Predictions**: Makes predictions for new data and appends them to the dataset.
- **Model Saving**: Saves the trained model for later use.
- **Data Handling**: Handles both training data and new data in CSV format.

This tool is useful for cloud phase prediction or any other classification problem using Random Forests.
