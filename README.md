# Kings of Machine Learning

In January 2018, I participated in the "Kings of Machine Learning" hackathon hosted online by the D.E. Shaw Group on Analytics Vidhya. Out of the 1503 participants, my teammate and I (Team "Serendipity") ranked 81st on the Private Leaderboard. In this repository, you'll find details on how I've applied data preprocessing/feature engineering and dimension reducing techniques to kda_ratio for the popular online game Dota2. Following are the information regarding the competition (https://datahack.analyticsvidhya.com/contest/kings-of-machine-learning/).

## Problem Statement 

Dota2 is a free-to-play multiplayer online battle arena (MOBA) video game. Dota 2 is played in matches between two teams of five players, with each team occupying and defending their own separate base on the map. Each of the ten players independentlycontrols a powerful character, known as a "hero" (which they choose at the start of the match), who all have unique abilities and differing styles of play. During a match, players collect experience points and items for their heroes to successful battle with the opposing team's heroes, who attempt to do the same to them. A team wins by being the first to destroy a large structure located in the opposing team's base, called the "Ancient". 
You’re given dataset of professional Dota players and their most frequent 10 heroes. The data also includes details about the heros (Kind of Hero (nuker, initiator and so on), their base attack, strength, movement speed). Here both train and test dataset is divided into two dataset(train9.csv & train1.csv and test9.csv & test1.csv).
 
train9.csv and train1.csv contain the user performance for their most frequent 9 heroes and 10th hero respectively. Both train9.csv and train1.csv have below fields.

## Input Variables 

### Train 9 & Train 1

1. user_id - the id of the user
2. hero_id - The id of the hero the player played with
3. Id - unique id 
4. num_games - The number of games the player played with that hero
5. num_wins - Number of games the player won with this particular hero
6. kda_ratio (target) - ((Kills + Assists)*1000/Deaths) 
Ratio: where kill, assists and deaths are average values per match for that hero

### Test 9 

1. user_id - the id of the user
2. hero_id - The id of the hero the player played with
3. Id - unique id 
4. num_games - The number of games the player played with that hero

### Hero_data

1. hero_id - The id of the hero the player played with
2. primary_attr - A string denoting what the primary attribute of the hero is
 (int- initiator, agi- agility, str- strength and so on)
3. attack_type - String, :”Melee“ or “Ranged”
4. Roles - An array of strings which have roles of heroes
 (eg Support, Disabler, Nuker, etc.)
5. base_health - The basic health the hero starts with
6. base_health_regen,base_mana,base_mana_regen,
base_armor,base_magic_restistance,
base_attack_min,base_attack_max,base_strength,
base_agility,base_intelligence,strength_gain,agility_gain,intelligence_gain,
attack_range,projectile_speed,attack_rate,move_speed,turn_rate - These are the basic stats the heroes start with 
(some remain same throughout the game)

## Evaluation Metric

The predictions will be evaluated on RMSE.
The public private split is 40:60





