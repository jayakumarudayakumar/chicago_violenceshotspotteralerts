## Chicago Police Department: Violence Reduction - Shotspotter Alerts 

The report on the Chicago Police Department’s use of ShotSpotter alerts analyzes gunshot incidents to understand spatial and temporal trends and develop predictive models. Key research questions address whether specific neighborhoods experience higher incident rates, the correlation of incidents with times of day or week, and the potential for a model to predict incident types.

### Three modeling approaches were explored,
1. The GLM-logistic regression model identified significant predictors like a month, day of the week, number of rounds, and longitude, showing promising but improvable results in classifying incidents
2. The decision tree model, with high accuracy and a robust AUC score, demonstrated exceptional predictive performance
3. The linear regression model, while identifying some significant factors, had limited explanatory power regarding incident frequency, suggesting a need for further refinement

### Research Questions and Answers

1. Community Safety Disparities: Are specific neighborhoods experiencing significantly higher gunshot incident rates than others?  

   This question analyzes spatial dynamics to identify areas burdened by disproportionate incidents, revealing potential hotspots and regions with lower occurrences. 

   Method to answer this question - EDA: We were able to illustrate the location-specific graphical plot in the exploratory data analysis by utilizing location features 

2. Temporal Patterns and Law Enforcement Resource Allocation: Is there a noticeable correlation between the time of day or week and the occurrence of gunshot incidents?  

   This investigation seeks to uncover temporal trends, highlighting peak activity periods. Insights gained will assist in optimizing resource allocation and scheduling     
   within law enforcement frameworks. 

   Method to answer this question - EDA: We can answer this question by performing exploratory data analysis. 

3. Predictive Model for Incident Discrimination: Can we develop a robust predictive model capable of distinguishing between incident types, such as single and Multiple 
   gunshots, using factors like location and time?  

   This question aims to harness predictive analytics to create a sophisticated model that facilitates swift and targeted responses, enhancing community safety and law 
   enforcement strategies. 

   Method to answer this question: Predictive Models: We have tried predictive models such as GLM—logistic Regression, linear regression, and Decision-Tree Models. 
 
## Model Performance

GLM-Logistic Regression
- Significant predictors: MONTH, DAY_OF_WEEK, ROUNDS, and LONGITUDE have low p-values, indicating their significance
- ROUNDS and LONGITUDE show high importance
- The model exhibits a good fit, as indicated by the AIC and residual deviance
- The confusion matrix shows strong performance with high true positive and true negative rates but room for improvement in minimizing false positives and false negatives. 
- ROC curve demonstrates robust discriminatory power with an AUC of approximately 0.925. 

Decision-Tree
- A decision tree structure was presented, showcasing variable importance and terminal nodes
- The AUC of around 0.995 indicates exceptional predictive capability
- Confusion matrix highlights high accuracy with minimal misclassifications
- ROC curve underscores outstanding predictive performance

Linear Regression
- Significant coefficients for ZIP_CODE, MONTH, and LATITUDE
- The model's performance metrics indicate limited explanatory power with a low R-squared value
- Comparison between trained and test data reveals differences in model performance

## Conclusion
Our detailed analysis explores three models to understand firearm incidents detected by ShotSpotter alerts. The GLM-Logistic Regression model identifies key predictors like MONTH, DAY_OF_WEEK, ROUNDS, and LONGITUDE, emphasizing their role in predicting incident types. While this model shows vital performance metrics and discriminatory power, there's potential for improvement in reducing false positives and negatives. In contrast, the Decision-Tree model excels in predictive capability, boasting high accuracy and minimal misclassifications. However, the linear regression model, which highlights significant predictors, falls short of explaining variations in incident occurrences, indicating the need for further refinement. These insights underscore the importance of selecting the right modeling approach tailored to address specific business inquiries effectively
