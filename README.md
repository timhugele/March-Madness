# March-Madness

|Name     |  Github   | 
|---------|-----------------|
|Tim Hugele|[Github](https://github.com/timhugele)


### Data Source
* The data for this project was obtained from [Kaggle](https://www.kaggle.com/c/mens-machine-learning-competition-2019).

### Jupyter notebooks
* [Data_Preparation.ipynb](https://github.com/timhugele/March-Madness/blob/master/Data_Preparation.ipynb)
* [Massey_Ordinals.ipynb](https://github.com/timhugele/March-Madness/blob/master/Massey_Ordinals.ipynb)
* [TrueSkill.ipynb](https://github.com/timhugele/March-Madness/blob/master/TrueSkill.ipynb)
* [Game_Location.ipynb](https://github.com/timhugele/March-Madness/blob/master/Game_Location.ipynb)
* [Modeling_Notebook_2.ipynb](https://github.com/timhugele/March-Madness/blob/master/Modeling_Notebook_2.ipynb)

### Project Presentation
* [Canva Slides](https://www.canva.com/design/DAD85iul94o/FQuRIMB4pS5TayYje1qctQ/view?utm_content=DAD85iul94o&utm_campaign=designshare&utm_medium=link&utm_source=sharebutton)


### Problem Summary
* Using the data from Kaggle, and other outside sources, I am attempting to predict the outcomes of NCAA Men's Basketball Tournament 
games. I intend to use this information to be able to place bets on an NCAA Tournament Bracket in future years.
### Metrics
The metrics that I am using for this project are log loss and accuracy. I used both of these metrics because they each provide useful 
information that the other doesn't communicate. The log loss metric is on a scale from 0 to 1, with 0 being perfectly right and 1 being 
perfectly wrong. The log loss is useful because it takes in the probability values that I generated with my model and compares them to 
the outcome that I predicted. For example, I used a value of 1 to indicate that team 1 won a particular game. If I predicted the that the 
probability that team 1 would win to be 0.75, I would get an even better log loss score if I had predicted the probability to be 0.8. 
How confident you are influences the model. However, it doesn't exactly tell you how many predictions were correct, meaning, a probability 
greater than 0.5.

Therefore, I used a second metric, accuracy. Accuracy is simply how many correct predictions I made divided by the total number of games. 
This metric is useful because it is very easy to understand and gives you the most important information. However, I thought that the 
logloss metric would still be useful, because ideally I would like my predictions to have a high degree of confidence.
### Key Takeaways
* Difficult to pick upsets
* Whether a feature is important depends on the model being used. There was quite a bit of difference between the logisitic regression 
model and the XGBoost model.
* Using data from too far into the past harms predictions with some variables more than others. The Massey Ordinals was one set of data 
that tended to hurt the logistic regression model quite a bit. However, the XGBoost model found it to be the most important feature.

### Initial Results
* Best model picks 55 winners correctly, missing 12 for an accuracy of 0.82, with a log loss of 0.41.

### Next Steps
  I would like to try predicting on all college basketball games for the past few years, instead of predicting on season averages dating 
back to 2003. I found that my predictions were getting better when I limited the training data to only the past few years. Therefore, 
this leads me to believe that college basketball changes a bit over time. The reason I didn't do this initially was that I would be 
unable to use some of my best predicting metrics. The data that I have for the Kenpom metrics only has end of year statistics, and 
therefore I would be unable to use them during the regular season. Furthermore, tournament seed was a useful statistic that I wouldn't be 
able to use either. Despite these reasons, I would still like to attempt to model it because it would allow me to have a much larger data 
set, all being data from the recent past.
  
  I would also like to try to use individual player quality as a factor in finding the quality of a team. Doing this would both allow 
  me to try modeling the data in a different way, but it would also allow me to factor in player injuries into my predictions. If a team's 
  star player gets injured before the NCAA tournament my model would probably prove inadequate at predicting that team's results. By 
  rating players individually, I would be able to attempt to estimate the quality of the team without said player be reweighting the 
  contributions of other players.
  
  I would also like to try and obtain information from other sources that I did not have for this project. One dataset that I used, 
  Kenpom data, was provided by a user on Kaggle. However, there is more data on the Kenpom website behind a paywall. I am considering 
  subscribing to the site to try out some of their advanced statistics.
  
  I would also like to try more models and different ways of combining them to see if I can capture the strengths of each one.
  
### Sources for Notebooks
* [Kenpom Data](https://www.kaggle.com/shahules/kenpom-2020)
* [City's Lat, Long, and Elevation](https://www.kaggle.com/c/mens-machine-learning-competition-2018/discussion/50209)
* [TrueSkill](https://www.microsoft.com/en-us/research/project/trueskill-ranking-system/)
* [Kaggle Competition Submission](https://github.com/DaveLorenz/NCAAMarchMadnessNN)
* [Kaggle Competition Submission](https://www.kaggle.com/raddar/paris-madness#Time-to-build-some-models!)
* [TrueSkill](https://www.kaggle.com/zeemeen/ncaa-trueskill-script/execution)
* [Massey Ordinals](https://www.kaggle.com/joseleiva/massey-s-ordinal-s-ordinals)
* [Kaggle Starter Kernel](https://www.kaggle.com/addisonhoward/basic-starter-kernel-ncaa-men-s-dataset-2019)
* [Medium Article](https://medium.com/re-hoop-per-rate/training-a-neural-network-to-fill-out-my-march-madness-bracket-2e5ee562eab1)
* [Toward Data Science Article](https://towardsdatascience.com/machine-learning-madness-predicting-every-ncaa-tournament-matchup-7d9ce7d5fc6d)
