# Customer-Lifetime-Value-CLV-Prediction

## Project Overview
This project focuses on predicting **Customer Lifetime Value (CLV)** using machine learning models based on real-world **e-commerce transactional data** from the **Online Retail II** dataset. The goal is to help businesses identify high-value customers and optimize their marketing strategies for better ROI.

## Dataset
The dataset used is the **Online Retail II Dataset** from the UCI Machine Learning Repository. It includes transactional data from 2009 to 2011 for a UK-based online retail company.

### Dataset Files:
- `Year 2009-2010.csv`
- `Year 2010-2011.csv`

### Key Columns:
- `InvoiceNo`: Unique invoice number for transactions
- `StockCode`: Product identifier
- `Description`: Product name
- `Quantity`: Number of units purchased
- `InvoiceDate`: Date of transaction
- `UnitPrice`: Price per unit
- `CustomerID`: Unique identifier for each customer
- `Country`: Customer location

## Project Structure
```
CLV_Prediction/
│── data/
│   ├── Year 2009-2010.csv
│   ├── Year 2010-2011.csv
│── src/
│   ├── preprocess.py     # Data cleaning and feature engineering
│   ├── train_model.py    # Model training (Random Forest, XGBoost)
│   ├── predict.py        # Predict CLV for new customers
│── notebooks/
│   ├── EDA.ipynb         # Exploratory Data Analysis (EDA)
│── app.py               # Deployment script (Flask API)
│── requirements.txt     # Python dependencies
│── README.md            # Project documentation
```

## Data Preprocessing
Run the following script to clean and transform the dataset:
```sh
python src/preprocess.py
```
This script will:
- Handle missing values (especially `CustomerID`)
- Convert `InvoiceDate` to datetime format
- Create new features (`TotalPrice`, `Recency`, `Frequency`, `Monetary`)

## Model Training
Train the machine learning models (Random Forest, XGBoost) using:
```sh
python src/train_model.py
```
This script will:
- Train models on customer features
- Evaluate model performance (MAE, R² Score)
- Save the trained model

## Predict CLV
Run predictions for new customers:
```sh
python src/predict.py --input new_customers.csv
```

## API Deployment
Deploy the trained model as a Flask API:
```sh
python app.py
```
Access the API at `http://127.0.0.1:5000/predict`.

## Skills & Technologies Used
- **Python** (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)
- **Machine Learning** (Random Forest, XGBoost)
- **Feature Engineering** (RFM Analysis, Data Cleaning, Transformation)
- **Data Visualization** (Matplotlib, Seaborn)
- **Flask API** (Deployment for real-time CLV prediction)



