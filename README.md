# March Madness 25 Kaggle Competition
[Kaggle Link](https://www.kaggle.com/competitions/march-machine-learning-mania-2025/overview) 

I, Nick, am working with my long time friend and colleague Ghaith, to predict the march madness tournaments for both the men and women. We are employing feature engineering and model selection processes to develop the best model possible with limited time.

Our feature engineering consists of:  
  -Counting regular season win totals for each time.  
  -Calculating the average game score differential for each team.  
  -Averaging a national ranking for each team (Men only).  
  -Calculating average differences for each of: points, rebounds, steals, turnovers, assists, FG%, 3FG%, FT%, and fouls.

We trained two ensemble learning algorithms and two linear models on the women's side. The Random Forest classifier was chosen for its out of the box performance. A Histogram Gradient Boosting Classifier was chosen for its ability to quickly process large datasets. Logistic Regression was used as a simple alternative. And Scikit Learn's Passive Aggressive Classifier was considered to see how well it aggressively accounted for mistakes.

Each model was trained iteratively over the past 5 seasons of data and assessed using Brier Score and F1_Score. F1_Score was used as our first layer of assessment, to see how frequently and accurately we were correctly predicting games. The competition used Brier Score Loss as its official scoring metric. This both rewards and punishes confidence in the predictions submitted. A 90% prediction scores better than a 55% prediction when correct and worse when wrong.

The competition required predictions on all possible matchups between Division 1 Men's and Women's teams. Those 131k+ predictions can be found in the submission_stage2.csv
