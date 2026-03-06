# Hotel Booking Cancellation Prediction

Predicting hotel reservation cancellations using machine learning and behavioral booking data.

This project analyzes historical reservation records to identify patterns associated with cancellations and builds predictive models that estimate the probability a booking will cancel.

The goal is to help hotel managers improve **revenue forecasting, booking management, and operational planning**.

---

## Project Overview

Hotels frequently experience reservation cancellations, which can create uncertainty in occupancy planning and revenue forecasting. In the dataset used for this project, **approximately one-third of reservations were canceled**, creating significant operational challenges.

This project uses historical booking data to:

- identify patterns associated with cancellations
- build predictive models estimating cancellation probability
- generate insights that could help hotels proactively manage reservations

By identifying high-risk reservations early, hotels could implement strategies such as reminder notifications, flexible booking policies, or controlled overbooking.

---

## Dataset

The dataset contains **36,238 hotel reservation records** with features describing customer behavior and booking characteristics.

Examples of variables include:

- booking lead time
- room type
- meal plan
- average room price
- number of special requests
- previous customer behavior
- market segment

Target variable:

**booking_status**
0 = booking not canceled
1 = booking canceled


Cancellation distribution:

- 67.2% bookings completed
- 32.8% bookings canceled

---

## Methodology

### Data Preparation

Data preprocessing steps included:

- removing non-informative identifiers
- converting the target variable to binary format
- handling missing values
- one-hot encoding categorical variables
- standardizing numerical variables

The dataset was split into:
80% training data
20% validation data


The split preserved the original class distribution to ensure realistic evaluation.

---

### Modeling Approach

Two feedforward neural network models were developed and compared.

**Model A**

- Two hidden layers
- 64 and 32 neurons
- ReLU activation
- Adam optimizer

**Model B**

- Smaller architecture
- 32 and 16 neurons
- Higher regularization

Early stopping and adaptive learning rates were used to reduce overfitting.

---

## Results

Model performance was evaluated using several metrics including:

- Accuracy
- Precision
- Recall
- F1-score
- Area Under the ROC Curve (AUC)

**Best performing model: Model A**

| Metric | Value |
|------|------|
| Validation AUC | **0.921** |
| Accuracy | 0.86 |
| Precision | 0.84 |
| Recall | 0.72 |
| F1 Score | 0.77 |

These results indicate strong predictive performance in identifying likely cancellations.

---

## Key Insights

Several important patterns emerged from the analysis.

### Lead Time

Reservations made far in advance were significantly more likely to cancel.

### Customer Engagement

Bookings with more **special requests** were less likely to cancel, suggesting higher commitment.

### Repeat Customers

Returning guests had much lower cancellation rates compared to first-time customers.

### Pricing

Higher-priced bookings without additional engagement signals were more likely to cancel.

---

## Potential Business Applications

The predictive model could be integrated into hotel booking systems to support:

**Cancellation risk scoring**

Each new reservation could receive a probability of cancellation.

**Customer engagement strategies**

High-risk bookings could trigger:

- reminder emails
- confirmation requests
- partial prepayment options

**Overbooking optimization**

Hotels could estimate expected cancellations and safely overbook rooms when appropriate.

---

## Tools Used

Python  
pandas  
NumPy  
TensorFlow / Keras  
scikit-learn  
Jupyter Notebook  

---

## Author

Richard Wilders

M.S. Data Science (Expected 2026)  
Former U.S. Marine Corps Signals Intelligence Analyst

LinkedIn  
https://linkedin.com/in/richard-wilders-915395106



