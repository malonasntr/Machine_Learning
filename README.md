# 🧩 Clustering and Classification Analysis - BMLP Sarma Elvita

## Project Description
This project is part of the final submission for the **"Belajar Machine Learning untuk Pemula (BMLP)"** program.  
The analysis consists of two main stages: **Clustering** and **Classification**, using a customer transaction dataset.

---

### Stage 1: Clustering
This stage aims to group customer data based on specific characteristics using the **K-Means Clustering** algorithm.

#### Steps Performed:
1. **Load Dataset and Exploratory Data Analysis (EDA)**
   - Display the dataset using `head()`, structure with `info()`, and summary statistics with `describe()`.
2. **Data Cleaning and Preprocessing**
   - Check for missing and duplicate values using `isnull().sum()` and `duplicated().sum()`.
   - Perform **feature scaling** using `MinMaxScaler()` or `StandardScaler()`.
   - Apply **feature encoding** to categorical columns.
   - Drop unnecessary ID-related columns such as `TransactionID`, `AccountID`, `DeviceID`, `IPAddress`, and `MerchantID`.
3. **Build the Clustering Model**
   - Determine the optimal number of clusters using the **Elbow Method** with `KElbowVisualizer`.
   - Train the model using `KMeans` from `sklearn.cluster`.
   - Save the trained model using `joblib.dump()` as `model_clustering.joblib`.
4. **Interpretation of Results**
   - Analyze the characteristics of each cluster using aggregated statistics (mean, min, max).
   - Add a new column named `Target` representing cluster labels.
   - Export the preprocessed dataset with cluster labels for the classification stage.

---

### 🔹 Stage 2: Classification
This stage aims to build a predictive model using the cluster results as the **target labels**.

#### Steps Performed:
1. **Data Preparation**
   - Split the dataset using `train_test_split()`.
2. **Build the Classification Model**
   - Use the **Decision Tree Classifier** algorithm from `sklearn.tree`.
   - Train the model and evaluate its accuracy.
   - Save the trained model using `joblib.dump()` as `decision_tree_model.h5`.

---

## 📊 Dataset
The dataset was provided in CSV format from Google Sheets:  
[Dataset Link](https://docs.google.com/spreadsheets/d/e/2PACX-1vTbg5WVW6W3c8SPNUGc3A3AL-AG32TPEQGpdzARfNICMsLFI0LQj0jporhsLCeVhkN5AoRsTkn08AYl/pub?gid=2020477971&single=true&output=csv)

It is stored locally in the `dataset/` folder as `clustering_dataset.csv` for easier access without requiring an internet connection.

---

## 🧠 Technologies Used
- Python 3.x  
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- yellowbrick  
- joblib  

---

## 📂 Folder Structure
