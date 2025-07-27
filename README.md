# Movie Market Evaluation: Analysis for best film type and movie decisions.
![Alt text](premium_photo-1710409625244-e9ed7e98f67b.jpeg)
## Introduction
For this analysis, we will use the folder [zipped Data](https://github.com/Haender-Michael/Movie_market_evaluation/tree/main/zippedData) , which contains datasets from [Box Office](https://www.boxofficemojo.com/), [IMDB](https://www.imdb.com/fr/) ,  [Rotten Tomatoes](https://www.rottentomatoes.com/), [TheMovieDB](https://www.themoviedb.org/), [The Numbers](https://www.the-numbers.com/). These datasets contain comprehensive information about movie genre, production budget, release date, title, film earnings, studio name,ratings, etc.


The goal is to draw meaningful information, identify patterns or trends, and provide actionable insights for decision-making that will help the head of the company's new movie studio decide what types of films to create and make important decisions.
## Dataset overview
For this Analysis we will focus on :
- **tn.movie_budgets.csv** : Contains movie titles, release date, production budget, and ticket sales revenue — both domestic and worldwide.

- **bom.movie_gross.csv** : Includes movie titles, studios, domestic gross, foreign gross, and release year.


- **im.db**: A SQLite database with 8 tables containing information about movie titles, genres, actors, ratings , etc.

## Exploratory Data Analysis (EDA)
For the purpose of this analysis we will take the following steps:
- Data cleaning
- Data Understanding
- Data Analysis
- Summary
- Recommendations
- contact information
## Data cleaning.
In this part we will:
- Create a copy of each Dataset.
- clean each dataset.
  
>  that includes : 
- Handling missing values/outliers.
- Handling data types and format.
  
these steps will ensure that everything run smoothly later during our Analysis.
## Data Understanding:
This section creates the framework for the upcoming analysis by defining the businees context, key questions to answer and the datasets we will use.
### Business Context:
The company is launching a new movie studio and needs information related to creating movies.
The goal is to draw meaningful information, identify patterns or trends, and provide findings for decision making.
The findings will, lastly, be presented as actionable recommendations to the head of the new studio.
### key questions: 
- what studio have the greatest success for foreign gross? ?
- How does budget affects revenue ?
- what movie genres perform the best at the box office ?
- Does using popular actors increase movie's performance ?
## Data Analysis
In this part we will use :
- Visualization
- Correlational Analysis
- Pattern Recognition
- Trend Identification
- Insights and Findings
- hypothesis testing
to answer the above questions.
### What studio have the greatest success for foreign gross?
![Alt text](https://github.com/Haender-Michael/Movie_market_evaluation/blob/4efe08b0d387975c4f37168c05947031ea0b09d8/the%20images/first_image.png)
### How does budget affects revenue ?
![Alt text](https://github.com/Haender-Michael/Movie_market_evaluation/blob/d923961ff2152507a8def53bf78a051eff90f80e/the%20images/second_image.png)
#### Analysis
#####  Correlation (r)
- Domestic Gross (r = 0.686)
  represents a **strong positive correlation**.We can ,therefore, say that  Bigger budgets tend to result in higher domestic revenue. Not perfect, but quite predictive.

- Worldwide Gross (r = 0.748)  
More budget usually means stronger international performance.

#####  Distribution Coefficient (r²)
- Domestic (r² = 0.47)
  ~43 % of variation in domestic gross is explained by the production budget.

- Worldwide (r² = 0.56)
  ~56 % of variation in worldwide gross is explained by the production budget.

That means **budget matters** — but it's **not everything**. The remaining variance could be due to other factors like the movie's genre, its marketing campaign, when it was released, who was in it, or what critics thought of it.

ing campaign, when it was released, who was in it, or what critics thought of it.
### what movie genres perform the best at the box office ?
![Alt text](https://github.com/Haender-Michael/Movie_market_evaluation/blob/d53af21e6477859348cd70a4d9c6187a8b898ac1/the%20images/fourth_image.png)
### Does using popular actors increase movie's performance?

**Does a Famous Actor Guarantee a Better Movie?**  Here’s How We Found Out.
We had a simple question: Do movies with big-name stars get better ratings? To get a real, data-backed answer, we couldn't just rely on gut feelings. We needed a fair and logical way to compare movies. Here’s the step-by-step plan we followed.

**Step 1:** Who is a "Popular Actor"?

First, we needed to define what "popular" means. We started with a list of the top 100 most famous actors from IMDb, a trusted source for movie information. We then checked our own data to see which of these actors had made enough movies for a fair comparison.

**Step 2:** Creating Two Groups for a Fair Comparison

To test our idea, we created two groups of movies:

The "Star Power" Group (The Blue Curve): This group included all the movies from our database that starred one of our famous actors.
The "Other Movies" Group (The Green Curve): This group was a random selection of movies that did not star one of our famous actors.
By creating these two distinct groups, we could make a direct, apples-to-apples comparison of their ratings.
![Alt text](https://github.com/Haender-Michael/Movie_market_evaluation/blob/3a182b1e915fa70604fe0330ce28f681bda9f45c/the%20images/fifth_image.png)
**Step 3:** Looking at the Results - The Distribution Plot

The plot you see is the final result of our analysis. It’s a simple way to see the ratings of both groups at a glance.

The Blue Curve shows the spread of ratings for movies with popular actors.
The Green Curve shows the spread of ratings for movies with other actors.
Think of each curve as a pile of all the movie ratings for that group. The peak of the pile shows the most common rating. The further to the right the pile is, the higher the ratings are in general.

What We Found:

As you can clearly see, the blue curve is shifted to the right of the green one. This isn't a random coincidence. It's a clear visual confirmation that movies in our "Star Power" group consistently earned higher ratings than the movies in the other group.

Our Conclusion:

Based on this evidence, we can say with confidence that casting a popular actor is strongly linked to higher movie ratings. While it's not the only factor for success, star power is a reliable ingredient for a better-received film.

## Summary

> For this analysis, we used datasets from the folder [zipped Data](https://github.com/Haender-Michael/Movie_market_evaluation/tree/main/zippedData)
After cleaning, we aimed to address key questions that the head of the company's new movie studio is likely to have.  
> For each analysis, we found respectively, the following information:  
> - the top 10 studios by Average foreign gross.
Among them the top 5 are : hc,p/dw,bv,grtindia and fox.

> - Bigger budgets tend to result in higher revenue. Not always the case, but quite predictive.
That means budget matters — but it's not everything. other factors like the movie's genre, its marketing campaign, when it was released, who was in it, or what critics thought of it also matters.

## Recommendations: 
The head of the company's new movie Team may want to :

**Prioritize Genres with Proven Success:**

- Our  analysis identified "Comedy, Documentary, Fantasy," "Documentary, Family, Musical," and "History, Sport" as the top three highest-rated genre combinations. The studio should consider producing films that fall into these categories to maximize the potential for critical acclaim and audience satisfaction.
- Explore hybrid genres: The top-rated categories are all combinations of genres. This suggests that audiences appreciate films that blend different elements. The studio should encourage creative projects that cross traditional genre boundaries.

**Use Smart Budgeting and Investment:**

- Invest in bigger budgets ,whenever necessary, for higher returns: The analysis shows a strong positive correlation between production budget and both domestic and worldwide gross. While not a guarantee, a larger budget often translates to higher production quality, better marketing, and ultimately, greater revenue.
- Don't rely solely on budget: While important, the budget isn't the only factor for success. The studio should also focus on other key elements like a strong story, effective marketing, and strategic release timing.

**Leverage Star Power:**

- Cast popular actors: Our Analysis concluded that casting popular actors is likely to lead to higher average movie ratings. The studio should prioritize collaborations with well-known and respected actors to increase a film's appeal and box office potential.

**Emulate Successful Studios:**

- Study the strategies of top-performing studios: The analysis identified the top 10 studios by average foreign gross. The new studio should analyze the types of films these studios produce, their marketing strategies, and their distribution networks to learn from their success.

These recommendations will be of great help to guide the new movie studio towards  making data-driven decisions that will increase its chances of success in the competitive film industry.
## **Contact Information**
- First Name: Haender Michael
- Last Name: Jean Louis
- Email: michaelhaenderjeanlouis@gmail.com
- Phone Number: +509 41 75 0264
- LinkedIn: https://www.linkedin.com/in/michael-haender-jean-louis-4b7320316?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app

For further inquiries, feedback, or collaboration on this analysis, feel free to reach out. I welcome discussions and any contract to work with the head of the company's new movie team.

