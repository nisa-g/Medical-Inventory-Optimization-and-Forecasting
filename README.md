# Medical Inventory Optimization and Forecasting

⚙️ **Tool** : Python, MySQL <br>
💻 **Presentation Deck** : PowerPoint <br>

## 📂 **Overview**

This project showcase on a typical time series forecasting pipeline, consisting of three major phases:

1. Feature engineering and Data preparation
2. Exploratory data analysis (time-series analysis)
3. Forecasting

<br>

---

## 📂 **Task 1 - Project Scope**

### **Background Information**

Development of a pharmaceutical forecasting model aims to mitigate the potential occurrence of drug shortages. It includes collecting historical sales data and analyzing it to identify patterns and trends in drug demand. Based on the analysis of the data, we developed a forecasting model that predicts the demand for medical supplies. The project will involve collecting data on the inventory levels, usage patterns, and other relevant factors. This data will be analyzed to identify trends and patterns in 
supply and demand.

**Business Problem:** 
- Drug shortages in stocks
- Increase of bounce rate
  
**Business Objective:** 
- Minimize drug shortages.
- Maximize availability of drug, customer satisfaction, and profits.

**Data Dictionary:** 
<br>

<p align="center">
  <kbd><img width="700" src="https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/assets/139193734/f27498c1-01d8-49fd-aaf3-edba523c5aa0"></kbd> <br>
  Figure 1 — Data Dictionary
</p>
<br>

---

## 📂 **Task 2 - Data Preprocessing**

### **Background Information**

Based on the problem and objective formal definition, the data sales transactions information system are cleaned, feature engineering approach was defined, and all data are transformed to monthly time series, consisting of aggregate sales among different classes of pharmaceutical drugs in monthly time periods.

## **Data Preprocessing**

### **Objectives**
- Data Cleaning: Identify errors, inconsistencies, and missing values in the dataset.
- Data Transformation: Convert data into an appropriate format or scale for analysis or modeling.
- Feature Engineering: Create new relevant features or variables from the existing data to improve the performance of machine learning models.<br>

8 data preprocessing methods were implemented:
1. Type Casting
2. Handling missing values
3. Removing duplicates
4. One-Hot encoding
5. Data manipulation

## **Descriptive Statistics**
1. First Moment Business Decision: Measure of Central Tendency
2. Second Moment Business Decision: Measure of Dispersion
3. Third Moment Business Decision: Skewness
4. Forth Moment Business Decision: Kurtosis

**[Click here to view full documentation of data preprocessing and descriptive statistics](https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/blob/main/Full-Project-Code.ipynb)**

---

## 📂 Task 3 - Exploratory Data Analysis (EDA) 

### Background Information

After data preprocessing and descriptive statistics, our next step involves developing EDA to analyze the trends and patterns of the datasets.
 
### Objectives
- Identify and analyze patterns, and trends within the data. 

### Result
#### 1. Data Distribution
<br>

<p align="center">
  <kbd><img width="500" src="https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/assets/139193734/cfa1a625-dad2-4531-b9f3-d1ef89948134"></kbd> <br>
  Figure 5 — Distribution of Data. The Quantity data shows it is not normally distributed since the data is not falling within the straight line
</p>
<br>

#### 2. Data Transformation : Log Transformation
<br>

<p align="center">
  <kbd><img width="500" src="https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/assets/139193734/4d70dfde-9b91-46cb-8484-ba3aace076e1"></kbd> <br>
  Figure 6 — Log Transformation. After log transformation, the data is normally distributed.
</p>
<br>

#### 3. Histogram: Final Sales
<br>

<p align="center">
  <kbd><img width="500" src="https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/assets/139193734/a1125797-6bc3-4bd9-91e9-19d58f968831"></kbd> <br>
  Figure 7 — Quantity of drugs sold by month
</p>
<br>

- Max. = 39490
- Right-skewed
- Most of transactions involve lower sales amounts, but there are a few instances with significantly higher sales amounts

#### 4. Bar Plot: Quantity of drugs sold by month
<br>

<p align="center">
  <kbd><img width="500" src="https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/assets/139193734/03dff1da-b759-42f9-a4e8-c615235caa83"></kbd> <br>
  Figure 8 — Quantity of drugs sold by month. The month of March, April, July, and September has highest quantity of medicines sold and it is approximately same.
</p>
<br>

#### 5. Trend in Quantity
<br>

