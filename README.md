# Capstone-Project-2---Final-Model---Supply-Chain-Analytics

Problem Statement

The instant noodles company is experiencing significant inventory cost losses due to inadequate supply management across its nationwide network of warehouses. The primary objective of this project is to develop a predictive model using historical data to determine the optimal weight of the product to be delivered to each warehouse on every occasion. By accurately forecasting product delivery amounts, the company aims to minimize costs associated with overstocking and understocking, thus maximizing overall supply chain efficiency.

About the Dataset

The dataset used for this project, titled Data-1.csv, comprises 250,000 rows and 24 attributes, capturing various aspects of warehouse operations and environmental factors. The data is structured as follows:

Ware_house_ID: Unique identifier for each warehouse.
WH_Manager_ID: Unique identifier for each warehouse manager.
Location_type: Categorical variable indicating the type of location (urban, rural, etc.).
WH_capacity_size: Numerical value representing the storage capacity of the warehouse.
zone: Categorical variable indicating the zone in which the warehouse is located.
WH_regional_zone: Categorical variable indicating the regional zone of the warehouse.
num_refill_req_l3m: Number of refill requests in the last 3 months.
transport_issue_l1y: Number of transport issues in the last year.
Competitor_in_mkt: Indicator if there is a competitor in the market.
retail_shop_num: Number of retail shops associated with the warehouse.
wh_owner_type: Categorical variable indicating the ownership type of the warehouse.
distributor_num: Number of distributors associated with the warehouse.
flood_impacted: Indicator if the warehouse has been impacted by floods.
flood_proof: Indicator if the warehouse is flood-proof.
electric_supply: Indicator of the stability of electric supply.
dist_from_hub: Distance of the warehouse from the central hub.
workers_num: Number of workers in the warehouse.
wh_est_year: Year the warehouse was established.
storage_issue_reported_l3m: Number of storage issues reported in the last 3 months.
temp_reg_mach: Indicator if the warehouse has temperature regulation machinery.
approved_wh_govt_certificate: Indicator if the warehouse has government certification.
wh_breakdown_l3m: Number of warehouse breakdowns in the last 3 months.
govt_check_l3m: Number of government checks in the last 3 months.
product_wg_ton: Target variable representing the weight of the product (in tons) to be delivered to the warehouse.

Approach
The methodology for this project involved the following steps:

Data Preprocessing:

Handling missing values by imputing median for numerical features and mode for categorical features.
Encoding categorical variables using Label Encoding.
Scaling numerical features using StandardScaler.

Exploratory Data Analysis (EDA):

Conducting univariate analysis to understand the distribution of individual features.
Performing bivariate analysis to explore relationships between features and the target variable.

Feature Selection:

Using Recursive Feature Elimination (RFE) with a DecisionTreeRegressor to select the top 10 features that have the most significant impact on predicting the target variable.

Model Creation and Hyperparameter Tuning:

Splitting the data into training and testing sets.
Implementing a Decision Tree Regressor and manually tuning hyperparameters using cross-validation to find the best parameters.

Model Analysis
The optimal model was determined through manual cross-validation, with the best parameters being a maximum depth of 10 and a minimum samples split of 10. The model evaluation results are as follows:

Best Cross-Validation Score: 0.0071
Mean Squared Error on Test Data: 0.0062
These metrics indicate that the model performs well in predicting the optimal weight of the product to be delivered, with a low mean squared error suggesting high accuracy.

Output Summary

The final predictive model successfully addresses the challenge of optimizing product delivery weights to each warehouse. With the best parameters identified and a robust evaluation process, the model demonstrates the ability to minimize inventory costs by accurately forecasting delivery amounts. This outcome will enable the instant noodles company to enhance its supply chain efficiency, reduce inventory cost losses, and ensure adequate supply management across its warehouse network.
