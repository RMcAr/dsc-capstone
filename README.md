# Predicting Online Game Player Counts through SARIMAX

## Introduction

As we enter the second decade of the 21st century, the interconnectedness of our world increases every day. Once, activities done alone are now conducted online with fellows, and video games are no different. An estimated 2.7 billion gamers exist in the world, and this number can only increase due to the impact COVID-19 has had, and will continue to have, on our culture. With that in mind, businesses that serve these customers must be able to handle the changes that surround us. They must effectively predict how their customer base will be changing in the long run to address capital restrictions, how their player base changes over the medium run to address capturing the largest player base for events/announcements, and how their player base changes over the short run to to address how employing short-term retention strategies. 

### Process

#### Data

We established criteria for selecting games from steamdb.info. Our selected games to investigate should:
1. Be online. 
2. Be popular.
3. Not be a new release.
4. Have in-game events, seasonal or non-seasonal
5. Have in-game rewards
6. Be available worldwide. 

While it is not imperative for our games to meet all of these criteria, the more that are met, the better we can apply the given game to our investigation. After some initial research on SteamDB, the following games meet most of our criteria, and will be used for our investigation:

- Rocket League, 2015
- Counter Strike: Global Offensive, 2012
- DOTA 2, 2013
- Team Fortress 2, 2007

#### Exploratory Data Analysis

- Our data suggested that as player counts increase, volatility in the number of players increases at a greater rate. This suggests that player counts get more unpredictable as number of players increases. 

- Events, surprisingly, did not strongly impact number of twitch viewers. This suggests that either our investigation is examining the wrong type of 'event' or that events are not an effective way at increasing viewership. 

#### Model Construction

We constructed two types of models. First, we performed basic model construction for each game, using this game's past data to predict the game's future data. Next, we attempted to construct an averaged model that could be applied to each game successfully. We accomplished this by taking the mean percent change of all of our games and constructing a model from the engineered data. 

#### Model Selection

We found that in the long run, our averaged model performed best, as our game-specific models tended to diverge in a dynamic forecast. 

For short run predictions, however, game-specific models perform best, as they capture the trends that are inherent to each game. 

#### Recommendations

1. As a player base increases, so too does the volatility of the number of players. This means that the maximum amount of players will increase exponentially as average number of players increases. Accounting for this would suggest that a company should invest in server space (capital) at a rate faster than the growth of its player base. 

2. Through our investigation of events, we found that an ongoing event did not have a significant impact on number of players, but did have a significant impact on number of twitch viewers. If a company is trying to increase social media presence, then events are an effective way of increasing viewership.

3. When predicting long-term player trends, a model built from multiple games will perform better than a model built from that one games data. Conversely, when predicting short-term trends, including data from other games hinders predictive power. 

#### Furtther Work

One major way in which this investigation could be improved is in data collection frequency, specifically if our data was collected at least hourly, instead of daily. This would allow us to discern smaller trends in player counts, giving better context to how these figures move throughout the day, instead of throughout larger periods as we have investigated here.

Attempting to include events as an exogenous variable in our modelling hindered accuracy, though the relationship between events and player counts was shown to exist in our EDA section, however small it may be. This suggests that our events, as we defined them, did not explain enough to merit being included in our final modelling. We should therefore work on collecting event data in a different way, or redefine 'event' for use in our investigation.

Finally, this process could be completed for games of a particular company. It may be possible that building models from one companies portfolio of games may lead to a more accurate model than our averaged model constructed here.

#### Communication

Ryan A McArthur, Flatiron School, Data Science
rmcar522@gmail.com