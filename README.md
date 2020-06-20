

# KICKSTARTER:
### Question: 
"Growing company profits by focusing resources on campaigns likely to successfully complete."

Kickstarter takes:
 - 5% from successful campaigns
 - 0% from unsuccessful campaigns

Kickstarter has limited resources for marketing and guidance.  Therefore, to maximize revenue, a predictive model can assist the marketing department in capitalizing on a campaign’s maximum potential.


### Hypothesis: 
Out of our variables I believe 'country', 'launched', and 'main_category' will have the most predictive power. While 'country' is unlikely going to be an option for an individual to manipulate, the other two variables have potential to be altered.
After this analysis we should be able to identify key variables we can manipulate to further increase the odds of success.  Variables that we cannot manipulate, such as country of origin, we can provide clients with advice on setting achievable goals.  It is suspected the largest impact will be “country”, the “main_category” of the campaign, and the “date launched”.  While “country” is not able to be manipulated, the campaign's “launch date” and a product's “main_category” can be discussed with the clients beforehand.

I will be looking into potential actionable insights that can assist users in designing productive campaigns.


## Data Cleaning:
- The data was collected from Kaggle and already in a pandas readable format.
- Dropped redundant columns as measured by correlation
- Convert non-numerical data to numerical (dummy variable)
- Convert date/time entries into pandas' date/time feature
- Create the feature "elapsed" by determining time used from start to completion

Percentage of un/successful campaigns compared to each main category
*insert countplot of successful to main category*
- Bar lengths represent the quantity of projects within that category. 
- "Music" is the largest and safest ratio of successful to unsuccessful campaigns.



The top 3 categories where we can find most of the revenue are "Games", "Design", "Technology". 
*insert onlysuccessful.groupby main category usd pledged real*
Above chart is of only successful campaigns, how much revenue each category brought in.


Distribution of pledged U.S. dollars within successful campaigns.Heavy successful campaigns at one end of the spectrum is not the norm.Most campaigns fall below $10,000.
*insert distplot(PledgedRealWin)*


Money makers: The top 3 categories where we can find most of the revenue are "Technology", "Design", "Games".
*barplot x=onlysuccessful usd pledged real  y=onlysuccessful main category*

Number of backers/pledgers distributed between main categories.This shows how a strong correlation between quantity of backers and monies raised instead of a select few high value donations.
*barplot onlysuccessful backers onlysuccessful main category*


### What does this all mean?
- We can predict the success of a campaign utilizing a linear regression model.
- The model can predict the funds that will be collected for a successful campaign.

Utilizing a linear regression model: 85% accuracy
