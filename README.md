# Group 10

Student 1: Amruth Nag

Student 2: Akshdeep Singh Rajawat

Student 3: Naveen kumar kannegundla

Student 4: Vasu Tiwari
 
## Introduction:

Covid-19 has affected every sector across the globe. In this project, we are focusing on how
Covid-19 has affected the hospitality industry.  Our goal is to analyze the effect on the
hospitality industry by processing, exploring, and performing in-depth analyses
of our datasets.
We are using The New York Times dataset for covid 19 and the Airbnb dataset for hotel listings. This project falls into the category of pandemic and hospitality industry.  

Instead of using a single city/county, we have used 7 different counties/cities (Austin, Broward, Cook, Denver, Los Angeles, NewYorkCity, Suffolk) from states like( Texas, Florida, Illinois, Colorado, California, New York, Massachusetts) respectively to understand the trends across the USA.
 
## Research questions:

1. What is the correlation between covid-19 cases and hotel bookings in California? What does the comparison between the trends look like for the post and pre-pandemic data?
2. Has the number of covid-19 cases affected the pricing of the listings in New york? If yes, what is the correlation?
3. Are there any anomalies in the observed trends in California? If yes, what are the factors that caused this?
 

## Data Source and Preparing

### Covid dataset 

We have taken open source Covid dataset from The New York Times - https://github.com/nytimes/covid-19-data

The dataset is the past 1-year Covid dataset which is county-based.

Columns in dataset
‘date' – Date of record  
'county' – County name  
'state' – State in which county is located  
'fips' - numbers that uniquely identify geographic areas  
'cases' – The total number of cases of Covid-19.  
'deaths’ - The total number of deaths from Covid-19.  

**Dealing with imbalance –**  

We have used a nullity matrix to select the most complete columns.  
We are using the date county and cases columns for our prediction. As the Covid data was complete and without any flaw we didn’t use any imputation.  
We have filtered the data based on county and have used data from Austin, Broward, Cook, Denver, Los Angeles, New York City, Suffolk) From states like ( Texas, Florida, Illinois, Colorado, California, New York, Massachusetts ).  

### Airbnb Dataset-

We are taking the Airbnb hotel review dataset - http://insideairbnb.com/get-the-data.html  
based on the listing_id and date.  

Columns in dataset  
listing_id – unique id of any hotel.  
date – date of the review.  

**Dealing with imbalance-**
Based on our requirements we have taken Airbnb data from the below counties.  
Austin, Broward, Cook, Denver, Los Angeles, New York City, Suffolk  
And have taken the sales count from 2017-01-01 to 2020-01-01 for pre-pandemic and after 2020-03-01 to visualize the after-pandemic situation.  
We are changing the column type of date to Datetime

## Visualizations :

**Austin Sales vs Cases:**

