# MORB glass water predictor

This project provides a Random Forest Regression model to predict water contents of mid-ocean ridge basalt (MORB) glasses based on their major and trace elements.

## Main directory
+ **model_training_code** : this directory contains the codes to train the model with designated hyperparameters and the dataset **"dataset1.xlsx"** used.
+ **MORB_water_prediction_code** : this directory contains the codes to utilize the model **"Established_RFR_model.pkl"** to predict water contents of unknown samples.

## Code distribution and usage
The code and datasets used for training the Random Forest Regression model and predicting unknown samples by the trained model are available on Github as a python script at https://github.com/ZJUEarthScienceJIA/MORBglass_prediction_2022_JingjunZhou. In this section, we will describe how to use each script. The script was written in the Jupyter Notebook, a web-based application for interactive computing that uses the python language. We recommend the users to use the Jupyter Notebook to run the code. Users who are not familiar with python are recommended to solve the installation of the Jupyter Notebook by installing the Anaconda, which automatically installs the Jupyter Notebook and other tools, as well as many useful packages with python (https://www.anaconda.com). 
### Code distribution
The code is divided into two files. The first file, named 'model_training_code', is used to train the model. It contains the code for training the model, 'model_training_code_RandomForest.ipynb'. Additionally, there are three secondary directories: 'datasets', 'images', and 'models'. These directories are used to store the dataset used for training the model, any generated pictures, and the established models, respectively.
The second file, named 'MORB_water_prediction_code', is used to predict unknown samples using the trained model. It contains the code for predicting unknown samples, 'MORB_water_prediction_code.ipynb'. Similar to the first file, there are three secondary directories in the second file: 'datasets', 'models', and 'results'. These directories are used to store the dataset for prediction, the pre-established models, and the predicted results, respectively.
### Model training
This script is used to train and save the model, as well as generating a binary graph. 
1)	Starting
First, users are supposed to open the Jupyter Notebook in the same directory as the downloaded code file. This procedure makes the following reading and saving processes available. Then, start the code ‘model_training_code_RandomForest.ipynb’ in the Jupyter Notebook. 
2)	Previous settings
This section contains 3 cells. The necessary packages used later are imported. The routes to import the dataset, save pictures and export trained models are defined. And some functions used to train models, obtain model’s scores and draw pictures are defined. These functions are used later to simplify the processes of training models.
3)	Data reading and preprocessing
This section contains 3 cells. The filtered dataset ‘dataset1.xlsx’, consisting of compiled MORB glasses with measured water contents, is imported from the secondary directory ‘datasets’. Then samples are labelled following the rules introduced in the section 2.2 of the main text. Next, the feature element compositions (major elements SiO2, TiO2, Al2O3, FeOT, MgO, CaO, Na2O, K2O, and trace elements Rb, Sr, Nb, Ba, La, Ce, Nd, Sm, Eu, Yb, Hf, Pb, Th, U) are extracted to ‘X_all’ and the target element compositions (H2O) are extracted to ‘y_all’, to prepare for the later model training.
4)	Model training
This section contains 3 cells. The dataset is divided into a training set (n=1,320), used to train the model, and a test set (n=147), not involved in model training and used to evaluate the model. The Random Forest Regression model is trained by the training set and then exported to the secondary directory ‘models’ with a file extension of ‘.pkl’. The binary diagram is drawn and saved in the secondary directory ‘images’ simultaneously.
### Sample prediction
This script is used to predict the water contents of unknown samples by pre-established models and export the predicted results.
1)	Starting
Similar to the section of ‘Model training’, users are recommended to start the code ‘MORB_water_prediction_code.ipynb’ in the Jupyter Notebook. 
2)	Previous settings
This section contains 2 cells. The packages used later are imported. The routes to read the dataset, import models and export predicted results are defined.
3)	Data reading and preprocessing
This section contains 2 cells. The dataset ‘dataset2.xlsx’, consisting of MORB glasses with complete major and trace elements but without determined water contents, is imported from the secondary directory ‘datasets’. The needed element compositions are extracted to ‘X_all’.
4)	Water predicting
This section contains 4 cells. The pre-established model ‘Established_RFR_model.pkl’ is imported from the secondary directory ‘models’. The water contents of samples are predicted by the model and inserted into the dataset with a column name of ‘H2O_P’. The predicted results are exported to file ‘result.xlsx’ in the secondary directory ‘results’. 
It is noteworthy that if users have trained a new model in the first file and want to predict samples by the new model, a transfer or copy of the new model from the secondary directory ‘models’ in the first file to the secondary directory ‘models’ in the second file is recommended, and the newly-trained model names in the code and in the secondary directory should be consistent to make sure the code can import the model successfully.

## Contributors
+ Jingjun Zhou  
Email : jingjunzhou1999@zju.edu.cn
