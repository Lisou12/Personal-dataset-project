# Study of participation in the 2024 legislative elections
This project is on the voting data of the last French legislative elections, in 2024. 

# Motivation
The political situation in France is currently characterized by instability and uncertainty, marked by the persistent risk of National Assembly dissolution and the subsequent necessity of new legislative elections.
Therefore, I choose to analyze the data of the previous egislative election of 2024. This projct adresses two core questions: 
- What was the overall voter turnout, and how does this rate vary across different departments?
- To what extent are the rates of specific voting behaviors independent of the absolute size of the electoral body across all departments? 

# Data Process
This data comes from the website data.gouv.fr. 
Before conducting any analysis, I needed to clean the dataset because every variables representing proportions were stored as character strings instead of numerical values. These values also contained formatting elements like commas and percentage symbols, which prevented them from being interpreted as numbers. To make the data usable for statistical analysis, I replaced commas with decimal points and removed the percentage signs, and then converted the cleaned values into numeric format.

# Visualizations: 
This first visualization is an histogram representing the proportions of blank, invalid, and valid votes, as well as abstentions, among registered voters in each department of the Paris region. The departments are ranked in descending order of the number of registered voters to determine if there is a trend between the number of registered voters and the proportions of each type of vote.
Unfortunately, we can not observed any trend in this visualization meaning the number of registered voters does not impact the proportions of each type of vote.

<img width="1906" height="965" alt="image" src="https://github.com/user-attachments/assets/a1e39ab1-46b9-40d4-8f4a-208e1a67147e" />


To verify what I observed in the Parisian region: the number of voters does not impact the proportion of each type of vote, I extended the analysis to the full national datset to verify whether this pattern holds. To do so, I created a scatter plot comparing the number of voters to the proportion of valid votes. 
The visualization shows that the percentage of valid votes remains relatively stable regardless of the size of the electorate. This suggests that the number of registered voters does not have a notable influence on voting behavior in terms of valid participation.

<img width="700" height="432" alt="image" src="https://github.com/user-attachments/assets/57614df6-b75e-4a49-9020-a28d6b929754" />


To further explore the relationship between electoral participation variables, I created a scatterplot matrix comparing registered voters, actual voters, and valid votes. The strong positive linear patterns observed across all pairwise combinations indicate that these variables are highly correlated with one another. As a result, applying a multiple regression model with these variables as predictors would not be appropriate, since their strong interdependence would lead to multicollinearity issues. 

<img width="700" height="432" alt="image" src="https://github.com/user-attachments/assets/313bdf5e-8468-4a3c-b5b6-f4f6fa00698d" />


To adress the strong multocollinearity among the previous variables, I shifted to proportional variables. The objective was to see if using proportions would remove the strong linear dependence observed previously. However, the resulting scatterplot matrix shows that the strong positive linear patterns are no longer present. Instead, the plots display a general lack of clear correlation between the proportional variables. In conclusion, the types of votes, as proportions, tend to vary independently of the electorate's size. 

<img width="700" height="432" alt="image" src="https://github.com/user-attachments/assets/af196147-aa4e-45e4-b13b-c98b0be9f4ab" />



# Analysis: 
I choose to focus my analysis on the number of voters per department. I generated a boxplot that revealed several outliers. These extreme values were removed using the Interquartile Range method, and 5 outliers were excluded from a new dataset. I choose not to remove the outliers from the original dataset because I am mostly using the proportions of type of vote in this project. 
Following this cleaning step, I calculated the basic descriptive statistics with the function summary(). We can observed a minimum of 2,807 voters, the 1st Quartile at 126,954, a median of 234,442 voters, a mean of 275,364 voters, the 3rd Quartile at 377,312, and a maximum of 766,963 voters.

<img width="949" height="416" alt="image" src="https://github.com/user-attachments/assets/1f24ba8a-0779-4beb-be45-e65a4cf47d40" />

<img width="284" height="42" alt="image" src="https://github.com/user-attachments/assets/aa3c83dc-092e-4267-aab1-fbc250d323b5" />
