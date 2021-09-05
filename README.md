

                                                        











1. Problem Statement: 
The Play Store apps data has enormous potential to drive app-making businesses to success. Actionable insights can be drawn for developers to work on and capture the Android market.
Each app (row) has values for catergory, rating, size, and more. Another dataset contains customer reviews of the android apps.
Explore and analyze the data to discover key factors responsible for app engagement and success.

2. Objective: 
The objective of this project is to deliver insights to understand customer demands better and thus help developers to popularize the product. It is of 10k Play Store apps for analyzing the Android market. This dataset contains details of different applications and reviews from different users.

3. Steps Involved:

 ●	Loading the dataset: 
 
 
 
 We created a directorial path for the play store dataset, using the Pandas read function we read it. It has a shape (10841,13) it means it has 10841-row labels and 13 features or   column labels.
 After reading it we found which are the dependent variable and which are the independent variable, there is one dependent variable which is the number of installs or just         installs, other are independent variables. 

 ●	Cleaning and Transforming Data:
 
 
 
Cleaning is the process of removing undesired features, values, or any suffix, prefix, or anything which can produce an exception. 
Transforming is completely a different process, transforming is required to ensure the consistent data type of features because inconsistent data type will generate an obstacle during the execution of the program. 
These two processes have specific subprocesses as follows.

●	Unwanted Data Removal:


In this step we ensured to make a data type of feature consistent by removing characteristics from the values of features, to make them usable.


●	Null values Treatment:


Two features of our data set have many null values, the first one is size and the second one is rating feature, so we filled null values with a method of forward linear interpolation. We implied this forward interpolation cause we can assume that the size of the application could be an average of sizes available for a particular category, and talking about rating we have taken the median of rating for each category, and then we filled it.


4. Exploratory Data Analysis:


Following are the observation which using Exploratory Data Analysis and visualization.

4.1.1 Average Rating Distribution Plotly Bar Plot: 


The average rating distribution for every category in the entire play store data set is around 4.2 out of 5. That’s incredible!

