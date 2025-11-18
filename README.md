# Personal-dataset-project
This project is on the last French legislative elections, in 2024. 
This data comes from the website data.gouv.fr. 
Te subject of voting in legislative elections is relevant because the French political situation is currently unstable, and the probability of the National Assembly being dissolved, which would lead to new legislative elections, is high.

# study of participation in the 2024 legislative elections

Questions: 
- What is the voter turnout for the 2024 French legislative elections? 
- Does the type of vote vary by department based on the number of people registered? 

# Visualizations: 
Histogram representing the proportions of blank, invalid, and valid votes, as well as abstentions, among registered voters in each department of the Paris region. The departments are ranked in descending order of the number of registered voters to determine if there is a trend between the number of registered voters and the proportions of each type of vote.
Unfortunately, we can not observed any trend in this visualization meaning the number of registered voters does not impact the proportions of each type of vote.

<img width="1906" height="965" alt="image" src="https://github.com/user-attachments/assets/a1e39ab1-46b9-40d4-8f4a-208e1a67147e" />

# Analysis: 

I choose to focus my analysis on the number of voters per department. I generated a boxplot that revealed several outliers. These extreme values were removed using the Interquartile Range method, and 5 outliers were excluded from a new dataset. I choose not to remove the outliers from the original dataset because I am mostly using the proportions of type of vote in this project. 
Following this cleaning step, I calculated the basic descriptive statistics with the function summary(). 

<img width="949" height="416" alt="image" src="https://github.com/user-attachments/assets/1f24ba8a-0779-4beb-be45-e65a4cf47d40" />

<img width="284" height="42" alt="image" src="https://github.com/user-attachments/assets/aa3c83dc-092e-4267-aab1-fbc250d323b5" />
