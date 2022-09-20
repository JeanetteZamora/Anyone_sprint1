# Sprint1
-NBAplayers-

## Objectives of the project

- Understanding how to query an API to create a dataset with Python and Pandas
- Learning how to cleanup a dataset and generate new fields from calculated data
- Storing the created dataset in a serialized manner
- Generating statistics about the data
- Visualizing data

## Install

You can use `Docker` to easily install all the needed packages and libraries:

```bash
$ docker build -t sprint1 -f Dockerfile .
```

### Run Docker 

```bash
$ docker run --rm -it -p 8888:8888 -v $(pwd):/home/app/src sprint1 bash 
```

## Run Project

It doesn't matter if you are inside or outside a Docker container, in order to execute the project you need to launch a Jupyter notebook server running:

```bash
$ jupyter notebook --ip 0.0.0.0 --port 8888 --allow-root
```

Then, inside the file `AnyoneAI_Project1.ipynb`, you can see the project statement, description and also which parts of the code you must complete in order to solve it.

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


