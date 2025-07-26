# Movie Market Evaluation: Analysis for best film type and movie decisions.
![Alt text](premium_photo-1710409625244-e9ed7e98f67b.jpeg)
## Introduction
For this analysis, we will use the folder zipped Data , which contains datasets from Box Office, IMDB , Rotten Tomatoes, TheMovieDB, The Numbers. These datasets contain comprehensive information about movie genre, production budget, release date, title, film earnings, studio name,ratings, etc.
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
## Data cleaning.
In this part we will:
- Create a copy of each Dataset.
- clean each dataset.
that includes to
 - drop columns/rows when necessary.
 - modify data type in entries and set Index.
 - fill rows with missing values.
these steps will ensure that everything run smoothly later during our Analysis.
## Data Understanding:
This section creates the framework for the upcoming analysis by defining the businees context, the key questions we will answer and the datasets we will use.
### Business Context:
The company is launching a new movie studio and needs information relative to creating movies
The goal is to draw meaningful information, identify patterns or trends, and provide findings for decision making.
The findings will be presented as actionable recommendations to the head of the new studio.
key questions
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
![Alt text](premium_photo-1710409625244-e9ed7e98f67b.jpeg)
### Analysis
#### Correlation (r)
- Domestic Gross (r = 0.731)
  represents a **strong positive correlation**.We can ,therefore, say that  Bigger budgets tend to result in higher domestic revenue. Not perfect, but quite predictive.
- Worldwide Gross (r = 0.779)  
More budget usually means stronger international performance.
####  Distribution Coefficient (r²)
- Domestic (r² = 0.534)
  ~53% of variation in domestic gross is explained by the production budget.
- Worldwide (r² = 0.607)
  ~61% of variation in worldwide gross is explained by the production budget.
That means **budget matters** — but it's **not everything**. The remaining variance (39–47%) could be due to other factors like the movie's genre, its marketing campaign, when it was released, who was in it, or what critics thought of it.
### what movie genres perform the best at the box office ?
![Alt text](premium_photo-1710409625244-e9ed7e98f67b.jpeg)
### Does using popular actors increase movie's performance?
### Hypothesis Test Plan: Actor Popularity vs Movie Ratings
To evaluate whether casting a popular actor increases a movie’s average rating, we will begin by identifying a list of well-known actors from an external source and verifying their presence in our database. For this, we will use a list of [the top 100 most popular actors from IMDB](https://www.imdb.com/fr/list/ls052283250/?view=compact&sort=list_order%2Casc).
Next, we will create a "popular actor" sample group by isolating all the rated movies these actors have appeared in. We will then create a comparison group by randomly selecting movies featuring other actors.
Finally, we will calculate the mean rating for each of these two independent samples and compare them. We will also construct a 98% confidence interval for the mean rating of the "popular actor" sample.
We will define our hypotheses as follows:
**Null Hypothesis (H₀)**: The presence of a popular actor does not increase a movie's average rating (μ₁ ≤ μ₂).
**Alternative Hypothesis (H₁)**: The presence of a popular actor leads to a higher average rating (μ₁ > μ₂).
to test these hypotheses, we will perform a one-tailed t-test for independent means. We will calculate the t-statistic and the critical value (which will be determined by our chosen significance level and the degrees of freedom).
If our calculated t-statistic exceeds the critical value, we will reject the null hypothesis. This would allow us to conclude that featuring a popular actor is statistically associated with higher movie ratings.
**NB**:
- μ₁ (mu 1) represents the mean average rating of the population of all movies featuring a popular actor.
- μ₂ (mu 2) represents the mean average rating of the population of all movies that do not feature a popular actor.
### Analysis of the Hypothesis Test Results
The results from our independent t-test give us a clear, data-driven answer to our question about the impact of popular actors on movie ratings.
* **T-statistic: 3.547**
  * This positive and relatively high value indicates that the average rating for movies with popular actors is significantly higher than the average rating for movies with other actors. It tells us that the difference between the two groups is almost 3.6 times the size of the standard error.
* **P-value: 0.0003279**
  * This is the most crucial result. The p-value represents the probability that we would see a difference this large (or larger) between the two groups purely by random chance, assuming the null hypothesis (that there's no difference) is true.
  * A p-value of 0.0003279 is very small (less than 1%).
#### **Conclusion**
Since our p-value (0.0003279) is much smaller than our chosen significance level (**alpha = 0.02**), we **reject the null hypothesis**.
This provides strong statistical evidence to support our alternative hypothesis. We can conclude with high confidence that **casting a popular actor is associated with a statistically significant increase in a movie's average rating.** The result is not likely due to random statistical noise.
## Summary
For this analysis, we used datasets from the folder zipped Data After cleaning, we aimed to address key questions that the head of the company's new movie studio is likely to have.
For each analysis, we found respectively, the following information:
- the top 10 studios by Average foreign gross. Among them the top 5 are : hc,p/dw,bv,grtindia and fox.
- Bigger budgets tend to result in higher revenue. Not always the case, but quite predictive. That means budget matters — but it's not everything. other factors like the movie's genre, its marketing campaign, when it was released, who was in it, or what critics thought of it also matters.
- the 10 top highest-rated genre combinations. Among them the top three are : "comedy,documentary,fantasy"," Documentary,family,musical ","history sport".
- The presence of a popular actor leads to a higher average rating
## Recommendations
The head of the company's new movie Team may want to :

**Prioritize Genres with Proven Success:**

- Our analysis identified "Comedy, Documentary, Fantasy," "Documentary, Family, Musical," and "History, Sport" as the top three highest-rated genre combinations. The studio should consider producing films that fall into these categories to maximize the potential for critical acclaim and audience satisfaction.
- Explore hybrid genres: The top-rated categories are all combinations of genres. This suggests that audiences appreciate films that blend different elements. The studio should encourage creative projects that cross traditional genre boundaries.
**Use Smart Budgeting and Investment:**
- Invest in bigger budgets ,whenever necessary, for higher returns: The analysis shows a strong positive correlation between production budget and both domestic and worldwide gross. While not a guarantee, a larger budget often translates to higher production quality, better marketing, and ultimately, greater revenue.
- Don't rely solely on budget: While important, the budget isn't the only factor for success. The studio should also focus on other key elements like a strong story, effective marketing, and strategic release timing.
**Leverage Star Power:**

- Cast popular actors: Our Analysis concluded that casting popular actors can lead to higher average movie ratings. The studio should prioritize collaborations with well-known and respected actors to increase a film's appeal and box office potential.
- Balance established and emerging talent: While popular actors are a safe bet, the studio should also invest in up-and-coming talent to build long-term relationships and discover the next generation of stars.
**Emulate Successful Studios:**
- Study the strategies of top-performing studios: The analysis identified the top 10 studios by average foreign gross. The new studio should analyze the types of films these studios produce, their marketing strategies, and their distribution networks to learn from their success.
  
These recommendations will be of great help to guide the new movie studio towards making data-driven decisions that will increase its chances of success in the competitive film industry.
## **Contact Information**
- First Name: Haender Michael
- Last Name: Jean Louis
- Email: michaelhaenderjeanlouis@gmail.com
- Phone Number: +509 41 75 0264
- LinkedIn: https://www.linkedin.com/in/michael-haender-jean-louis-4b7320316?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app
- For further inquiries, feedback, or collaboration on this analysis, feel free to reach out. I welcome discussions and any contract to work with the head of the company's new movie team.