Your app's rating will affect its chances of being featured. Apps with 3 stars or lower will not be featured. The app rating is an important aspect of ASO (app store optimization). Negative mobile app reviews combined with a poor rating will hurt your app's rank, but great app reviews and high ratings will help increase your app's rank.
![newplot (37)](https://user-images.githubusercontent.com/75175373/132113138-8a758fcc-8b38-4926-85cf-612bdcc46b12.png) fig 1: Category(free & paid) vs Ratings
![newplot (42)](https://user-images.githubusercontent.com/75175373/132113584-a6900e80-03a4-4b8c-9f33-3e867781bfdd.png)
Fig 2: Price vs Rating
![newplot (28)](https://user-images.githubusercontent.com/75175373/132113592-9f03a34f-3c78-432d-9887-26981a9c99fb.png)
Fig 3: Rating vs Size
![newplot (29)](https://user-images.githubusercontent.com/75175373/132113599-2ae9380a-15b5-463a-8b12-03a7ad8aa2e1.png)
Fig 4: Reviews vs Rating
                                     



4.1.2 Correlation Between features Seaborn Heatmap:


By plotting seaborn heatmap correlation we got to know that there are five features in the given play store data set which are highly correlated with each other, reviews are highly correlated with the number of installations. There are 64% chances of downloading an application by users if previous reviews on that applications are positive.
Likewise, size and download or the number of installations are negatively correlated, It means as the size of the applications increases user avoids downloading those applications.
 Another two features which correlate with each other are category type and the number of installations. It is found that people will still download an application with a bigger size if it is free of cost. But customers are not willing to download a paid bigger size applications.
 ![heatmap_new](https://user-images.githubusercontent.com/75175373/132113149-71f8b0df-c948-4796-a8d5-0cc407a2931d.png)
 
fig 5: Heatmap Correlation Matrix


4.1.3 Content Rating, And Number of Application Per Category Countplot:


Most of the applications on google play is having a content rating for everyone. However, only the dating category is for the mature 17+ age group.
We used the count plot to count the total number of applications available inside a particular category.

![content_rating_pro](https://user-images.githubusercontent.com/75175373/132113160-ec6d0109-f444-49c7-9e32-61a46ec19eda.png) fig 6: Category vs Content Rating
![newplot (21)](https://user-images.githubusercontent.com/75175373/132113618-418707a4-f57f-4043-bcc2-284b9d4a680f.png)
Fig 7: Content Rating vs Installs
![newplot (26)](https://user-images.githubusercontent.com/75175373/132113176-e22c78ef-3fa1-4ee6-94dd-8350e427482b.png) fig 8: Category Vs App Count


4.1.4 Size And Type Effect On Number of Downloads Or Installs Plotly Scatter Plot: 


We used the scatter plot for the understanding effect of the size of the applications and their type; on the number of installs or downloads. 
The scatter plot we implied gives the result that when the size of applications increases there is a decrement in the number of downloads.
![newly_distributed_size](https://user-images.githubusercontent.com/75175373/132113270-2e8eac6e-0096-4748-8fc6-ba8425313c81.png) fig 9: Size Distribution
![newplot (25)](https://user-images.githubusercontent.com/75175373/132113178-8780d8c5-1c84-4fd6-b0da-c479fa7e88b0.png) Fig 10: Size vs Type Vs Installs


4.1.5 Most Reviewed vs Most Space required vs Most Installed Category Plotly bar plot:


We used plotly bar plot to find out the most installed, most reviewed, and most space-consuming categories.
With the help of plotly bar plot, we found that gaming and communication these two categories have the highest reviews and thus the number of downloads. However, family and gaming categories are the two most space consuming categories in the google play store.
![newplot (30)](https://user-images.githubusercontent.com/75175373/132113497-b39c3e0b-65a3-497b-85a5-83af93d9bb36.png)
Fig 11: Category vs Percentage Space Consumption
![newplot (43)](https://user-images.githubusercontent.com/75175373/132113539-0295f9ee-2eaa-4169-a45b-f6f56760331b.png)
Fig 12: Category vs Reviews
![newplot (41)](https://user-images.githubusercontent.com/75175373/132113189-ef22f438-b35c-4d91-8524-acb4e4973910.png) Fig 13: Category Vs installs



4.1.6 Last Update vs Year vs Month:
we can conclude that before 2012 there were no paid apps, but with the years passing free apps has been added more in comparison to paid apps, By comparing the apps updated or added in the year 2011 and 2018 free apps are increases from 0.01% to 64.61% and paid apps are gone from 0.27 to 3.18%. So, we can conclude that most people are after free apps.
![newplot (40)](https://user-images.githubusercontent.com/75175373/132113195-d89029a6-6868-49ba-b9d9-580dfe895ac9.png) Fig 14: Last Updated Vs App Added
![newplot (36)](https://user-images.githubusercontent.com/75175373/132113449-183bd241-a207-477c-b71b-d055ca989bbb.png)
Fig 15 : Category Vs Last Updated Month

4.1.6 Most Installed Android Version:
![newplot (32)](https://user-images.githubusercontent.com/75175373/132113751-484abdfc-1a3e-4bdd-9ce1-05ab887af5ae.png)
Fig 16: Android Version vs Installs


4.1.7 Sentiment Distribution and Analysis Matplotlib histograms and pie-chart:


There are more than 63% reviews are positive on google play store, around 26% are negative and remainning 11% neutral.
![Percentage_distribution](https://user-images.githubusercontent.com/75175373/132113241-49335985-f4b7-436c-a47b-5441867cecb0.png) 
Fig 17: Percentage Reviews Sentiment

![newplot (34)](https://user-images.githubusercontent.com/75175373/132113468-e0a5ab93-470c-40d9-b437-ded96712b122.png)
Fig 18: Category vs Reviews Sentiment





5. Conclusion:


That's it! We reached the end of our exercise. As per our Exploratory Data Analysis on the google play store data and user reviews data, An ideal application on the google play store should have the following properties.


1. Category Type: Almost every customer on the google play store expects that application should belong to the category free.


2. Size vs install vs type: As we have observed in the size vs installation vs type scatterplot, the ideal size of the application should be below 40 MB and max up to 50 MB. we have seen that peoples are less interested to install and use heavy-size applications even though the application is free of cost.


3. Reviews vs install: We have experienced from the seaborn heatmap that reviews on the google play store are highly correlated with the rate of installation. Reviews are given by users as per their experience with the application. So reviews on the application should be examined properly to get to know the performance of the application, whether it is catering to the need of users, From review, we will get an idea on which aspect to work on.


4. The most installed category: As we have explored applications belongs to the category gaming and followed by communication are being installed the most, secondly, applications from the productivity category followed by the social media category are being installed the most, It gives us tips to choose domain as per the customer affection inclination.

5. Size vs Rating vs Reviews vs Price: We have seen that if there are fewer number of reviews, there will be a lesser number of ratings, and as price increase, there are fewer ratings as there are fewer downloads.


6. Android version vs Installs vs Size: We observed that android version 4.1 and up is being installed most and the size of the applications is ranging from 0 to 40 Mb. It is a hint for us to choose the version for the applications.











































































































