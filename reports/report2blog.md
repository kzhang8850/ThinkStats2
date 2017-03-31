# What's the Chance You will Die to Terrorism?
## by Kevin Zhang
## 3/31/2017


Especially in recent years, Western fear of terrorism and paranoia toward specific regions in the Eastern Hemisphere, particularly the Middle Eastern region, has been on the rise. Now, the US government is voicing for controversial bills such as travel bans on Middle Eastern countries. The supporters' argument is that this is to protect against the possibility of another "9/11-like" catastrophe, for the sake of national security. This brings into question exactly how much more "national security" we need from terrorism. What are the chances that a given person in the United States will be the victim of a terrorist attack? The purpose of this article is to answer this question.

To answer the question, I found two databases of interest: the [Global Terrorism Database](https://www.start.umd.edu/gtd/), and the [World Bank Population Database](http://data.worldbank.org/indicator/SP.POP.TOTL). The Global Terrorism Database is claimed to be the most comprehensive database on terrorism in the world, with virtually every documented incident of terrorism around the world dating from 1970 to 2015. The World Bank database is a database that holds the population of every country in the world by year, from the 1960s to present time. To answer the question of the chance of being a victim of terrorism, I decided to derive the probability per capita of being hit by terrorism. In order to do so, I will require both data on terrorism and data on population, thus requiring two databases.

I decided to define "a victim of terrorism" by four of the variables found in the GTD database, which are for a given incident, the number dead, the number wounded, property damage, and hostage situations. The dead and wounded categories were numerical values, and property damage and hostage situations were binary values that denoted whether that criterion occurred in the given incident or not. I deemed that these were sufficient because they cover a wide breadth of various results that can occur during terrorist incidents, such as whether people were harmed, whether the surrounding environment was harmed, and whether things escalated to become "complicated".

To calculate the probability of terrorism per capita, I perform the following steps. For a given year in a given region, I would total up the number of kills, wounded, and instances of damage or hostages, and then divide them all by the total population of the region in that year. I would do this for 45 years, from 1970 to 2015, to not only show what the chance is but also how it evolved over time. In other words, my punchline will look like X probability for 1 person, with X = 1 meaning that it will definitely happen, and X = 0 meaning that it's impossible. As an aside, further into the report I will report this probability differently, where the notation will be 1 in X people; this is just the inverse of the former probability, but will be more meaningful compared to the value of the former.

To provide quantitative analysis, I derive probabilities for both North America (NA), because it is the region of interest, and the Middle East (ME), because it is considered the center of terrorism, and thus provides a good reference point from which to view and better understand the NA values.

To explore the variables in the GTD database in detail, check out the [documentation](https://www.start.umd.edu/gtd/downloads/Codebook.pdf)

For a deeper dive into the source code, check out my [ipython notebook](https://github.com/kzhang8850/ThinkStats2/blob/master/code/report2.ipynb).


I calculated the probabilities for deaths and wounded separately from property damage and hostage situations, due to the nature of the variables. To begin, I created Figure 1 below by calculating the chance of being physically harmed by a terrorist over time.

![alt text](Casualty.png)

*Figure 1: A time series graph showing the probability of being harmed by a terrorist both in North America and the Middle East. The NA graph is almost 0 and has been for the past 40 years. The ME graph reaches closer towards .00008, and is about two orders of magnitudes higher than the NA graph. This shows NA has a much lower chance of terrorist casualties than ME. Even then, the scale of the graph tells that an NA person has an extremely low chance of dying to a terrorist.*


Figure 1 shows a time series graph qualitatively displaying the probabilities for being harmed by a terrorist incident in both the NA and ME regions. Immediately upon seeing it, it is clear that the NA region has significantly lower probabilities than the ME region, which is consistent over time. Note that the large spike in the ME graph, which is correlated with the only major spike in the NA graph, is most likely due to the 9/11 attack which occurred in 2001. The NA graph basically hugs the x-axis for the entire duration of the past 40 years, meaning that the chance of being hit by a terrorist in the US is nearly improbable. In comparison, the ME graph has a more tangible result, reaching up to .00008, which is about two orders of magnitude higher than the NA graph. This shows that NA has a much smaller chance of being hit by terrorism than ME. In addition, looking at the scale of the two graphs, with is the hundred thousandths for ME and even smaller for NA, it is reasonable to suggest that the chance of being harmed by a terrorist in NA is negligibly small.

To more quantitatively display the results above, Figure 2 below shows direct comparison of the probabilities for the two regions for the most recent year of available data, 2015.



|North America | Middle East | Difference |
| :------: | :----: | :-------:|
| 1 in 4,139,212 | 1 in 11,997 | NA is 345 times less likely|


*Figure 2: A table which shows the most recent probabilities of being harmed by a terrorist, which can be deemed the most relevant to people in present time. Note that NA is 345 times smaller than ME, and even then, the chance of a person being attacked by a terrorism in ME is quite low. The extremely small values point toward irrational fears from the people.*

Figure 2 is a table that shows a direct comparison between the most recent probabilities, calculated for 2015. As can be seen, the NA region's probability is 345 times less likely than that of the ME region's, and looking at the ME probability alone, it is already a quantitatively small value. To give a sense of comparison, this [article from Tulane University](http://www.tulane.edu/~sanelson/Natural_Disasters/impacts.htm) provides some events that have probabilities higher than that of the probability of being harmed by terrorism. While the credibility of the statistics given in the article aren't necessarily confirmed, these statistics are meant just to provide an additional reference point for how small the numbers in Figure 2 are. Looking at the article, North Americans have a higher probability of being killed by an asteroid than being killed by terrorism.

To provide another perspective to this question, I created Figure 3 below by calculating the chance of being a victim to property damage or a hostage situation by a terrorist over time.

![alt text](Victim.png)

 *Figure 3: A time series graph showing the probability of being a victim of property damage or a hostage situation by a terrorist both in North America and the Middle East. The NA graph has been consistently decreasing over time to almost 0, suggesting that NA has almost no chance of having property damaged or hostages taken as well. The NA graph is also significantly lower than that of the ME graph, and the scale of the graph is an order of magnitude smaller than the casualty graph. This once again supports the idea that the average person in NA is very unlikely to be hit by terrorism.*

Figure 3 is another time series graph, this time showing the two regions for the binary variables of whether the incident included property damage or a hostage situation. As can be seen, once again the trends and comparison between the ME region and NA region are similar to that of the casualty graph, where the NA graph is lower than that of the ME graph. However, the major difference this time is to notice the y-axis scale. It's actually an entire order of magnitude lower than that of the casualty graph.  This means that the probability of a person in the North America having their property damaged or becoming a hostage is even lower than that of them just being killed. This result also states with additional likelihood that the probability of being affected by terrorism in NA is extremely low.

Looking at Figure 3 in a quantitative manner, Figure 4 below shows the derivation and direct comparison of the probabilities for the two regions for the most recent year of available data, 2015.


|North America | Middle East | Difference |
| :------: | :----: | :-------:|
| 1 in 15,622,187 | 1 in 242,492 | NA is 64 times less likely|


*Figure 4: A table which shows the most recent probabilities of being a victim of property damage or a hostage situation by a terrorist. Notice that once again the NA region has a lower probability. In addition, the probabilities this time are much smaller than for casualties, showing the chance for this criterion is especially low. This further supports the idea that people have unfounded fears towards the Middle East.*

This figure shows another table, this time for the property damage or hostage criterion. Once again it can now be numerically seen that the NA region does indeed hold a lower probability than the ME region for being affected by terrorists, this time 64 times less likely. In addition, the probabilities for this criterion are an entire order of magnitude lower than that of the casualty calculations, as seen qualitatively in the graph. Focusing on the numbers by themselves, it is quite clear that they are extremely small. Looking at the [article from Tulane University](http://www.tulane.edu/~sanelson/Natural_Disasters/impacts.htm) again, the comparisons become even more outrageous. For the United States, a person could die from a shark attack more easily than have their property damaged or become a hostage to a terrorist.

Based on this data, it is reasonable to suggest that the chance a person in the United States is affected by terrorism is negligible, especially when comparing it to the chance of being affected in the Middle East, the very center of terrorism. The data suggests that the fears and reactions towards Middle Eastern citizens could potentially be said to be irrational or unfounded.


##### Limitations and Next Steps:

Evidently there are some shortcomings of the model and the data I chose to use. The GTD database particular, could potentially be incomplete in some ways. While the variables I used were mostly well documented, there was a good amount of the database that contained missing data, so it's highly possible that some things were mis-recorded or that incidents were missing. In addition, my quantitative analysis could've potentially dived deeper to see distributions or standard deviations of the probabilities, which might've made the results more clear. In addition, this analysis assumes both domestic terrorism and foreign terrorism lumped together as a singular entity, whereas in reality they are quite different. That could've been a potential confounding variable that the GTD database did not have answer to, and had it been addressed might've led to more conclusive or interesting results.

Some next steps would be to see if it's possible to differentiate between foreign and domestic terrorism, which might be an area of interest. Another idea would be to explore other regions with this same approach and see what comes of it. Finally, potentially diving deeper into more quantitative analysis onto the probabilities might yield better results.

In any case, I believe this is a compelling statement that the chance of the average person being affected by terrorism in the US is close to 0, so people should stop being afraid of an enemy that virtually doesn't exist.
