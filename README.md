# Overview of the analysis
The goal of the project was to analyse usage of citi bikes in New York City. I took the [data]( https://www.citibikenyc.com/system-data) for the most popular month – August, created [visualisations, and put them in a story in Tableau]( https://public.tableau.com/profile/angela6018#!/vizhome/CitibikeData_16218817476910/NYCCitiBike?publish=yes)

Before I was able to analyse trip duration I had to convert second to datetime data type using Pandas library in Python.


# Results
I started my analysis with the question “How many bike rentals (rides) are done every day?”
I built the line chart with number of rides daily made in August.

![rides_per_day]()

There are 70-80 thousand rides per day with 95% confidence level.

Next, I tried to figure out who are the customers of citi bike. To answer the question, I built a couple charts. 

I divided all customers by age using bar chart and discovered that most of the customers are 25-40 years old.

![customers_by_age]()

Then I looked at gender distribution.

![customers_by_gender]()

65% of customers are male and only quarter of customers are female. There are also 10% of customers who prefer not to share the information. Most of them are short-term customers who doesn’t have annual subscription and rent bikes occasionally.

I wondered what is the average trip duration and built the line chart with number of rides for up to 3 hour of trip duration.

![trip_duration]()

The chart revealed that the most rentals are 5-10 minutes long.

Also, there some interesting findings at this point if rides are divided by gender.

![trip_duration_by_gender]()

Grey line, which represents the unknown customers, doesn’t have a peak at 5 minutes trip duration and is almost flat between 5 and 30 minutes. As we already know, unknows customers are mostly short-term customers. Now we can see that they rent bikes for longer time.

But what about prime time for bike rentals? I built a heatmap with weekdays and time when bikes were taken.

![trips_by_time]()

It’s easy to see that majority rentals are done at 8am - 9am and 5pm – 6pm, in other words, before and after office hours. As we know, the most of the rentals are 5-10 minutes long, now we can assume that people use bikes to get to work and back home, when the distance for walking is too long, but for bus/subway is too short to pay for ticket.
However, during weekends popular hours are in the afternoon. Probably, people take bikes for recreational rides.

Then I divided the heatmap by gender:

![time_trips_by_gender]()

This step revealed that, while female and male customers have the same pattern and take bikes to get to work, short-term customers tend to rent bikes during weekends and, as we know, they make longer trips.

So, we can define 2 main categories of customers:
1.	The majority of customers are males 25-40 years old who buy annual subscription and use bikes as a transportation between home and work. Also, there are 25% females who use the bikes in the same way.
2.	10% of rentals are done by short-term customers who customers who rent bikes for recreational trips usually up to 30 minutes in the afternoon during weekends.

The similar heatmap with only weekdays helped to discover that the best day for bike maintenance is Wednesday as there is the least count of bike rentals during that day among all types of customers.

![trips_by_day]()

Also, I wondered where the most popular bike stations are located. I built the map with number of bikes taken and return for each bike station.

![start_end_locations]()

I discovered that bike stations located in Manhattan are more popular than in others borough. Also, I noticed that starting and ending location are actually the same. In other words, if a lot of bikes are rented from a popular station, there are also a lot of bikes was left here. So, the bike station is not empty and shortage of bike doesn’t happen here. That means the manual relocation of bikes is not required. It’s regulated naturally. 

# Summary


![image](https://user-images.githubusercontent.com/59183092/119485302-e4cc5200-bd24-11eb-853e-fec1f7abece8.png)
