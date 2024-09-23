# Haunted Places in the United States

Project 1 repo for INFO 526 - Fall 2024.

#### Disclosure:
Derived from the original course by Mine Çetinkaya-Rundel @ Duke University

Haunted Places in the United States
Halloween is coming soon, so we're exploring a spooky dataset: a compilation of Haunted Places in the United States. The dataset was compiled by Tim Renner, using The Shadowlands Haunted Places Index, and shared on data.world.

We're also using this dataset as a reminder that several R packages for spatial data are heading to the graveyard next week. Don't be tricked by their demise!

## The Data

```{r}
# Option 1: tidytuesdayR package 
## install.packages("tidytuesdayR")

tuesdata <- tidytuesdayR::tt_load('2023-10-10')
## OR
tuesdata <- tidytuesdayR::tt_load(2023, week = 41)

haunted_places <- tuesdata$haunted_places

# Option 2: Read directly from GitHub

haunted_places <- readr::read_csv('https://raw.githubusercontent.com/rfordatascience/tidytuesday/master/data/2023/2023-10-10/haunted_places.csv')

```

Haunted Places Data Exploration

Welcome to the Haunted Places Data Exploration project! In this project, a fascinating dataset of haunted locations across the United States is provided for exploration. Whether experience in data science is present or just beginning, an opportunity is offered to delve into interesting relationships within the data.

How to Get Involved

The dataset is encouraged to be explored for intriguing patterns or insights. It should be remembered that while correlations can be observed, conclusions about causation should not be drawn. Various external factors may influence the data, many of which are not captured in this dataset. This opportunity is presented to practice data cleaning, visualization, and analysis skills while thinking critically about the underlying factors that could influence these relationships.

Visualizations, predictive models, Shiny applications, or any other data-related projects can be created using R or a preferred programming language. Once work is completed, results and code should be shared on social media using the hashtag #TidyTuesday. The community would love to see what is created!

The dataset haunted_places.csv includes several columns, each providing insights into haunted locations. A breakdown of the data is presented below:

### Dataset Overview

The dataset [haunted_places.csv](https://query.data.world/s/glc736mqf4dxrqe6nbsamblqndemb6?dws=00000) includes several columns, each providing insights into haunted locations. A breakdown of the data is presented below:


|variable       |class     |description    |
|:--------------|:---------|:--------------|
|city           |character |The city where the place is located. |
|country        |character |The country where the place is located (always "United States") |
|description    |character |A text description of the place. The amount of detail in these descriptions is highly variable. |
|location       |character |A title for the haunted place. |
|state          |character |The US state where the place is located. |
|state_abbrev   |character |The two-letter abbreviation for the state. |
|longitude      |double    |Longitude of the place. |
|latitude       |double    |Latitude of the place. |
|city_longitude |double    |Longitude of the city center. |
|city_latitude  |double    |Latitude of the city center. |


**Data Source** - The dataset was downloaded from Data World.


Cleaning Script

Data downloaded directly from https://query.data.world/s/glc736mqf4dxrqe6nbsamblqndemb6?dws=00000
