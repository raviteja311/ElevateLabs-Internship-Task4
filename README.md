# Task 4: Breast Cancer Prediction with Logistic Regression

This notebook (`Task4.ipynb`) shows how to use Logistic Regression to predict whether a breast mass is malignant (M) or benign (B) based on cell measurements.

## Dataset

*   Uses the **Wisconsin Breast Cancer Dataset** (`data.csv`).
*   Goal: Predict the `diagnosis` (M or B).

## Steps Taken

1.  **Load Data:** Reads the data from `data.csv`.
2.  **Prepare Data:**
    *   Cleans up the data (removes unnecessary columns).
    *   Checks the data for issues (like missing values).
    *   Splits data into training and testing sets.
    *   Scales the features (makes sure values are in a similar range).
3.  **Train Model:** Trains a Logistic Regression model on the training data.
4.  **Evaluate Model:**
    *   Tests the model on the unseen test data.
    *   Checks how well the model performs using:
        *   Confusion Matrix
        *   Precision (How many predicted positives are actually positive?)
        *   Recall (How many actual positives did the model find?)
        *   ROC-AUC Score (Overall model performance)
5.  **Tune Threshold:** Finds the best probability cutoff (threshold) to improve the F1-score (a balance of precision and recall).
6.  **Explain Concepts:** Briefly explains the Sigmoid function (used in logistic regression) and why adjusting the threshold matters.

## Key Ideas

*   **Sigmoid Function:** Turns model output into a probability (0 to 1).
*   **Threshold Tuning:** Changing the probability cutoff (usually 0.5) can make the model better at finding positives (higher recall) or better at being right when it predicts positive (higher precision).

## Required Libraries

*   `numpy`
*   `pandas`
*   `matplotlib`
*   `seaborn`
*   `scikit-learn`

Install them using: `pip install numpy pandas matplotlib seaborn scikit-learn`

## How to Run

1.  Make sure you have Python and the libraries above.
2.  Have `data.csv` in the same folder as `Task4.ipynb`.
3.  Open and run the notebook using Jupyter Notebook or JupyterLab.

## Results

*   **Precision:** 0.975 (Model is quite accurate when predicting Malignant)
*   **Recall:** 0.929 (Model finds most of the Malignant cases)
*   **ROC-AUC:** 0.996 (Model is very good at distinguishing between classes)
*   **Best F1-Score:** 0.976 (Achieved by adjusting the threshold to 0.25)
