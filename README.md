# NYC_CitiBikes

## Project Overview
In this project, we analyzed the ride data of the citibike bike-sharing platform in New York City to determine whether a similar service could be feasible in the city of Des Moines, Iowa. Given the large differences in size and character between the two cities, we needed to create visualizations of the citibike data which could convince investors that this service could work in Des Moines. To do this, we first used Python (pandas) to remove the index from the dataset and export the transformed dataset to be used in Tableau, a business analytics software. Tableau was used to create easily interpretable visualizations based on criteria of the dataset including average trip times, peak hours of usage, user type (subscriber vs customer), as well as user gender. In total, we created 7 visualizations that were merged into a single story-board which compactly displayed each graph for easy presentation to investors. 

## Results

### Trip Duration (All riders)
In this graph, we can see that by far the most popular ride duration is somewhere in the 5-10 minute range. This data suggests that these bikes are mostly being used by professionals to commute to their jobs indicated by the short ride durations. I would not make sense for tourists to be taking rides of such short duration as tourists generally try to visit many different areas of a city rather than sticking to one locality. Instead, it makes much more sense that the bikes are being used mostly by professionals who live close to their workplace and have no need for a car, thereby making citibikes a cheap and effective mode of transport. 

### Trip Duration by Gender
This graph is similar to the one above in purpose however, it offers a more detailed view of the citibike user demographics. Once again, we see that the 5-10 minute trip range is most popular across all genders, although the line for unknown genders has a much flatter peak with rides of 25 minutes being roughly as common a rides of 5 minutes. There is still a significant amount of rides lasting 10-30 minutes for men and women but, any ride longer than this is rare as past this point the lines are moreless in line with the x-axis. This data suggests that men are far more likely to use this service compared to other genders. This is evident based on the area under the curve of the Male line being much larger than the areas of the other genders. There is still a significant userbase of women and people of unknown gender so they should still not be overlooked when planning on how to implement citibike in Des Moines.

### Ride Startimes by Weekday
This graph is a heat map showing the count of rides started at each hour of the day as well as the day of the week. In this graph, we see that during weekdays, the most popular startimes are at 7-9 AM and 5-7 PM. This supports our previous hypothesis that these bikes are being used mostly for commuting as these times correspond to the standard workday hours for office workers in the United States. On the weekends, the bikes are equally popular during all daylight hours, with a small increase in rides around noon. Overall, the bikes are ridden much more during weekdays, especially during commuting hours.

### Ride Startimes by Gender and Weekday
This graph is the same as the heatmap described above but also accounting for user gender. For men and women, the trend noted in the above heatmap remains the same. The bikes are mostly used during workday commuting times with moderate, spread-out usage on the weekends. Interestingly, for people of unknown gender, there is no clear pattern for ride startimes during the week. On weekends, the ride startimes are in-line with those of men and women.

### Weekday Trip Count by Userype and Gender
