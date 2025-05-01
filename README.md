# Teamfight Tactics Champion Tier Prediction (mini ML project)

### Goal
Predict whether a champion is "strong" or "not strong" in TFT (Teamfight Tactics) using basic stats. 

### What I did
- Collected champion data (health, damage, cost, etc.) through HTML parsing.
- Standardised all the data into numbers.
- Moved the scraped data into a CSV and then made it into a Pandas dataframe.
- Created labels 1 for "strong" and 0 for "not strong"
- Trained logistic regression and random forest models using the Scikit-learn library.
- Explored the effects of the train/test split on a small dataset.

### Important Insights
The model performed poorly (~50%) accuracy because:
- The dataset is very small (60 samples), as only data from the current version of TFT is easily accessible.
- Champion tiers depend on more than just the base stats, e.g., the synergies with other champions and the strength of the items that the champion needs.
- Typically the labels for the tiers go from S -> A -> B -> C -> D, with S-tier being the strongest. However due to the lack of data, I found that it would be better to make this a binary classification problem,
  with champions from S and A tier being considered "strong", so a label of 1, and champions in B, C, and D tier being "not strong", a label of 0.


### What I'd do next
- Possibly scrape more data from older TFT sets (versions).
- Look to use SMOTE (Synthetic Minority Oversampling Technique) in order to balance the dataset more.
  
  
  

