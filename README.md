# S1-NBAplayers-

## Objectives of the project

- Understanding how to query an API to create a dataset with Python and Pandas
- Learning how to cleanup a dataset and generate new fields from calculated data
- Storing the created dataset in a serialized manner
- Generating statistics about the data
- Visualizing data

## Creating my dataset

I want to create a single pandas dataframe with information about all active players in the current NBA season. The dataset needs to have the following structure:

#### Personal Information
  - player_id (int) (INDEX)
  - player_name (str)
  - team_name (str)
  - position (str)
  - height (int) (in centimeters)
  - weight (float) (in kilograms)
  - country of origin (str)
  - date_of_birth (datetime)
  - age (str) (years and months)
  - years_of_experience (int) (years since entering the league)
  - Draft position (int)
  
#### Player career statistics
  - games played (int)
  - minutes per game (float)
  - points per game (float)
  - rebounds per game (float)
  - assists per game (float)
  - steals per game (float)
  - blocks per game (float)
  
#### Misc
  - salary in dollars (int) (contract value for this season only)

## Using the API

https://github.com/swar/nba_api

This is a Python library that can be used to obtain data from stats.nba.com, it provides a set of methods that abstracts you from making the HTTP calls, but directly makes calls to the NBA stats page and parses the results.


