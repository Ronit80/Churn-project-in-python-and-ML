### Part A: EDA & Machine Learning Algorithm

#### Step 1: Names and IDs of all team members
- **Team Member 1:** Ronit [Insert ID]

---

#### Step 2: The Problem

- **Objective:** 
  - Predict whether a customer will churn (the loss of clients or customers).
  
- **Data Available (Input):**
  - Customer demographics
  - Account information
  - Subscription details
  - Usage patterns

- **Motivation and Applications:**
  - Reduce customer churn rates.
  - Improve customer retention strategies.
  - Enhance customer satisfaction and service offerings.

---

#### Step 3: Data Description

- **Dataset:**
  - Total examples: 7,043 customers
  - Training set: 80% (5,634 customers)
  - Testing set: 20% (1,409 customers)
  
- **Features:**
  - Total features: 21
  
- **Label Distribution:**
  - Churned: 1,869 (26.5%)
  - Not Churned: 5,174 (73.5%)
  
- **Missing Values:**
  - Yes, in the 'TotalCharges' column

- **Sample Graphs:**
  - Distribution of churn by gender
  - Monthly charges distribution
  - Tenure distribution
  - Churn rate by contract type
  - Churn rate by payment method
  - Churn rate by internet service type

---

#### Step 4: Data Engineering

- **Removed Features:**
  - CustomerID (irrelevant for modeling)

- **Added Features:**
  - Tenure groups

- **Handling Missing Values:**
  - Replaced missing 'TotalCharges' with calculated values using tenure and monthly charges.

---

#### Step 5: Machine Learning Algorithms

- **K-Nearest Neighbors (KNN):**
  - Tested with k=3, k=5, k=7

- **Decision Tree:**
  - Tested with max depth = 5, 10, 15

- **Random Forest:**
  - Tested with max depth = 5, 10, 15 and 100 estimators

---

#### Step 6: Algorithms Introspection

- **Decision Trees:**
  - Visualizations of the decision trees for each max depth

- **Random Forest:**
  - Feature importance plot

---

### Part B: MongoDB Project

#### Step 1: Create Database and Collection

- **Database Name:** BDA
- **Collection Name:** Customers

#### Step 2: Import Churn Data

- **Using MongoDB Compass:**
  - Imported churn.json into the Customers collection

#### Step 3: PyMongo and MongoDB Queries

- **Connect to MongoDB:**
  - Established connection using PyMongo

- **MQL Queries:**
  - a. Return documents with all fields
  - b. Return all fields except "_id"

#### Step 4: Data Import to Pandas DataFrame

- **Import Collection to DataFrame:**
  - Used MQL query to fetch data and import it into a Pandas DataFrame

#### Step 5: Data Cleaning

- **Using MongoDB Compass:**
  - Cleaned and adjusted problematic columns with non-scalar values

#### Step 6: Data Preparation for ML

- **Prep Data:**
  - Applied the data preparation steps from Part A

#### Step 7: Add Predicted Churn Column

- **Using Best Model:**
  - Added the predicted churn column to the DataFrame

#### Step 8: Export Final DataFrame

- **Export to CSV:**
  - Ensured the format matches the original churn.csv file

---

### Part C: Spark Project

#### Step 1: Create Notebook in Google Colab

- **Import Spark Libraries:**
  - Established connection between Colab and Google Drive

#### Step 2: Import Data

- **Import churn_location_and_rating.csv:**
  - Loaded data into a Spark DataFrame

#### Step 3: Data Cleaning and Preparation

- **Handle Null Values:**
  - Applied appropriate handling based on data type and whether it is a measure or attribute

- **Remove Duplicates:**
  - Removed duplicate rows

- **Split Data:**
  - Split data into CustomerID, Country, State, City, Rating columns

---

### Part D: Tableau Project

#### Step 1: Connect with Tableau Prep

- **Datasets:**
  - Connected to churn.csv and churn_location_and_rating.csv

#### Step 2: Data Mashups and Transformation

- **Create Star Schema Model:**
  - Created 4 Hyper Files: Dim_Customers, Dim_Services, Dim_Contract, and Fact

#### Step 3: Data Cleaning

- **Create SK:**
  - Created surrogate keys for dimensions

- **Handle Null Values:**
  - Applied appropriate handling based on data type and context

- **Check CustomerIDs:**
  - Ensured all CustomerIDs in churn.csv exist in churn_location_and_rating.csv

#### Step 4: Tableau Desktop Analysis

- **Tasks:**
  - Connecting to Data Source
  - Creating Reports and Dashboards
  - Filtering and Sorting
  - Creating and Editing Calculated Fields
  - Aggregations, String Functions, Date Calculations, Table Calculations

---

### Administrations

#### Project Team

- **Notebook:**
  - Provided Jupyter Notebook with all steps implemented

- **CSV:**
  - Exported final churn.csv

---

Please provide the dataset churn.csv and any additional files necessary to start the project.
