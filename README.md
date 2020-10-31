# Predict Customer reponse of bank marketing campaign using CatBoost

Customer propensity predictive models are one of the most common preditive models in Data mining for Customer insights. It is a very powerful tool to predict Customer responses as well as Customer response probabilities for certain Customer engagement activities, like Marketing Campaigns, based on labeled historical data using features like Customer demographics, Customer behaviours, and Customer engagement stats etc. Then the predicted Customer response probability can be used to design marketing campaigns so as to improve marketing campaign effectiveness and increase ROI. Moreover, the relationships between selected features and target Customer response identified from the predictive analysis also have great business value. The insights of these relationships can be used to gain deep understanding of Customers and enable business to better serve Customers through offerings.

# Data

The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be (or not) subscribed.
This open bank marketing campaign dataset can be downloaded from [UCI data repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing#). The full dataset was described and analyzed in [[Moro et al., 2011]](https://www.researchgate.net/publication/236231158_Using_Data_Mining_for_Bank_Direct_Marketing_An_Application_of_the_CRISP-DM_Methodology). 
This banking dataset has variables below.
- Bank client data:
	1. **age** (numeric)
	2. **job** : type of job (categorical) 
	3. **marital** : marital status (categorical)
	4. **education** (categorical)
	5. **default**: has credit in default? (binary: "yes","no")
	6. **balance**: average yearly balance, in euros (numeric) 
	7. **housing**: has housing loan? (binary: "yes","no")
	8. **loan**: has personal loan? (binary: "yes","no")
- Related with the last contact of the current campaign:
	9. **contact**: contact communication type (categorical) 
	10. **day**: last contact day of the month (numeric)
	11. **month**: last contact month of year (categorical)
	12. **duration**: last contact duration, in seconds (numeric)
- Other attributes:
	13. **campaign**: number of contacts performed during this campaign and for this client (numeric, includes last contact)
	14. **pdays**: number of days that passed by after the client was last contacted from a previous campaign (numeric, -1 means client was not previously contacted)
	15. **previous**: number of contacts performed before this campaign and for this client (numeric)
	16. **poutcome**: outcome of the previous marketing campaign (categorical)
- Target variable:
	17. **y**: has the client subscribed a term deposit? (binary: "yes","no")

# Problem Statement
Term deposits allow banks to hold onto a deposit for a specific amount of time, so banks can invest in higher gain financial products to make a profit. In addition, banks also hold better chance to persuade term deposit clients into buying other products such as funds or insurance to further increase their revenues. As a result, the Portuguese bank would like to identify existing clients that have higher chance to subscribe for a term deposit and focus marketing effort on such clients.

**Objective**: Develop a classification model to predict whether a Customer will subscribe the bank term deposit or not, and also the likelihood.

# Predictive Model
I have used **[CatBoost](https://catboost.ai/)** to develop classification model to predict the target variable in this specific case. CatBoost handles the categorical features/variable very conveniently.
