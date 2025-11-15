# Diabetes-Prediction-Model

**Diabetes Prediction Web App**
This repository contains the source code for a simple machine learning web application that predicts the onset of diabetes based on a set of medical features.

The app is built entirely in Python using Streamlit for the web interface and Scikit-learn for the machine learning model.

**How It Works**
The script _app.py_ performs the following operations:

**Data Loading:** Loads the diabetes dataset _from diabetes.csv_ using Pandas.

**Data Preprocessing:**

Separates features (X) and the target variable (y - 'Outcome').

Applies StandardScaler to normalize the input features, which is crucial for SVM performance.

**Model Training:**

Splits the data into training and testing sets.

Initializes a Support Vector Machine (SVM) classifier with a linear kernel.

Trains the SVM model on the (scaled) training data.

**Streamlit Web Interface:**

Displays a title and an image for the app.

Creates a sidebar form with sliders for the user to input all required medical features (e.g., Pregnancies, Glucose, BMI, Age).

On "_Predict_" button submission, the app captures these inputs.

**Prediction:**

The user's input data is converted to a NumPy array, reshaped, and scaled using the same scaler that was fit on the training data.

The trained SVM model (model.predict()) is used to make a prediction on this scaled input.

A success or warning message is displayed indicating whether the person is predicted to have diabetes.

**Additional Information:**

The app also displays the model's training and testing accuracy scores.

A summary of the dataset (.describe()) and the mean values grouped by outcome are shown for context.

**Core Technologies Used:**

**Streamlit:** For building and running the interactive web app.

**Scikit-learn (sklearn):** For the SVM model, train_test_split, StandardScaler, and accuracy_score.

**Pandas:** For data loading, manipulation, and summary statistics.

**NumPy:** For numerical operations and array reshaping.
