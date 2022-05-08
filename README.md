# Web-Scraping-for-Indeed.com-and-Predicting-Salaries

Business Case Overview
I was working as a data scientist for a contracting firm that's rapidly expanding. Now that they have their most valuable employee (me!), they need to leverage data to win more contracts. My firm offers technology and scientific solutions and wants to be competitive in the hiring market. MY principal wants me to determine the industry factors that are most important in predicting the salary amounts for these data.
To limit the scope, my principal has suggested that I focus on data-related job postings, e.g. data scientist, data analyst, research scientist, business intelligence, and any others I might think of. I may also want to decrease the scope by limiting my search to a single region.

Hint: Aggregators like Indeed.com regularly pool job postings from a variety of markets and industries.

## Goal: 
Scrape my own data from a job aggregation tool like Indeed.com in order to collect the data to best answer this question.

Directions¶
In this project I will be leveraging a variety of skills. The first will be to use the web-scraping and/or API techniques I've learned to collect data on data jobs from Indeed.com or another aggregator. Once I have collected and cleaned the data, I will use it to address the question above.

### Factors that impact salary

To predict salary the most appropriate approach would be a regression model.
Here instead I just want to estimate which factors (like location, job title, job level, industry sector) lead to high or low salary and work with a classification model. To do so, I've splitted the salary into two groups of high and low salary, for example by choosing the median salary as a threshold.

Used all the skills I have learned so far to build a predictive model.
The most important thing is to justify my choices and interpret my results. *Communication of the process is key.* Note that most listings **DO NOT** come with salary information. I'll need to be able to extrapolate or predict the expected salaries for these listings.

## Suggestions for Getting Started

1. Collect data from [Indeed.com](www.indeed.com) (or another aggregator) on data-related jobs to use in predicting salary trends for my analysis.
  - Select and parse data from *at least 1000 postings* for jobs, potentially from multiple location searches.
2. Find out what factors most directly impact salaries (e.g. title, location, department, etc).
  - Test, validate, and describe my models. What factors predict salary category? How do my models perform?
3. Discover which features have the greatest importance when determining a low versus high paying job.
  - My Boss is interested in what overall features hold the greatest significance.
  - HR is interested in which SKILLS and KEY WORDS hold the greatest significance.   
4. Author an executive summary that details the highlights of my analysis for a non-technical audience.
5. Tried framing the salary problem as a classification problem detecting low versus high salary positions.



## Useful Resources

- Scraping is one of the most fun, useful and interesting skills out here.
- [Here is some advice on how to write for a non-technical audience](http://programmers.stackexchange.com/questions/11523/explaining-technical-things-to-non-technical-people).
- [Documentation for BeautifulSoup can be found here](http://www.crummy.com/software/BeautifulSoup/).



## Conclusion:

After determining the job title and Summary to create predictors for my models I ran Logistic Regression,KNN classifier,DTC,RFC on my training data. After using GridSearch to find the optimal parameters for GridSearch on Logistics Regression and GridSearch on Descission Tree Classifier, the best score achieved on my  data for the Logistic Regression model is 75%,the best score for the DTC model was 68%,
Therefore TP is Low Salary and True N is High Salary;FP is Predicted Higher Salary than FN Predicted Lower Salary.
The confusion matrix provide a compromise balancing  to adjust the threshold:
TP=True Positive=111/,TN=True Negative=156,FP=False Positive=70,FN=False Negative=30
For Random Forest Classifier:TP=True Positive=123/,TN=True Negative=126,FP=False Positive=58,FN=False Negative=60.
Per graphs shown above the Log.Reg. Model coefficients are indicating predictors of a lower Salary in keywords,such:Education,Research,Graduate,on the other hand predictors for higher Salary in keywords are:Scientist,Senior,Enjineer,Lead.All the rest key words are less frequently used for the job listings and are less influenced features in the Decision Tree.

The ROC Curve  plotted above for class 1 High Salary and class 0 Low Salary. As a matter of fact the Log. Reg. model is performing the baseline in the way that  as it increased the threshold to remove false positives, it will acquire less false negatives in relation to how many false positives will be lost.

ROC gives a visualisation of the increased number of false positives for each increase in true positives that my models predict.

Copy Right © | Olga Caireac | General Assemply | 
Copy Right © | Olga Caireac | General Assemply | 
