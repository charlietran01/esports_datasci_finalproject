---
title: "Esports: League of Legends"
author: "*Charlie Tran*"
date: "12/18/2020"
output: 
  html_document:
    keep_md: TRUE
    toc: TRUE
    toc_float: TRUE
    df_print: paged
    code_download: true
    theme: united
  
---





```
## -- Attaching packages --------------------------------------- tidyverse 1.3.0 --
```

```
## v ggplot2 3.3.2     v purrr   0.3.4
## v tibble  3.0.4     v dplyr   1.0.2
## v tidyr   1.1.2     v stringr 1.4.0
## v readr   1.4.0     v forcats 0.5.0
```

```
## -- Conflicts ------------------------------------------ tidyverse_conflicts() --
## x dplyr::filter() masks stats::filter()
## x dplyr::lag()    masks stats::lag()
```

```
## 
## Attaching package: 'lubridate'
```

```
## The following objects are masked from 'package:base':
## 
##     date, intersect, setdiff, union
```



## The Growing Esports Industry
  
The first competitive games started on arcade machines in the late 1970s with Space Invader and Twin Galaxies where the professional players strive to beat each other's record to become the world record holder. In the 1980s, more games were released that many of us know today like Pac-Man. A shift from arcades to gaming consoles occurred with the release of Nintendo systems. The new popularized way of gaming was becoming more accessible to the average consumer than ever before. As Nintendo continued to grow through the 1990s, the fast advancing computer technology became a new and different mode of gaming with personal computers. 

![1980s competitve games](1980sgamespicture.png)

The large amount of competitive users led to organized competitions where tens of millions of fans of the top games follow these matches allowing the game companies to profit. Eventually these competitive matches transformed into a sport known as Esports. Many of the top games help create and influence the start of Esports teams and organizations made of world-class gamers. In total, hundreds of millions of US dollars are profitted from the Esports industries only in terms of prize earnings from professional tournaments. 

- (HERE OF BEFORE THE PARAGRAPH ABOVE) DISCUSS THE DATA COLLECTION PROCESS AND POSSIBLY A CLEARER INTRO TO THE TOPIC IF NOT CLEAR ENOUGH ALREADY 


```
## `summarise()` ungrouping output (override with `.groups` argument)
## `summarise()` ungrouping output (override with `.groups` argument)
```

![](esports_datasci_finalproject_files/figure-html/unnamed-chunk-1-1.png)<!-- -->

As seen above, in late 1990s to the late 2010s there was a exponential growth in the tournaments' prize earnings from all Esports teams, orgnaizations, and all variety of competitive. In fact the earnings from tournaments in the last 3 years totals to more than the 20 years before! Unfortunately for the Esports industry in 2020, the toll of the COVID-19 pandemic is evident where large gatherings were impossible to view the professional matches. the canceled tournaments destryed the potential of growth of Esports although some game companies like Riot Games worked with the teams to provide a remote competitive experience to provide a fair tournament to take place (more on this later).

These Esports organizations are created with a focus on a specific game and eventually grow from tournament prizes.

![](esports_datasci_finalproject_files/figure-html/unnamed-chunk-2-1.png)<!-- -->

The bargraph above shows the top Esports organzations/teams around the world with teams that have contracted professional players who competed in professional matches and earn the tournaments prizes. One of the games that provide one the largest percent of the organization's total earnings is League of Legends.

![](esports_datasci_finalproject_files/figure-html/unnamed-chunk-3-1.png)<!-- -->

Of the top four Esports teams that have earned the majority of their prize from professional tournaments from League of Legends, the three teams, SK Telecom T1, Invictus Gaming, and Fnatic, have all won the international League of Legends Worlds tournament. League of legends have impacted the massive growth of the largest Esports teams in the world.

## What is League of Legends?

![Map of League of Legends - Summoner's Rift](Summoner's_Rift_Update_Map.png)


But before we can discuss the impact of League of Legends, it is good to know what the praise and large following of the game is about. Created in 2009, League legends is a team multiplayer online battle arena where the two teams made of 5 players where the goal is to defeat the enemies' "nexus" or their base located on opposite sides of the map. The map, called "Summoner's Rift, is split by three lanes lined with three turrets in each lane and two more turrets protecting the nexus for each side of the map. In between each lane is an area known as the jungle where jungle monsters (raptors, krugs, wolves, gromp, golem, blue sentinel, and red brambleback)reside. There is also a river that runs across the map with pits home to the Rift Herald, Baron Nashor, and Elemental Dragons. 

Each team chooses a champion that spawn on the map that have with an assigned role: top lane, mid lane, bot lane, support (also in the bot lane), and jungler. Based of the name of their roles, they will play the game in those repective locations. When the game starts, the lane players (also called laners) meet each other in their lane with a small group of minions that continously respawn and walk from the nexus down their repective lanes, while the jungler traverses through the jungle. In each lane, the laners goal is to kill the minions for earning in game gold and also attempt to kill the opposing enemy laner which also grants them a significant amount more gold. The junglers also earn in game gold by killing the jungler monsters or visiting a lane to kill the enemy. This process of killing minions, monsters, and enemy players goes on as each player accumulates gold in order to purchase specialized items to increase the strength and health of each player's champion. The stronger the champion becomes the higher the chance the team can kill the enemies and push towards their base to destroy the nexus and win the match.

The becomes much more complicated when professional players and teams consider the smallest details, stats, and actions. A small mistake by buying the wrong in game item or walking to the wrong area and getting ambushed by the enemy can turn the game around towards the team that would seem to be losing. But what statistics will majorly determines the likelihood the team will win?

![](esports_datasci_finalproject_files/figure-html/unnamed-chunk-4-1.png)<!-- -->