![image](https://github.com/amruthsrepo/ITCS-6162_KDD_project/blob/main/Images/Austin_sales_vs_cases.png)

From April 2020 sales are decreasing and Covid19 cases are increasing as this is the first wave of Covid19 and most of the world is in lockdown.
The second wave is completed somewhere in October and the sales are increasing at a faster pace. After that in January 2021 cases started increasing due to the holiday season and new variants of the virus started infecting more people and sales are decreasing from January.
From May 2021 till July, most of the people who are already vaccinated and which initiated the sales raise. After July 2021 still, new varients from other countries are spreading so cases are increasing, and as there are fewer lockdown norms sales also increasing.





**Broward Sales vs Cases:**

![image](https://github.com/amruthsrepo/ITCS-6162_KDD_project/blob/main/Images/Broward_sales_vs_cases.png)


From April 2020 sales are decreasing and Covid19 cases are increasing as this is the first wave of Covid19 and most of the world is in lockdown.
From June 2020  covid cases are in decreasing trend and sales are in increasing trend and once the vaccine is available to people we see a drastic fall in cases in Broward.
After July 2021 still, new variants from other countries are spreading so cases are increasing, and as there are fewer lockdown norms sales also increasing.


**Cook County sales vs Cases:**

![image](https://github.com/amruthsrepo/ITCS-6162_KDD_project/blob/main/Images/Cook_sales_vs_cases.png)

From April 2020 sales are decreasing and Covid19 cases are increasing as this is the first wave of Covid19 and most of the world is in lockdown.
Covid19 cases are in increasing trend till the second wave was completed after the second wave completed from November cases are decreasing and sales are increasing. Once roll out of vaccine drastic decreasing on covid cases.
After July 2021 still, new variants from other countries are spreading so cases are increasing, and as there are fewer lockdown norms sales also increasing.

**Denver sales vs cases:**

![image](https://github.com/amruthsrepo/ITCS-6162_KDD_project/blob/main/Images/Denver_sales_vs_cases.png)

From April 2020 sales are decreasing and Covid19 cases are increasing as this is the first wave of Covid19 and most of the world is in lockdown.
the decrease in the Covid19 trend after Nov 2020 is due to more restrictions in Colorado city and its counties which make the fall of Covid19 cases.
After July 2021 still, new variants from other countries are spreading so cases are increasing, and as there are fewer lockdown norms sales also increasing.

**New York  sales vs Cases:**

![image](https://github.com/amruthsrepo/ITCS-6162_KDD_project/blob/main/Images/NewYorkCity_sales_vs_cases.png)


From April 2020 sales are decreasing and Covid19 cases are increasing as this is the first wave of Covid19 and most of the world is in lockdown. From April 2020 sales are increasing as cases are un decreasing trend. After September cases started increasing where sales started decreasing due to schools reopening and election campaigns in the Newyork city.
After July 2021 still, new varients from other countries are spreading so cases are increasing, and as there are fewer lockdown norms sales also increasing.


**Los Angles sales vs Cases:**

![image](https://github.com/amruthsrepo/ITCS-6162_KDD_project/blob/main/Images/LosAngeles_sales_vs_cases.png)


The cases are in constant increase trend till whole year 202 due to elections the first wave, second wave and sales are on constant decrease trend. Once the vaccine is rolled out cases are stabilized and sales are increased. After July 2021 still, new varients from other countries are spreading so cases are increasing, and as there are fewer lockdown norms sales also increasing


**Sufflock sales vs cases:**

![image](https://github.com/amruthsrepo/ITCS-6162_KDD_project/blob/main/Images/Suffolk_sales_vs_cases.png)


The cases increased in the first wave and for some time after the first wave cases decreased, once the second wave started and due to election campaign cases increased. Vaccine rollout helped the sales to some extend After July 2021 still new varients from other countries are spreading so cases are increasing and as there are fewer lockdown norms sales also increasing.

## Conclusion

We are combining the Airbnb and Covid datasets into one dataset and visualizing the sales based on the number of cases. When combining the data frames we are dropping null valued data.
We have used Evaluation metrics to find the accuracy of the matrix. An evaluation metric quantifies the performance of a predictive model. This typically involves training a model on a dataset, using the model to make predictions on a holdout dataset not used during training, then comparing the predictions to the expected values in the holdout dataset
With Scikit-Learn it is extremely straightforward to implement linear regression models, as all you need to do is import the Linear Regression class, instantiate it, and call the fit() method along with our training data. So we can use a machine learning library to train on your data.

We have applied our model to 7 different states or cities, out of which the best result is in Broward. And the rest of the city's results are not up to the mark.

Data for the Airbnb sales were not available directly. So we took review data as someone will post the review if they have stayed there.


## Future Scope

The data for both the sales and covid was very limited. So the accuracy of our model prediction was very less. In the future, we can create synthetic data from past data and can improve the model's accuracy.

Considering datasets from other industries and study the following:

1. The effect of the pandemic on these industries.
2. Studying the correlation between these industries.