<p align="center">
  <kbd><img width="500" src="https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/assets/139193734/a4e64247-b27d-461a-8f79-28f6c6209177"></kbd> <br>
  Figure 9 — Quantity Trend. December has the highest quantity of medicines sold while February and June is the lowest.
</p>
<br>

#### 5. AutoEDA: D-Tale
<br>

<p align="center">
  <kbd><img width="600" src="https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/assets/139193734/c2d660c6-94d5-4cc8-84c2-4198c6c5761d"></kbd> <br>
  Figure 10 — AutoEDA using D-Tale.
</p>
<br>

---

## 📂 Task 4 - Forecasting Model

### Background Information

Based on the analysis of the data, the project will develop a forecasting model that predicts the demand for medical supplies.
 
### Objectives
-  To accurately predict future sales based on historical data, minimizing forecasting errors and improving the model's predictive performance. 

### Model Building

1. Select Models:
- 2 types of model being developed in this project which is the Random Forest Regression Model and Linear Regression Model.


2. Train and Test Models:
- Split historical data into training and testing sets.
- The training set is used to train the models, while the testing set is used to assess their performance.
- Each selected model is trained on the training set using appropriate parameters.


3. Generate Forecasts:
- Trained models is used to generate forecasts for the required period.
- For each forecasted point, the predicted value is compared with the actual value from the testing set.

  
4. Calculation of Evaluation Metrics:
- Common evaluation metrics are calculated to assess the accuracy of each model.
- Metrics for time series forecasting include:<br>
  i. Mean Squared Error (MSE)<br>
  ii. Root Mean Squared Error (RMSE)

### Result

#### 1. Holt-Winters Method
<br>

<p align="center">
  <kbd><img width="600" src="https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/assets/139193734/38332f85-6de4-48c9-a02e-edd95e25e036"></kbd> <br>
  Figure 12 — Forecast for the next 12 periods. 
</p>
<br>

- MAPE = nan
- RMSE = 5032.711977063249

#### 2. Random Forest Regression
<br>

<p align="center">
  <kbd><img width="600" src="https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/assets/139193734/b6c7942a-1a83-407c-985e-55d8736c7cd7"></kbd> <br>
  Figure 13 — Random Forest Regression Model
</p>
<br>

- MSE = 111.60992195041523

#### 3. Linear Regression
<br>

<p align="center">
  <kbd><img width="600" src="https://github.com/nisa-g/Medical-Inventory-Optimization-and-Forecasting/assets/139193734/0a98aa97-0b12-4179-a3a2-df68b6bc9817"></kbd> <br>
  Figure 14 — Linear Regression Model
</p>
<br>

- MSE = 159.57892788366377

#### Best Model

1. Considering the lower MSE value of the Random Forest Model (111.61) compared to the Linear Regression Model (159.58), the Random Forest Model appears to be the better performer in terms of prediction accuracy.
2. A lower MSE indicates that the Random Forest Model's predictions are, on average, closer to the actual values, resulting in better overall model performance.
3. The Random Forest Model is capable of capturing complex non-linear relationships in the data, which can be important when dealing with diverse and intricate patterns in pharmaceutical sales and demand.
4. It is less sensitive to outliers compared to Linear Regression, potentially resulting in more reliable predictions.

---

#### Project Challenges

1. Difficulty to predict stock with return quantity when model implanted on quantity only.
2. Restriction on patients’ privacy info with different nature of health condition leads to another drugs in present environment and it automatically leads drug shortage.
3. Limited knowledge in new drugs development.
4. Ensuring the forecasting model aligns with pharmaceutical regulations and patient privacy laws.
5. Data integration with existing inventory systems is complex and time-consuming.
7. External factors of sudden market shifts, or unexpected events (e.g., pandemics) could disrupt the accuracy of
forecasting models and inventory plans.

#### Future Scopes

**1. Enhanced Forecasting Model:**
Continuously improve and refine the pharmaceutical forecasting model by incorporating more advanced machine learning techniques, considering additional factors like seasonal trends, public health events, and external influences on medicine demand.

**2. Supply Chain Optimization:**
Collaborate with suppliers and distributors to optimize the entire supply chain. This might involve streamlining delivery routes, and reducing lead times

**3. Machine Learning for Bounce Rate Reduction:**
Utilize machine learning to predict and mitigate factors causing high bounce rates in pharmacies, offering insights into optimizing store layouts and reduce return products
