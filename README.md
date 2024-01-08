# AA1_S2151960
DESCRIPTION OF CASE STUDY:
In this case study, we examine customer engagement and purchasing patterns in an e-commerce setting using Talend Data Prep, Talend Data Integration, and SAS Enterprise Miner.

Dataset Source: https://www.kaggle.com/datasets/shriyashjagtap/e-commerce-customer-for-behavior-analysis/data

OBJECTIVES : 
- To determine whether the customer will come back to purchasing or not
- To determine the pattern trend on customer behaviour

Talend Data Prep (Data Cleaning)
- Act ad preparation stage
- The raw data excel being uploaded into Talend Data Prep
- The data cleaning start with replace the inconsistent data with the respective values CC = Credit Card. This to ensure there gonna be standardize payment method on those column.
- Invalid values are removed from the customer ID. Also, the rows from the blank customerID column are removed.
- Empty cells on Returns are also removed from the rows.
- Adjust the Date Purchased by removing the clock and remain the format as DD/MM/YYYY. This helps to avoid using exact data without a clock.
- ![image](https://github.com/NurShafiqahs2151950/AA1_S2151960/assets/102545710/8697f319-a7ba-44bd-ab4a-2b5858f99877)



Talend Data Integration
- connect two tables (ecommerce_customer_data_DIRTY Preparation_final.csv and ecommerce_customer_data_add on city Preparation_final.csv). ecommerce_customer_data_add on city Preparation_final.csv table are same as ecommerce_customer_data_DIRTY Preparation_final.csv accept the "City"
- match the both table by using Customer_ID as the primary key
- new column is added into the new column named as Churn_Category that potray the churn analysis (1= Customer won't come back, 0= Customer will come back)
- The new table is generated as (ecomm_output.csv) that have the City and churn category added.
  ![image](https://github.com/NurShafiqahs2151950/AA1_S2151960/assets/102545710/6beb8013-efee-4f9a-ab5e-7b60aa279a9a)

- ![image](https://github.com/NurShafiqahs2151950/AA1_S2151960/assets/102545710/42da5ee5-995b-433c-805a-0d6552690a0a)

![image](https://github.com/NurShafiqahs2151950/AA1_S2151960/assets/102545710/77852976-8354-4ff4-b044-897f14253117)


SAS Enterprise Miner
- The variables is custom accordingly by set The Chrun as the target value
- Library is created and the data source is generated.
- The sample dataset is set to 20% since the dataset is too large
- Use the decision tree and HP Forest to generate the analysis.
- Data partition properties: training and validation are set as equals.
- Results of Decision Tree:
![image](https://github.com/NurShafiqahs2151950/AA1_S2151960/assets/102545710/cfd84dd6-c84c-4f55-afb1-9f6c222a6adc)
- End result of Random Forest:
![image](https://github.com/NurShafiqahs2151950/AA1_S2151960/assets/102545710/a73c5e20-7355-4f0b-994a-1f8b09f54475)




