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

## 4- Conclusion
