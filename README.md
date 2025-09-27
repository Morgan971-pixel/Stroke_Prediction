# Stroke Prediction Project

This project analyzes a dataset of patient attributes to predict the likelihood of a stroke. It includes data cleaning, exploratory data analysis (EDA), and the implementation of a predictive model.

## Dataset

The dataset contains patient information, including demographic data, health metrics, and lifestyle factors. Key features include:

*   `gender`, `age`
*   `hypertension`, `heart_disease`
*   `ever_married`, `work_type`, `Residence_type`
*   `avg_glucose_level`, `bmi`
*   `smoking_status`

The target variable is `stroke` (1 if the patient had a stroke, 0 otherwise).

## Methodology

The project follows these key steps:

1.  **Data Cleaning:** The notebook handles missing values and prepares the data for analysis.
2.  **Exploratory Data Analysis (EDA):** Visualizations are used to understand the relationships between different features and the likelihood of a stroke.
3.  **Feature Engineering:** Categorical features are encoded into a numerical format suitable for machine learning models.
4.  **Model Training:** A classification model is trained on the preprocessed data to predict stroke risk.
5.  **Model Evaluation:** The model's performance is assessed using various classification metrics.

## Getting Started

### Prerequisites

*   Python 3
*   Jupyter Notebook or JupyterLab

### Installation

1.  Clone this repository:
    ```bash
    git clone <repository_url>
    ```
2.  Navigate to the project directory:
    ```bash
    cd Stroke_Prediction
    ```
3.  Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1.  Open the Jupyter notebook:
    ```bash
    jupyter notebook Stroke_Prediction.ipynb
    ```
2.  Run the cells in the notebook to follow the analysis and see the results.