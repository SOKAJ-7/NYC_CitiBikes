# NYC_CitiBikes

## Project Overview
In this project, we analyzed the ride data of the citibike bike-sharing platform in New York City to determine whether a similar service could be feasible in the city of Des Moines, Iowa. Given the large differences in size and character between the two cities, we needed to create visualizations of the citibike data which could convince investors that this service could work in Des Moines. To do this, we first used Python (pandas) to remove the index from the dataset and export the transformed dataset to be used in Tableau, a business analytics software. Tableau was used to create easily interpretable visualizations based on criteria of the dataset including average trip times, peak hours of usage, user type (subscriber vs customer), as well as user gender. In total, we created 7 visualizations that were merged into a single story-board which compactly displayed each graph for easy presentation to investors. 

## Results

### Trip Duration (All riders)
In this graph, we can see that by far the most popular ride duration is somewhere in the 5-10 minute range. This data suggests that these bikes are mostly being used by professionals to commute to their jobs indicated by the short ride durations. I would not make sense for tourists to be taking rides of such short duration as tourists generally try to visit many different areas of a city rather than sticking to one locality. Instead, it makes much more sense that the bikes are being used mostly by professionals who live close to their workplace and have no need for a car, thereby making citibikes a cheap and effective mode of transport. 

![Trip Duration (All Riders)](https://user-images.githubusercontent.com/93050931/153681854-c945907c-38b1-4a79-89e7-7209d5373013.png)

### Trip Duration by Gender
This graph is similar to the one above in purpose however, it offers a more detailed view of the citibike user demographics. Once again, we see that the 5-10 minute trip range is most popular across all genders, although the line for unknown genders has a much flatter peak with rides of 25 minutes being roughly as common a rides of 5 minutes. There is still a significant amount of rides lasting 10-30 minutes for men and women but, any ride longer than this is rare as past this point the lines are moreless in line with the x-axis. This data suggests that men are far more likely to use this service compared to other genders. This is evident based on the area under the curve of the Male line being much larger than the areas of the other genders. There is still a significant userbase of women and people of unknown gender so they should still not be overlooked when planning on how to implement citibike in Des Moines.

![Duration_gender](https://user-images.githubusercontent.com/93050931/153681883-0390addb-721a-4708-ad52-d5cf4ca71402.png)


### Ride Startimes by Weekday
This graph is a heat map showing the count of rides started at each hour of the day as well as the day of the week. In this graph, we see that during weekdays, the most popular startimes are at 7-9 AM and 5-7 PM. This supports our previous hypothesis that these bikes are being used mostly for commuting as these times correspond to the standard workday hours for office workers in the United States. On the weekends, the bikes are equally popular during all daylight hours, with a small increase in rides around noon. Overall, the bikes are ridden much more during weekdays, especially during commuting hours.

![week_trips](https://user-images.githubusercontent.com/93050931/153681910-d8d0fa11-690d-4ec5-910e-48ec4a01bc6c.png)


### Ride Startimes by Gender and Weekday
This graph is the same as the heatmap described above but also accounting for user gender. For men and women, the trend noted in the above heatmap remains the same. The bikes are mostly used during workday commuting times with moderate, spread-out usage on the weekends. Interestingly, for people of unknown gender, there is no clear pattern for ride startimes during the week. On weekends, the ride startimes are in-line with those of men and women.

![week_gender](https://user-images.githubusercontent.com/93050931/153681925-f0d7590a-99c6-4a85-a259-2ab8662a4323.png)



### Weekday Trip Count by Usertype and Gender
This heatmap shows the count of rides taken during each day of the week, broken down based on whether a user is a customer (single-user) or a subscriber as well as the users gender. Looking at the graph, we can see that the working days of the week are clearly the more popular days overall but especially amongst subscribers. During the week, Wednesdays appear to be the least busy day amongst all demographics. Amongst customers, we can see that weekends are actually considerably busier than the workweek, although with much less overall trips. As far as gender is concerned, these trends seem constant across all user/gender combinations with the exception of subscribers of unknown gender. Amongst this demographic, there doesn't appear to be any day(s) where there is a considerable rise or drop in bike usage. This data suggests that the subscriber base mostly uses the bikes for commuting with moderate weekend usage. The customer userbase most likely are tourists and weekend joyriders looking to spend time outdoors.

![User_gender_week](https://user-images.githubusercontent.com/93050931/153681944-1aeec1f7-c634-4a33-a54d-bd5caf12f190.png)


### Usertype proportions
This pie chart is a visual representation of the difference in the count of subscribers to customer users. We can see that there are roughly 4.3 times the number of subscribers to customer-users. The obvious takeaway from this graph is that having a strong subscriber base has been a large part of citibike's success in New York City.

![user_prop](https://user-images.githubusercontent.com/93050931/153681967-e9da4f25-ce52-4fb7-8f49-ace161acdc99.png)


### Bike Utilization
This heatmap shows the number of rides each bike in the fleet has completed. A darker square signifies higher usage and can be used to predict the likelihood a given bike will need to undergo repairs. These repairs will take resources out of our budget so it is important that we minimize the amount of repairs needed by spreading the number of rides each bike completes evenly across all of the bikes in our fleet. This would ideally appear as every single block in our graph having the same size and a similar shade of blue. This is not the case in our graph. It appears that roughly 66% of the graphs area is occupied by a shade of blue below the median shade represented in our legend, one must also realize that because ridecount also imfluences the size of each square(bike_id) this number represents a much larger share than 66% of all the bikes. The inverse relationship is true for heavily used bike as a very small percentage are being used at much higher frequency relative to the total fleet. One could infer from this graph that this is because the bikes are not being rotated from station to station. So, bikes in high usage areas will break down at far higher realtive to other bikes, resulting in inefficiencies in the repair budget. A system where bikes are continuously rotated from station to station could help spread out the wear and tear dealt to each bike. resulting in lower repair costs.

![Bike_usage](https://user-images.githubusercontent.com/93050931/153682088-410102db-b429-4b4a-8378-9e0a647edf62.png)


### Summary 
As mentioned in the results section of this report, it appears that the majority of the citibike userbase is made up of subscriber-users with a small percentage of users being customer-users. Based on the times and days at which citibike is most popular, as well as average trip durations, it is highly likely that citibike's userbase is dominated by commuters looking for an inexpensive way to get around the downtown core of New York City. It also seems that our userbase is much more likely to be male as opposed to women and people of unknown gender. Lastly, it is clear that the way bikes are currently distributed across the citibike network is resulting in cost-inefficiencies regarding bike repairs.

To understand some of the concerns mentioned above, I suggest two visualizations be created from the citibike data:

- An interactive map where each bike ID is represented by a dot who's size corresponds to the number of trips completed. This could help determine which bikes need to be rotated from station to station.

- An interactive map showing which stations are more likely to be used by a customer versus a subscriber. This could understand the types of neighborhoods where each type of rider is more likely to be located in and cross-reference that with our knowledge of Des Moines' downtown to asses the viabilty of citibike in our city. 
