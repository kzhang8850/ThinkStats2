# Report 2 Review
# William Lu and Apurva Raman - Does it get Warmer before it Rains?
## by Kevin Zhang
## Data Science 3/27/2017

The primary motivating question of this report is whether temperature deviations, specifically warmer temperatures, can predict precipitation. The team is trying to prove a weather myth that warmer weather is an indicator of coming precipitation.


The dataset used is the database from Boston and Seattle about historical climatological data. The agency who produced this data is the US National Oceanic and Atmospheric Administration (NOAA), which seems to be a pretty credible source.


The team performed scatterplot analysis to create a visual of temperature deviations in Seattle with vertical lines to represent precipitation. They also used CDFs on the precipitation data and temperature deviations for Seattle and Boston to see if there were more warmer days that had precipitation. Finally, they directly looked into the predictive power of temperature deviation on precipitation days using a logistical regression model.


The analysis provided by the team does indeed answer the question. They attempt to prove through visual analysis of the scatterplot that there was no correlation between precipitation and temperature. They also used a different representation in the CDF to show that different cities can yield different results regarding trends between precipitation and temperature. Finally, they attempted to show quantitatively that no such correlation existed with regression. The information is all there, however I would argue that some additional questions existed that weren't answered, and the reader must do excessive work to understand what is being presented.



I think the article is interesting, as weather prediction is always a cool topic to explore. The team's question, framework, and analysis approach were all well-thought out and engaging. I would argue that the clarity of the analysis could use a bit of work. Going down section by section:

- The introduction was thoughtful and interesting.
- The framing of the problem was excellent, it really helped me understand what I was getting into. The breaking down of the problem into two parts, the precipitation and the temperature, and then elaborating on how to quantify and evaluate them, made me very prepared to dive deeper into the analysis and understand what I should look out for. One small thought was was ambiguity of the "before" idea in "warmer before it rains". For instance, maybe warmer temperature today tends to result in precipitation three days later, or rather than the very next day or even the day of. It seemed that the original idea was that they were looking at warmer weather and then precipitation the day of, so maybe just clarifying that would be nice.
- The analysis part was a little confusing:
  - The scatterplot could've used work. I'm not sure that lacing lines together with dots was a useful representation, as I get the feeling that even if a correlation existed I wouldn't have seen it because of the clutter and large number of data points being shown. An alternative might be to look into color-coded scatterplots, where the same scatterplot is used but color is used to denote precipitation. That way, you remove all the lines, but you can still tell whether precipitation days (a specific color dot), correlate with higher temperatures (the location of the dot on the graph). It appears that the team was okay with the lack of clarity because that was the intention, so this is more of a suggestion should they choose to do so.
  - The CDFs are probably the best pieces of analysis on this paper. I thought they were well-done and held the most information I could easily see. One small tidbit is that I wish there was explanation on what the graphs, including the CDFs, mean. More often than not, the text just presents a graph and then immediately jumps to the conclusion. Some explanation of what the graph is trying to say and how that proves the conclusion would be helpful. A basic example is something like, "the CDF shows that the precipitation graph is more to the right of the non-precipitation graph, showing that Boston tends to have warmer temperatures before rains."
  - The regression analysis seemed vague. It appears that the point was to show a progression of calculations to arrive at the answer of 51%. Perhaps a more visual way of showing that calculation derivation, such as a table to visually represent all the numbers presented, would be nice. In addition, the end result, 51% seemed relatively high for a probability, when in fact it was being compared to 50-50 implicity. Explicitly stating the 1% difference between the control and the prediction would make it easier to understand that 51% is indeed a nonsignificant probability.

The presentation is quite professional. The visuals were well made and properly labeled, the spelling and grammar was fine, and formatting was clear and well spaced-out. I think the idea and the flow was great, and just some more clarity so that the reader wouldn't have to do so much work to understand what was happening would make it stellar.
