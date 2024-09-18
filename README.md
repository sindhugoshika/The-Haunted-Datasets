# project_01

Project 1 repo for INFO 526 - Fall 2024.

#### Disclosure:
Derived from the original course by Mine Çetinkaya-Rundel @ Duke University

Haunted Places in the United States
Halloween is coming soon, so we're exploring a spooky dataset: a compilation of Haunted Places in the United States. The dataset was compiled by Tim Renner, using The Shadowlands Haunted Places Index, and shared on data.world.

We're also using this dataset as a reminder that several R packages for spatial data are heading to the graveyard next week. Don't be tricked by their demise!

The Data
# Option 1: tidytuesdayR package 
## install.packages("tidytuesdayR")

tuesdata <- tidytuesdayR::tt_load('2023-10-10')
## OR
tuesdata <- tidytuesdayR::tt_load(2023, week = 41)

haunted_places <- tuesdata$haunted_places

# Option 2: Read directly from GitHub

haunted_places <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-10-10/haunted_places.csv')

Haunted Places Data Exploration

Welcome to the Haunted Places Data Exploration project! In this project, a fascinating dataset of haunted locations across the United States is provided for exploration. Whether experience in data science is present or just beginning, an opportunity is offered to delve into interesting relationships within the data.

How to Get Involved

The dataset is encouraged to be explored for intriguing patterns or insights. It should be remembered that while correlations can be observed, conclusions about causation should not be drawn. Various external factors may influence the data, many of which are not captured in this dataset. This opportunity is presented to practice data cleaning, visualization, and analysis skills while thinking critically about the underlying factors that could influence these relationships.

Visualizations, predictive models, Shiny applications, or any other data-related projects can be created using R or a preferred programming language. Once work is completed, results and code should be shared on social media using the hashtag #TidyTuesday. The community would love to see what is created!

Dataset Overview

The dataset haunted_places.csv includes several columns, each providing insights into haunted locations. A breakdown of the data is presented below:

Column Name	Type	Description
city	character	The city where the haunted location is found.
country	character	The country of the location (always "United States").
description	character	A description of the haunted place, varying in detail.
location	character	The name or title of the haunted site.
state	character	The US state where the site is located.
state_abbrev	character	The two-letter abbreviation for the state.
longitude	double	The longitude coordinate of the haunted place.
latitude	double	The latitude coordinate of the haunted place.
city_longitude	double	The longitude of the city center.
city_latitude	double	The latitude of the city center.
Data Source
The dataset was downloaded from Data World.


Cleaning Script

Data downloaded directly from https://query.data.world/s/glc736mqf4dxrqe6nbsamblqndemb6?dws=00000