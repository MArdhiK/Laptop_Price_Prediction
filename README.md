# Laptop Price Prediction
First of all, I get this data from https://laptopmedia.com/ , by scraping with the plugin called [Web Scraper](https://chrome.google.com/webstore/detail/web-scraper-free-web-scra/jnhgnonknehpejjnehehllkliplmbmhn?hl=en).
   
Of course the data I get is dirty/raw so I need to clean, extract, and used some feature engineering to make it easier to make the model   
     
I used some method to get the best model, as the base model of course I use Linear Regression, and then for the comparison I use Decision Tree Regressor, Random Forest Regressor, XGB, and Light GBM, and I use Randomized Search CV in all of them, of course except the Linear Regression.    
Surprisingly the Standard XGB model get the highest adjusted Rsquared with score 75,9%

### Here's some of the glimpse on my notebook

##### This is the raw data, as you can see the data have 7109 rows and 11 columns and its so messy
<img src=images/1.raw.png width=700>

##### This is after extract the information from the data, and drop little duplicated value, and looks nice to see :D
<img src=images/2.halfclean.png width=700>

##### This is the final data, after drop some columns that have many distinct values, and drop duplicated data and limit the outlier
<img src=images/3.clean.png width=700>

##### This is the metrics of the base model 
<img src=images/4.performacelr.png width=700>

#### This is the metrics of the XGB model
<img src=images/5.performacexgb.png width=700>
