# IEEE Fraud Detection

This project aims to detect fraudulent online transactions using the IEEE-CIS Fraud Detection dataset. The notebook demonstrates a machine learning workflow using the AutoGluon library, including data loading, merging, preprocessing, model training, prediction, and submission file generation.

## Dataset

The dataset used in this notebook is the IEEE-CIS Fraud Detection dataset, available on Kaggle. It contains a large number of transaction and identity features.

*   `train_transaction.csv`: Transactional data.
*   `train_identity.csv`: Identity data.
*   `test_transaction.csv`: Transactional data for testing.
*   `test_identity.csv`: Identity data for testing.
*   `sample_submission.csv`: A sample submission file in the correct format.

**Note:** Due to the large size of the dataset, the notebook includes steps to sample the training and testing data to manage memory usage and reduce training time.

## Notebook Steps

1.  **Install Libraries**: Installs the necessary libraries, primarily `autogluon`.
2.  **Load Data**: Loads the training transaction and identity data into pandas DataFrames.
3.  **Merge Training Data**: Merges the training transaction and identity DataFrames.
4.  **Sample Training Data**: Reduces the size of the training data by sampling.
5.  **Train Model**: Trains a machine learning model using AutoGluon's `TabularPredictor` on the sampled training data.
6.  **Load and Merge Test Data**: Loads and merges the testing transaction and identity data.
7.  **Sample Test Data**: Reduces the size of the test data by sampling.
8.  **Make Predictions**: Uses the trained model to predict the probability of fraud on the sampled test data.
9.  **Generate Submission File**: Creates a submission file in the specified format with the predicted fraud probabilities.

## How to Run the Notebook

1.  Clone this repository to your local machine or open it in Google Colab.
2.  Download the IEEE-CIS Fraud Detection dataset from Kaggle and place the CSV files in a directory named `IEEEfraud` within the notebook's environment.
3.  Run the cells sequentially.

## Dependencies

*   `pandas`
*   `numpy`
*   `autogluon`

These dependencies are installed in the first cell of the notebook.

## Results

The notebook trains a TabularPredictor model and generates a `my_submission.csv` file containing the predicted fraud probabilities for the test set. The performance of the trained model is summarized after the training process.
