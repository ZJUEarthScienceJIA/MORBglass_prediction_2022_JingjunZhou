# Structure
+ **datasets**: It contains the dataset **"dataset2.xlsx"** consisting of global MORB glasses with complete major and tracements but lack of experimentally measured water contents.
+ **models**: It contains the established machine learning model **"Established_RFR_model.pkl"**.
+ **results**: It contains the predicted results produced by the code in **"MORB_water_prediction_code.ipynb"**.
+ **"MORB_water_prediction_code.ipynb"**: The code for predicting unknown samples by using the model **"Established_RFR_model.pkl"**.

# Prediction Steps
**First**, overwrite your data in the excel **"dataset2.xlsx"** based on its original header, and make sure there are no null values in your data.  
**Second**, run the code in **"MORB_water_prediction_code.ipynb"** to make predictions and output results.  
**Third**, open the excel **"result.xlsx"** to view the results.
