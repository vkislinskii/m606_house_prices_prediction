## House Price Prediction

#### Overview
This project is part of a machine learning course at the Gisma University of Applied Sciences. The goal of the project is to predict the price of a house. 

#### Dataset
The data was originally taken from the leading Australian property marketplace Domain.com.au and is [publicly available at Kaggle](https://www.kaggle.com/datasets/anthonypino/melbourne-housing-market). It includes the following features: suburb name, number of rooms, type of real estate, method of sale, agent name, sale date, price, etc.

#### Methodology
1. Data exploration
    * Exploring distributions of features 
    * Exploring feature relations
    * Exploring extreme feature values (95th percentile)
2. Data Preprocessing
    * Getting rid of rows with nonsense data
    * Handling missing values using KNN Imputer
3. Feature engineering
    * Encoding categorical values
    * Scaling numerical features (making mean equal to 0 and scaling variance to one)
    * Taking a logarithm of the label column Price to transfer its distribution from Long-tailed to be more like Normal
4. Model training
    * Implemented and compared multiple machine learning models:
      * Linear Regression
      * Elastic Net
      * Support Vector Regression (SVR)
      * K-Nearest Neighbors (KNN)
      * Decision Tree
      * Random Forest
      * Gradient Boosting
    * Evaluated model performance using MedAE (Median Absolute Error) metric

#### How to Use
* Or clone the repository
  
```sh
git clone https://github.com/vkislinskii/m606_house_prices_prediction.git
```

Install all the needed packages

   ```sh
   pip install pandas
   pip install numpy
   pip install sklearn
   pip install seaborn
   pip install scipy
   pip install matplotlib
   ```
Finally, open the project in Jupyter Notebook 

* Or open the "project_real_estate.ipynb" file in Google Colab by simply clicking the blue button on the first line of the Jupyter Notebook file

#### Results
The best-performing model on training data was Random Forest. The final result on testing data was
* Median Absolute Error (MedAE): 82333.17
* Mean Absolute Percentage Error (MAPE): 0.134
* R² Score: 0.824
