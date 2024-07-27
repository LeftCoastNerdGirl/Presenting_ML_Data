# Pesticide Use on Cancer Rates

This repo is forked from the single repo we used to collaborate for our project. Exploratory data on other branches was conducted, but ultimately left out in final pushes.  

Group 1  
Mo Smith  
Lori Bradshaw  
Hayley Parnell  
Elizabeth Dworkin  
Ashlee Vo  

# Project Guidelines



# Our Topic

Often we see farmers spraying pesticides and other chemicals on their fields, to protect their crops and increase their yield. We may even use similar products on our own yards and in our gardens. But do we truly think about the long term affects of these chemicals on ourselves, our food supply, and the health of the farmers and workers who apply them?  

For our final project, we chose to analyze pesticide use correlated with incidences of various types of cancer in the areas where they pesticide use is high. We categorized the data as follows:  

Types of Pesticides  
-Fungicide  
-Herbicide  
-Insecticide  

Types of Cancer  
-Leukemia  
-Lung Cancer  
-Breast Cancer  
-Prostate Cancer  
-Non-Hodgkin Lymphoma  

# Our Data Sources

The geographical scope of our research was established at the county level within the United States. We made this decision because it provided an appropriate mid-level geographic area that the effects of pesticide use could be constrained to. The data also includes historical data of pesticide use between the years 2013-2019 and pesticides broken down by category (i.e herbicide, insecticide, and fungicide). Data on cancer rates per 100k and specific cancer incidence types over an average of 5 years (2016-2020).  

The data needed to be preprocessed before any numerical and statistical evaluations could be conducted. This included removing columns that were not necessary, formatting data types, and removing null values and symbols that represented a null value.  

A table for historical pesticide use by year was compiled, with 2019 being the ending point. Additionally, another table was compiled that contained data on specifically 2019 pesticide rates since that was the most recently available data as well as the peak of pesticide use in the data. Other columns within the table included total cancer incidence rates, specific cancer incidence rates, and fungicide, herbicide, and pesticide use in kilograms.  

An outlier was identified and removed from the dataset which was Union County, Florida.  

We explored an assortment of 18 different correlations between the variables in order to find the strongest correlations between the data collected. The strongest correlation we were able to find was between total cancer incidence rates and herbicide use, granted not a strong correlation but the strongest we could work with.  

Cancer Data: https://www.statecancerprofiles.cancer.gov/incidencerates/index.php?stateFIPS=00&areatype=county&cancer=001&race=00&sex=0&age=001&type=incd&sortVariableName=rate&sortOrder=default&output=0#results  
Pesticide Data: https://www.sciencebase.gov/catalog/item/6081a924d34e8564d68661a1

# Our Initial Plan

The first machine learning model we implemented was linear regression. This is the easiest and most simple model to perform and was our first option. We supplemented this with a user GUI where users can input a value for herbicide usage, and the given output will be the predicted cancer incidence rate according to the model. Given the beginning correlation with the data, the model performs the best that it can with the following results.  

![image](https://github.com/user-attachments/assets/f3d0d3fd-9d9d-4dca-969b-f2e96a79985f)

Next, a random forest regression was created considering the same two variables. Using multiple decision trees, we trained our Random Forest model to output the mean prediction of those trees for regression results. Again, performance was limited due to existing low correlation between variables in source datasets. We were unable to lower variance and prediction error to rates of linear regression model with use of increased number of decision trees and the results are as follows.  

![image](https://github.com/user-attachments/assets/29726647-30e9-4454-a85d-e7c1084e86ea)

# Our Project Goal

We stop by our local grocery stores once a week, or every other day even to fill up on our household food necessities. However, how frequently do we consider where it really comes from and how the food we have in our homes affects those living around where they’re produced? Our goal is to evaluate if the effects of agricultural food production correlate to health conditions of nearby residents of these areas, specifically incidences of cancer.  

# Conclusions and Limitations

In attempts to optimize the data, the linear regression model appears to be better than the random forest regression model given the circumstances of the data. The linear regression model has a lower MSE than the random forest regression which implies better model performance. This could be because the random forest regression accommodates to not "overfit" the model but given the variability of the base data, overfitting may be more appropriate.  

In terms of data allocation, pesticide use rate was based on a survey so there are states and counties that are excluded from the data. For example, California conducts its own specific process of pesticide evaluation and research.  

Our study was very limited due to data availability, time, and the fact that cancer is a very long term developing illness that has many factors that come into play other than exposure to agricultural chemicals. In further studies, pesticide exposure could be an aspect to consider when evaluating the effects of cancer rates as a feature, but not a holistic correlating factor.  

# Links to Project Components Outside of This Repo

Tableau: https://public.tableau.com/views/BootcampCapstoneProject_17124418928630/InteractiveMap?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link  
User GUI Github: https://github.com/varunsly/Linear_Regression_GUI.git
