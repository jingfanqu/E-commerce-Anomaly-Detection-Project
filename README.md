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

- Fusion Model: Soft Voting
<img width="760" alt="algorithms comparison 2" src="https://github.com/jingfanqu/E-commerce-Anomaly-Detection-Project/assets/116844729/329eeccf-30a6-4ef8-b936-9b30cfcf439f">

  

### Results and Findings
- From the results, we can find that the performance of the model on the test set is quite good, although it is lower than the training set. This model is still  overfitting, but this score can be used as an "early warning" in the business.
- In the cross-validation of the train set, our model has shown good generalization ability. However, the distribution of the data in the test set may be too different from that in the train set (e.g., the new orders are not related to the past orders, or the new orders contain too much information that is not available in the past orders), which leads to unsatisfactory results in the test set. For data similar to the train set, the model can give good generalization results. At this point, we can also do the following to tune the model:
  1. Correct the final prediction using label-related rules obtained from the business, e.g., transactions with the same order number are bound to have the same labels.
  2. Continue to perform finer tuning to improve the generalization ability of the model.
  3. Utilize feature synthesis methods to form more aggregated features to improve data quality.
  4. Build more integrated models to increase the number of models in the fusion model.


