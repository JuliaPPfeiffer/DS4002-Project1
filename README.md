# DS4002-Project1

## Repository Contents
This repository contains the following contents:
- ***SCRIPTS***: this folder contains all scripts used to clean our data, conduct our analysis, and generate visualizations.
- ***DATA***: this folder contains our initial dataset (nfl_sentiments) that sparked our interest as well as all the data used to complete our project.
- ***OUTPUT***: this folder contains outputs produced from our analysis, such as tables and graphs. This includes all NFL sentiment graphs, such as histograms, bar graphs, and word clouds, which visualize our exploratory analysis.

### Section 1: Software and platform section

***Software Used***:
For this project, we used python as the primary language for conducting our analysis and generating visualizations. Coding was completed through the resourses Google Collab and Visual Studio Code. 

***Packages***:
Packages used include pandas, numpy, TextBlob, stopwords, re, matplotlib, seaborn, and WordCloud.

***Platform***: 
All members of this project used Mac as their platform. 

### Section 2: Documentation Map 
![Project 1 GitHub Outline](https://github.com/user-attachments/assets/14b82b97-7cc9-4875-9b67-483a40855c64)

### Section 3: Reproduction Steps  

#### **Step-by-Step Instructions to Reproduce Results**  

##### **1. Set Up the Environment**  
- Install necessary Python libraries, including pandas, numpy, matplotlib, seaborn, statsmodels, and sklearn.  

##### **2. Load the Dataset**  
- Download the **NFL Twitter Sentiment Analysis dataset** from Kaggle.  
- Ensure the dataset file (CSV) is in the working directory.  
- Load the dataset into a pandas DataFrame.  

##### **3. Preprocess the Data**  
- Remove invalid entries, such as missing team names or incorrect sentiment labels.  
- Convert timestamps to a datetime format for easier filtering.  
- Map sentiment labels to numerical values:  
  - Positive → +1  
  - Neutral → 0  
  - Negative → -1  

##### **4. Aggregate Pre-Game Sentiment**  
- Filter tweets posted up to three days before each team's game.  
- Group the data by team and compute the average sentiment score for each team.  

##### **5. Merge with Game Results**  
- Assign each team a game result label:  
  - **1** if the team won  
  - **0** if the team lost  
- Merge this game result data with the computed average sentiment scores.  

##### **6. Fit Logistic Regression Model**  
- Use logistic regression to analyze the relationship between a team's pre-game sentiment and their game outcome.  
- Train the model using average sentiment scores as the independent variable and game outcomes as the dependent variable.  

##### **7. Statistical Significance Test (Wald Test)**  
- Use the Wald test to determine if fan sentiment has a statistically significant effect on game outcomes.  
- Extract the p-value from the test.  
- If the p-value is less than 0.05, reject the null hypothesis, indicating a significant relationship.  

##### **8. Visualize Findings**  
- Create a histogram to visualize the overall distribution of sentiment scores.  
- Generate bar plots to compare the average sentiment for each team before their game.  

##### **9. Interpretation of Results**  
- If the p-value is below 0.05, conclude that fan sentiment before a game is significantly related to the game’s outcome.  
- If the p-value is above 0.05, conclude that pre-game sentiment does not significantly predict game results. 