Before I can answer this question, I will explain what the data is collected on. In multiplayer League of Legends, there are two main gamemodes on Sommoner's Rift: Normal and Ranked. The difference between the two gamemodes is Ranked gives the players a tier from Iron to Challenger where the players can climd the tier ladder by earning "LP" points. another thing to note is when a player quenes up for a game match on the Summoner's Rift map they will spawn on the right side nexus of the left side nexus where right is blue side and left is red side.

The graph above shows the data collected from over 9,800 Diamond ranked games from the Western European server. The focus of this specific analysis for League of Legends shows that among the many variables inside the game over 70% of the games a team wins by non professional players are greatly impacted by the positive gold difference relative to the opposing team where the gold is earned by farming minions and jungle monsters, killing the enemy, and accomplishing the objectives that give gold.

![Ranks from left to right: Iron, Bronze, Silver, Gold, Platinum, Diamond, Master, Grandmaster, Challenger](lol_emblems_and_positions.png)

Other factors that lead to the result of the game that are less related (although paritally involve gold game for the players) are objectives. In the game on Summoner's Rift there are certain objectives to help the team pull ahead to reach the final goal of destroying the nexus.
The following is a general list of objectives that the team can achieve located in the pits around the river of the map:
- Rift Herald: killing this creature gives the player a drop that can be spawned to act as a battering ram against turrents and other enemy structures that will grant gold to the players
- Elemental Dragons: There are four elemental dragons that the players can kill that will grant the entire team a buff in creased in a certain stat based on whcih dragon is slain
- Baron Nashor: A giant serpent-like creature that when killed grants the the player 300 gold on the team. Also gives them power of strengthen the ally minions when the payer is close enough to the minions.
- Elder Dragon: killing the Elder dragon grants the team 250 gold and strongest individual buff to each player that lasts for a short time.

![](esports_datasci_finalproject_files/figure-html/unnamed-chunk-5-1.png)<!-- -->

For each objective that the team achieves from the list above within a match, one objective point is given to the blue/red team. The graph above shows how completing objectives can result in a win. Matches labeled "Expected" means a team's objective score is higher than the other team and the final result is the team with the higher score won. Matches labeled "Undefined" means the objective score for both teams are equal so the result of the match depends on other factors. Matches labeled "Unexpected means a team's objective score is lower than the other team and the final result is the team with the lower score won. Over 60% of the matches in over 9800 Diamond ranked games show that completing objectives

So what does all this data mean for the average League of legends?
In order for you to have the best chance possible to win the game, it is extremely important to farm minions and kill jungle monsters to have the safest path towards earning the most gold without dying by the enemy and winning a game. 

## Professional League of Legends Esports

-talk about how i only selected the top 4 regions
-use the data and explain its meaning
- use the high diamond ranked games data 
- use the pro matches to show the level and difference between diamond and pro player games


```
## `summarise()` regrouping output by 'league' (override with `.groups` argument)
```

![](esports_datasci_finalproject_files/figure-html/unnamed-chunk-6-1.png)<!-- -->

![](esports_datasci_finalproject_files/figure-html/unnamed-chunk-7-1.png)<!-- -->


```
## Warning: Problem with `mutate()` input `t1_elders`.
## i NAs introduced by coercion
## i Input `t1_elders` is `.Primitive("as.double")(t1_elders)`.
```

```
## Warning in mask$eval_all_mutate(dots[[i]]): NAs introduced by coercion
```

```
## Warning: Problem with `mutate()` input `t2_elders`.
## i NAs introduced by coercion
## i Input `t2_elders` is `.Primitive("as.double")(t2_elders)`.
```

```
## Warning in mask$eval_all_mutate(dots[[i]]): NAs introduced by coercion
```

```
## Warning: Problem with `mutate()` input `t1_heralds`.
## i NAs introduced by coercion
## i Input `t1_heralds` is `.Primitive("as.double")(t1_heralds)`.
```

```
## Warning in mask$eval_all_mutate(dots[[i]]): NAs introduced by coercion
```

```
## Warning: Problem with `mutate()` input `t2_heralds`.
## i NAs introduced by coercion
## i Input `t2_heralds` is `.Primitive("as.double")(t2_heralds)`.
```

```
## Warning in mask$eval_all_mutate(dots[[i]]): NAs introduced by coercion
```

```
## Warning: Problem with `mutate()` input `t1_firsttothreetowers`.
## i NAs introduced by coercion
## i Input `t1_firsttothreetowers` is `.Primitive("as.double")(t1_firsttothreetowers)`.
```

```
## Warning in mask$eval_all_mutate(dots[[i]]): NAs introduced by coercion
```

```
## Warning: Problem with `mutate()` input `t2_firsttothreetowers`.
## i NAs introduced by coercion
## i Input `t2_firsttothreetowers` is `.Primitive("as.double")(t2_firsttothreetowers)`.
```

```
## Warning in mask$eval_all_mutate(dots[[i]]): NAs introduced by coercion
```

```
## Warning: Problem with `mutate()` input `t1_inhibitors`.
## i NAs introduced by coercion
## i Input `t1_inhibitors` is `.Primitive("as.double")(t1_inhibitors)`.
```

```
## Warning in mask$eval_all_mutate(dots[[i]]): NAs introduced by coercion
```

```
## Warning: Problem with `mutate()` input `t2_inhibitors`.
## i NAs introduced by coercion
## i Input `t2_inhibitors` is `.Primitive("as.double")(t2_inhibitors)`.
```

```
## Warning in mask$eval_all_mutate(dots[[i]]): NAs introduced by coercion
```

![](esports_datasci_finalproject_files/figure-html/unnamed-chunk-8-1.png)<!-- -->

## Why is this game imapctful to Esports?

- TALK ABOUT TWITCH   


