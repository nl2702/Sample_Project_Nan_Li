# Sample_Project_Nan_Li

In this project, I built a Principal components analysis model that predicts Yield to Maturity of Chinese Funds USD Bonds using macroeconomic factors such as US-Treasury rate, exchange rate, GDP. First I acquired and validated this large dataset and manipulated them into a clean framework. Then I started with linear models but found out that the multicollinearity introduced huge variance for the coefficients. To solve this problem, I tried different methods including reducing the number of predictors, adding ridge and lasso regularization and using PCA models. I found out PCA models deliver the most consistent result both in sample and out of sample.

The Jupyter Notebook has the following contents:

  1. Load data and manipulate data \
        1.1 Melt date Column \
        1.2 Change date to to_datetime and set index 
    
  2. Calculate weighted YTM \
        2.1 Calculate daily average YTM weighted by market cap \
        2.2 Plot YTM         
        2.3 Group by YTM by different rating
        
  3. Load and manipulate Macro data \
        3.1 Change date to to_datetime and set index \
        3.2 Merge all macro data and Average YTM into one big dataframe
        
  4. Run regression \
        4.1 Perform linear regression of YTM and each factor \
        4.2 Summary statistics (level of significance) \
        4.3 Plot results \
        4.4 Conclusion for results
        
  5. Perform PCA and split into train sample and test sample \
        5.1 Find cross correlation of macro factors \
        5.2 Define insample data (prior to 2019). Out of sample data (2020) \
        5.3 Standardize all factors (x-mean)/sd \
        5.4 Perform linear regression of YTM to all factors \
        5.5 Perform PCA \
        5.6 Use result to predict both train and target data \
        5.7 Plot the results \
        5.8 Compute RMSE and R^2 \
        5.9 Run correlation between actual targets and predicted targets \
        5.10 Conclusion 
