<font size="12"> Reddit Classification Project</font>
-----------------------------------------------------------------------------------------------------------------------------


<font size="8"> Problem Statement</font>

The underlying task of the project is to stratify the posts from the subreddits:
particle physics and astrophysics, to atleast a sixty five percent accuracy. In doing so, 
identifying the significant constituents that contributed to the efficacy of the predictive models. 

----------------------------------------------------------------------------------------------------------------------------
Table of Contents 


[Data Aquisition](https://git.generalassemb.ly/shiffraw/Project-3-/blob/master/Data-Acquisition.ipynb)



[Data Cleaning](https://git.generalassemb.ly/shiffraw/Project-3-/blob/master/DataCleaning.ipynb)



[Explaratory Data Analysis](https://git.generalassemb.ly/shiffraw/Project-3-/blob/master/EDA.ipynb)



[Modeling](https://git.generalassemb.ly/shiffraw/Project-3-/blob/master/Modeling.ipynb)



[Presentation Slides](https://git.generalassemb.ly/shiffraw/Project-3-/blob/master/project%203%20.pptx)



[Particle Physics Data](https://www.reddit.com/r/ParticlePhysics/)



[Astrophysics Data](https://www.reddit.com/r/astrophysics/)

---------------------------------------------------------------------------------------------------------------------------

<font size="8"> Subreddits</font>
The predictive model stratified posts from two subreddits: r/particle physics and r/astrophysics

<font size="6"> Particle Physics</font>


| Particle Physics |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Members          | 13.6 thousand                                                                  |
| Date of Creation | August 6th 2009                                                                |
| Summary          | Subreddit dedicated to the discussion and discourse of Particle Physics topics |


<font size="6"> Astrophysics</font>


| Astrophysics     |                                                                            |
|------------------|----------------------------------------------------------------------------|
| Members          | 26.2 thousand                                                              |
| Date of Creation | January 16th 2010                                                          |
| Summary          | Subreddit dedicated to the discussion and discourse of Astrophysics topics |



<font size="4"> Astrophysics</font>
Dataframe consisted of 1000 rows. The information that were acquired are:  title, selftext, timestamp, permalink and id. These were extracted by mechanism of the  Pushshift's API. The Title and selftext were combined for the predictive model. 

------------------------------------------------------------------------------------------------------------------------------

<font size="6"> Predictive Models Utilized </font>


| Estimator                    | Transfomer         |
|------------------------------|--------------------|
| Logistic Regression          | Count Vectorizer   |
| Random forest                | Tfidf Vectorizer   |
| Multinomial Bayes            | Wordnet Lemmatizer |
| Stochastic Gradient Descent  | Porter Stemmer     |

------------------------------------------------------------------------------------------------------------------------------

<font size="6"> Conclusion </font>

The best model that most accurately stratified posts from the two subreddits was logistic regression coupled with 
the Tfidf vectorizer.  The accuracy score was 82 %.  The challenge of this project was choosing two subbreddits 
that were similar and limiting the model to only incorporate 500 posts for each subreddit.  The n-grams that optimized
the accuracy was (1,2).  The regular expression tokenizer split the text in terms of both words and floats, since 
different constants are relative for both particle physic and astrophysics.  




