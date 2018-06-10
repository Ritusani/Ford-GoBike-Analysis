# Bike Rental Data - Exploratory Analysis 
_Written Data Analysis Exercise_

### By: Ritu Pardasani

**Link to Tableau Public** : https://public.tableau.com/profile/ritu.pardasani#!/vizhome/Fordgobike_Analysis/Ford-GobikeRentaAnalysis?publish=yes

I created some visualizations in tableau and created a story. I have published the workbook on Tableau public forum (the link above will take you there). I have also uploaded the workbook in the github files, its called as "Fordgobike_Analysis.twb".

Also, I would like to share with you an analysis that I have done before on a similar data set. This dataset was also a bike rental data set with a few different data points. I have also applied machine learning algorithm to predict the demand of bike rentals. I hope you find it interesting. You can check out the [project here](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/8181352227773554/2637382646426183/8924879640601769/latest.html).

Now coming to the dataset that I was given for this exercise. 
First and foremost step of data analysis is to look at the data. I downloaded the file and tried to look at the fields and see what kind of data I have been given in excel format itself. I made a few transformations in formats here and there to understand the data. I used some filters and sorting to find unique values and to understand the purpose of fields like "bike_ID". I have uploaded a little transformed data set on git hub because I used the same in my python notebook. 

The dataset is called as "2017-fordgobike-tripdata" has in total of 16 fields, shown as follows:  


1. Trip Duration (seconds)<br>

2. Start Time and Date<br>

3. End Time and Date<br>

4. Start Station ID<br>

5. Start Station Name<br>

6. Start Station Latitude<br>

7. Start Station Longitude<br>

8. End Station ID<br>

9. End Station Name<br>

10. End Station Latitude<br>

12. End Station Longitude<br>

13. Bike ID<br>

14. User Type (Subscriber or Customer – “Subscriber” = Member or “Customer” = Casual)<br>

15. Member Year of Birth<br>

16. Member Gender<br>

The next step is to reasearch a bit on bike-share and understand what bike share business is about and how it works. Ford go bike is a company that provides on-demand bike rentals for customers in the bay area, that through San Francisco and San Jose. Users can unlock bikes from a variety of stations throughout each city, and return them to any station within the listed cities, thus making it a good option for one-way trips. People use bike share to commute to work or school, run errands, get to appointments or social engagements and more. It's a fun, convenient and affordable way to get around.

The bikes are available for use 24 hours/day, 7 days/week, 365 days/year and riders have access to all bikes in the network when they become a member or purchase a pass. 

Three pass options are available:
1. Single Ride: One ride up to 30 minutes. Perfect for quick, one-way trips.


2. Access Pass: Explore the city with unlimited 30-minute trips in a 24-hour period.


3. Monthly Membership: Unlimited 45-minute trips for the whole month.


4. Yearly Membership: Unlimited 45-minute trips for the whole year.

As given by you, these are first and foremost analysis that I also thought of:

- Average, standard deviation, general distribution of trip duration


- What are the busiest dates and times?


- What are the most common starting and end stations?


- User population descriptions


- Some analysis on Users by calculating their age 


- Most popular route 


- Understanding bike rentals with respect to cities

## My 3 key take aways:

_**1. When is the Ford go bike used the most and by whom?**_

<img width="902" alt="screen shot 2018-06-10 at 2 36 53 am" src="https://user-images.githubusercontent.com/32205588/41200333-9a2b3912-6c57-11e8-842e-652f09499e41.png">


The line plot of hour of the day against bike rental count categorize by day of the week shown above - shows the difference of rental demand for weekday and weekend in different hours. The rental count remains active later in the midnight during the weekend than weekday. We can also see that the bike rental count has a dip at around 12 P.M. during weekdays, whereas around the same time during weekends shows peak of demand of the day. The peak of demand during weekdays is around 8 A.M. in the morning and 4 to 5 P.M. in the afternoon, possibly due to people who want to go to work or are done working and in need of transportation to go home. 

<img width="903" alt="screen shot 2018-06-10 at 2 45 36 am" src="https://user-images.githubusercontent.com/32205588/41200374-66094dc6-6c58-11e8-8f6f-015d55a26160.png">

When bike rentals are plotted against weekdays and are categorized by type of user - we see that mazimum bikes are rented by subscribers in the weekdays and since we also found the popular times, we know that people going to work or coming back from work are the most popular users of this bike at these times. Therefore, more such people can be targetted through promotions and dicounts to attract more subscriptions.


2. On which route is it used the most? 

This is also a very inetersting insight because then we know the busiest routes and this can help us to have a count of minimum number of bikes that should be available of these stations. If we are able to determine the demand at a particular route, we can use other technologies to predict the demand and hence ammend our business model accordingly. 

Now the station routes can be A to B and B to A as well, for this analysis I ahve taken these routes as two different directions rather than unidirectional because making it unidirection doesn't give us the exact number of rentals of either of stations.

I applied group by on the combination of start station name and end station name and counted the index, since thats the only unique value I had, Thus this gave me number of rides for each route.

3. An idea on increasing subscriptions:

This data is almost close to get a closer look on the customers which are the main drivers of the revenue. Understanding users is the best and the most important thing when it comes to data analysis of something which involves demands of users and revenue of the company is directly proportional to that demand. The revenue model for Ford bike share is based on their subcription model, main revenue comes from subscriptions. Thus finding ways to increase the number of subcriptions will directly increase the revenue. 

If I am given the user id of each user, I will be able to look at each user closely. Secondly, if I am also

# Some additional Take aways:

I have made a couple of graphs in tableau which give interesting insights like busiest day, clamest day, average trip duration, 80% of the customers are subsribers, ditribute of bike rentals over the year which also gives a seasonal demand idea, user demographics, yearly distribution with respect to type of user etc. Please have a look at my tableau workbook. 


## Aditional insights that can be found if gathered more data:

Apart from these some of the following insights I would like to know from the data but for these I would need some additional data points such as user id to get specific information particularly for a specific user:

- Which users are more likely to pay for yearly subscription?

- Which users are more likely to buy single rides or 24 hour passes? 

By looking for the insights above we could have a better idea of the composition of customers which will help the company put improve the marketing strategy accordingly and also come up with better commercials and market promotions which would increase the sale.

Also looking at the following insights would help us in understanding the using pattern of bikes with respect to each city which can help the company to distribute their resources more efficiently. 

- How does the use of bikes vary by cities? For example, do users in some cities prefer longer trips to shorter ones than users in other cities? 


- How many bikes are needed for each city? 

Data points like user id of the user and more details on the user type can be very beneficial to the business as marketing and sales strategy can be modeled accordingly. 
