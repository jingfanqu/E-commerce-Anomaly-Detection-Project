# E-commerce-Anomaly-Detection-Project
### Project Overview
In this project, I built a model for detecting anomly orders on an E-commerce company. 
### Data Sources
The primary dataset used for this project is the "abnormal_orders.txt" file, containing detailed information about each transaction on this e-commerce platform.
### Tools
- Excel - Data Cleaning and formatting
- Python - Data Analysis & Modling
### Data Cleaning/Preparation 
In the initail data preparation phase, I preformed the following tasks:
- Data Loading and inspection
- Handling missing values
- Handling duplicated values
- Handling Outliers
### Exploratory Data Analysis(EDA)
EDA involved exploring the transaction data to answer key questions, such as:
- where is the dataset original from?
- Is missing information related to the anomalies?
- What's Hiding Behind Duplicate Order_id？
- Are feature anomalies related to transaction anomalies?

### Encoding and Build Benchmarck
- Encoding - OrdinalEncoder
- Benchmarck - Random Forest

### Feature Engineering
- split train dataset and test dataset
  - This dataset is different from other dataset beacuse one order id contains samples which have the same label. In other words, under the same order id, once one sample is abnormal, others will also be abormal. Therefore, we must ensure that samples under the same order id are not split into the different set.
- Feature Exploratory and Encoding
  
### Modeling
- Random Forest
- GBDC
- XGboost
<img width="631" alt="algorithms comparison" src="https://github.com/jingfanqu/E-commerce-Anomaly-Detection-Project/assets/116844729/29b291da-a540-48ed-a07e-bd1361f20c17">

  

### Results and Findings

### Recommandations

