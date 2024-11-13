# Banana Quality Prediction Model

## Overview

The **Banana Quality Prediction Model** is a machine learning application that predicts the quality of bananas based on various features, such as size, weight, sweetness, and ripeness. This project demonstrates how to apply machine learning algorithms to real-world datasets and create a simple web-based API for predictions.

## Technologies Used

- **Python**: Programming language for implementing the machine learning model.
- **Pandas**: Data manipulation and analysis library used for data preprocessing.
- **Scikit-learn**: Machine learning library for building classification models.
- **Flask**: Web framework used to deploy the machine learning model as an API.
- **Jupyter Notebook**: Used for data exploration and model training.

## Features

- **Multiple Classification Algorithms**: Implements various models including Random Forest, KNN, and MLP to predict banana quality.
- **Data Preprocessing**: Utilizes Pandas for cleaning and preparing the dataset for modeling.
- **Model Deployment**: The trained model is deployed using Flask, allowing users to submit input and receive predictions via a simple API.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/dheeraj404/banana-quality-prediction.git
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. To train and test the model:
    - Run the `model_training.py` script, which trains the machine learning model using the dataset.

2. To use the deployed API:
    - Start the Flask server by running:
      ```bash
      python app.py
      ```

3. Send a POST request to the API with the following data format:
    ```json
    {
      "size": 250,
      "weight": 150,
      "sweetness": 7,
      "ripeness": 5
    }
    ```

4. The response will be the predicted quality of the banana.

## Example Request
```bash
curl -X POST http://127.0.0.1:5000/predict \
    -H "Content-Type: application/json" \
    -d '{"size": 250, "weight": 150, "sweetness": 7, "ripeness": 5}'
