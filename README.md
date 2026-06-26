# Customer Churn Prediction using ANN

This project predicts whether a bank customer is likely to churn (leave
the bank) using an Artificial Neural Network (ANN) built with TensorFlow
and deployed using Streamlit.

## Features

-   Customer churn prediction using a trained ANN model
-   Interactive web application using Streamlit
-   One-Hot Encoding for Geography
-   Label Encoding for Gender
-   Standard Scaling for numerical features
-   Real-time churn probability prediction

## Technologies Used

-   Python
-   TensorFlow / Keras
-   Scikit-Learn
-   Pandas
-   NumPy
-   Streamlit
-   Pickle

## Dataset

The model is trained on the Bank Customer Churn dataset containing the
following features:

-   Credit Score
-   Geography
-   Gender
-   Age
-   Tenure
-   Balance
-   Number of Products
-   Has Credit Card
-   Is Active Member
-   Estimated Salary

**Target Variable:**

-   Exited (0 = No Churn, 1 = Churn)

## Project Structure

``` text
ANN_PROJECT/
│
├── app.py
├── model.h5
├── onehot_encoder_geo.pkl
├── label_encoder_gender.pkl
├── scaler.pkl
├── Churn_Modelling.csv
├── requirements.txt
└── README.md
```

## Installation

Clone the repository:

``` bash
git clone https://github.com/your-username/customer-churn-ann.git
cd customer-churn-ann
```

Install dependencies:

``` bash
pip install -r requirements.txt
```

## Running the Application

Start the Streamlit app:

``` bash
streamlit run app.py
```

The application will open in your browser at:

``` text
http://localhost:8501
```

## Model Architecture

The Artificial Neural Network consists of:

-   Input Layer
-   Hidden Layer 1 (ReLU Activation)
-   Hidden Layer 2 (ReLU Activation)
-   Output Layer (Sigmoid Activation)

**Loss Function:**

``` python
binary_crossentropy
```

**Optimizer:**

``` python
adam
```

**Metric:**

``` python
accuracy
```

## Input Features

The user provides:

-   Geography
-   Gender
-   Age
-   Credit Score
-   Balance
-   Estimated Salary
-   Tenure
-   Number of Products
-   Has Credit Card
-   Is Active Member

The application preprocesses the input using:

-   One-Hot Encoding for Geography
-   Label Encoding for Gender
-   Standard Scaling

before passing it to the trained ANN model.

## Output

The model predicts:

``` text
Churn Probability: XX.XX%
```

If the probability exceeds 50%:

``` text
Customer is likely to churn.
```

Otherwise:

``` text
Customer is not likely to churn.
```

## Future Improvements

-   Deploy the application on Streamlit Cloud
-   Add model evaluation metrics to the UI
-   Implement SHAP for model explainability
-   Improve UI design
-   Add Docker support

## Author

**Prakhar Awasthi**

Machine Learning and Deep Learning Enthusiast
