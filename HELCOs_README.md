# Home Equity Lines of Credit(HELOCs) Probability of Defaults Analysis

## 1- Business Goals Overview
Analyzing the **Probability of Default (PD)** for a financial entity like a **Helco** (Home Equity Line of Credit) involves assessing borrowers' likelihood of failing to meet their debt obligations. The primary goal is to help stakeholders accurately assess and manage **default risks**, ensuring regulatory compliance, maintaining portfolio health, and making informed decisions that balance risk and profitability.
                                                                                    
## 2- Technical Highlights
This project extensively leveraged the powerful capabilities of **Python** to conduct a comprehensive range of tasks including meticulous data cleaning, sophisticated preprocessing techniques, intricate modeling, and creating detailed, insightful visualizations achieved by using **Pandas, Numpy, Scikit-learn, Matplotlib, and Seaborn** to handle and interpret the dataset effectively. In predictive modeling, the project went beyond the conventional use of **Logistic regression**, embracing more sophisticated and advanced machine learning algorithms. Specifically, it included the implementation of **Decision Trees and Random Forest models**. These models are known for their ability to handle complex, non-linear relationships in data, and they provide robust, data-driven insights.

## 3- Model Selections 
1. **Univariate Logistic Regression:** Knowing the relationship between each single predictor and the targeted variable.
<img width="800" alt="image" src="https://github.com/jh4581/resume-projects-portfolio.github.io/blob/main/images/univariate.png">
<img width="600" alt="image" src="https://github.com/jh4581/resume-projects-portfolio.github.io/blob/main/images/univariate1.png">

2. **Multiple Logistic Regression:** captures the relationship between multiple independent variables and the probability of default, providing a more comprehensive risk assessment. It allows for including interaction terms and non-linear relationships using polynomial or spline functions.
<img width="800" alt="image" src="https://github.com/jh4581/resume-projects-portfolio.github.io/blob/main/images/Multi.png">
<img width="800" alt="image" src="https://github.com/jh4581/resume-projects-portfolio.github.io/blob/main/images/Multi1.png">

3. **Decision Tree Model:** can model complex, non-linear relationships without needing any transformation of the variables; Decision trees intrinsically perform feature selection by choosing the most informative features for splitting.
<img width="800" alt="image" src="https://github.com/jh4581/resume-projects-portfolio.github.io/blob/main/images/tree1.png">
<img width="800" alt="image" src="https://github.com/jh4581/resume-projects-portfolio.github.io/blob/main/images/tree2.png">
<img width="1000" alt="image" src="https://github.com/jh4581/resume-projects-portfolio.github.io/blob/main/images/tree3.png">

4. **Random Forest Model:** can provide high accuracy and good performance on a variety of datasets due to their ensemble nature and give estimates of feature importance, helping to identify the most significant predictors of default.
<img width="1200" alt="image" src="https://github.com/jh4581/resume-projects-portfolio.github.io/blob/main/images/rf1.png">
<img width="800" alt="image" src="https://github.com/jh4581/resume-projects-portfolio.github.io/blob/main/images/rf2.png">
<img width="800" alt="image" src="https://github.com/jh4581/resume-projects-portfolio.github.io/blob/main/images/rf3.png">

When considering the factors contributing to the probability of default, DELINQ, DEBTINC, NINQ,  DEROG, and VALUE emerge as the most significant predictors. DEBTINC, or the debt-to-income ratio, underscores the importance of a customer's financial burden in evaluating credit risk. DELINQ (number of delinquent credit lines), NINQ (number of recent credit inquiries), NINQ (number of recent credit inquiries), and DEROG (number of major derogatory reports) exhibit a positive correlation with default probability. These factors are indicative of recent financial stress or mismanagement, which can signal a higher risk of default. However, the 'VALUE' of an asset has a negative correlation with default probability. This is because a higher property value can provide a financial safety net, enabling borrowers to access equity in tough times instead of defaulting. It also suggests that the borrower may have greater financial stability and more to lose by defaulting, thereby providing a strong incentive to maintain their loan payments. However, this relationship can be influenced by market conditions and the borrower's overall financial health, underscoring the importance of a multifaceted risk assessment.

## 4- Conclusion
1. Logistic Regression has the lowest performance across all metrics compared to the other two models. It has particularly low recall and F1 scores, indicating that it may not be the best at capturing all the default cases.

2. The Decision Tree Model shows very high recall and precision. It has the highest F1 score, which is a harmonic mean of precision and recall, suggesting a good balance between the two. Additionally, its AUC is the highest, showing a strong capability in distinguishing between classes.

3. The Random Forest Model has a high precision, indicating that when it predicts a default, it is very likely to be correct. It has a slightly lower recall than the Decision Tree, suggesting it doesn't capture as many of the true default cases. However, it does have a higher accuracy and the AUC score is very close to that of the Decision Tree.

### Choosing the Final Model:
The choice of the final model should be guided by the specific business objectives and the costs associated with false positives (incorrectly predicting default when there is none) versus false negatives (failing to predict a default that does occur).

- If the cost of missing a default is very high (a false negative is very costly), the Decision Tree Model may be the best option due to its highest recall and F1 score.

- If the goal is to ensure that the cases identified as defaults are indeed defaults (minimizing false positives), the Random Forest model would be preferable because of its high precision.

- If overall accuracy and the balance between true positive and true negative rates are the priority, then the Random Forest model may be the most suitable as it has the highest accuracy and a very competitive AUC score.

Given the metrics, the Decision Tree Model stands out for its ability to correctly identify default cases (high recall) while maintaining high precision, and it has the highest AUC score. However, the Random Forest model, with its slightly better accuracy and competitive AUC, could be more appealing if the problem requires a more balanced overall performance.

In this instance, the Decision Tree model's superior performance metrics make it the preferred choice, provided the model's robustness has been validated through appropriate cross-validation techniques and that it has been tested on an independent validation set to confirm these results.

