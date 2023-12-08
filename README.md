# ![A clapperboard, film reel, and popcorn with a blue wood background](https://github.com/RigatN/Winning_Movie_Genres_for_New_Studios/blob/main/Images/01Film.png)

# Cinematic Returns: Unveiling the Art and Science of Movie Profitability
By [JD](mailto:jediaeldsr@gmail.com), [Katie](mailto:kpegg916@gmail.com), & [Rigat](mailto:rigatanirayo@gmail.com)

## Overview

Our company is entering a new market and has created a movie studio. This analysis uses statistical methods to provide actionable insights into movie profitability and identify peak times for movie releases.

## Business Understanding

The film industry has almost always been considered to be unpredictable and volatile. Despite this, certain production companies thrive within this market. This market analysis aims to identify some underlying factors that may contribute to a movie's box office success. We are aiming to answer these questions:
- Which genre of movies have the highest ROI?
- What is the best time to release films for maximum profitability?
- Is there a direct positive relationship between the amount spent on a movie and the profitability?
## Data Understanding

Movie data from Box Office Mojo, IMDB, The Movie Database, and The Numbers was used and analyzed. The data files provided titles, release dates, genres, length of movies, budgets, revenue, along with a multitude of other attributes involved in movies. The movies used for analysis were released between 1967 and 2016 with a total number around 1100 movies.
## Data Preparation

The dataset underwent a review, involving cleaning, consolidation of databases and tables, and subsequent refinement to ensure a targeted focus on pertinent elements for the analysis. To consolidate the databases & tables, inner joins were used. Duplicates were removed by title, and then, because most movies have two or more genres, '.explode' was used on the dataframe in order to have one row per genre per movie. This allowed us to subset by the horror genre first.
## Analysis and Recommendations

#### ROI
Return on investment, or ROI, was explored as it seemed the most logical metric to analyze to assess the financial performance of the initial genre.

# ![graph showing mean ROI, highlighting horror as the genre with highest ROI](https://github.com/RigatN/Winning_Movie_Genres_for_New_Studios/blob/main/Images/Mean_ROI_by_genres.png)
Horror came out on top and was statistically significantly different. We further corroborated this metric with the use of an ANOVA test. First, we set up our Null and Alternate Hypotheses, which are as follows: 

- H<sub>0</sub>: There is no significant difference between the average ROI among all of the varying genres in our data set.
- H<sub>a</sub>: There is a significant difference between the average ROI of films produced in the Horror Genre, and the average ROIs of movies made in other genres.

We then found the average ROIs across all genres in our data set. We chose a significance level of 0.05. The p-value we arrived at was 4.678. Since this value was lower than 0.05 we were able to reject our null hypothesis and accept the alternative hypothesis. 

#### Mean Profit per Month
Since horror movies tend to have the highest ROI, we looked at the mean profit per month for the first genre we will focus on.

# ![graph mean profit per month for horror movies]([https://github.com/RigatN/Winning_Movie_Genres_for_New_Studios/blob/main/Images/Mean_Profit_Horror.jpg](https://github.com/RigatN/Winning_Movie_Genres_for_New_Studios/blob/main/Images/horror_movies_mean_profit_per_month.png))
This graph shows that typically horror films made the most when released in August or September, not October like we had originally surmised. Perhaps movie buffs are looking for some motivation before Halloween.

#### Budget vs. Worldwide Gross
We also attempted to find a correlation between worldwide gross and production budget. Our logic behind this was to see if the amount of money spent on production had any relationship with worldwide gross income.

# ![linear regression between production budget and worldwide profit](https://github.com/RigatN/Winning_Movie_Genres_for_New_Studios/blob/main/Images/Linear_regression_plot_R2.png)
In the correlation matrix we set up between the two variables, the correlation coefficient between these two variables was .74. This indicated a strong to moderate relationship between the two variables and was further corroborated by the R2 value of 0.61 and accounts for the variation around the regression line.

From the variation around the line, it is hard to say definitively that the more a company spends on production, the greater the worldwide gross income. To find a production budget range that made a decent worldwide gross income, we looked at the lower 25th percentile in spending. To generate a spending range leading to the best projected worldwide gross income. 

## Conclusion and Next Steps

- First focus will be on creating & releasing horror films, due to typically low production costs and relatively high ROI
- Action would be the next genre to focus on, since action tends to have the highest mean profit per month

# ![bar graph showing mean profit per month for action movies](https://github.com/RigatN/Winning_Movie_Genres_for_New_Studios/blob/main/Images/neax_step_action_movies_mean_profit_per_month.png)

- Maximize the profitability: May or June would be the ideal months for release: potentially May and June have the highest mean profits since people are on vacation or students are no longer in school so they have more time for leisure activities. November & December could be another good time to release the movie as well, since people may be on vacation or watch more movies around the holidays
- It should be recognized that action films can entail higher risks, stemming from the elevated budget invested in the production
- Production budget: keep the budget somewhere in between $3-9.5M range
- Further analysis on which genres will perform well in the foreign market

## For More Information

Please see the full analysis in the [cleaning](https://github.com/RigatN/Winning_Movie_Genres_for_New_Studios/blob/main/Cleaning_and_Exploring_Data.ipynb) and [analysis](https://github.com/RigatN/Winning_Movie_Genres_for_New_Studios/blob/main/Analysis_and_Stats.ipynb) or the [presentation]().

## Repo Structure

```
├── data
├── images
├── Notebooks
├── Cleaning_and_Exploring.ipynb
├── Analysis_and_Stats.ipynb
├── README.md
├── Movie Profitability Analysis.pdf
└── Final.ipynb
```
