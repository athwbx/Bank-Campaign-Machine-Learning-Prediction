### Bank Campaign Machine Learning Prediction

**By: Aryo Atha Rizaldi**

---

#### Business Understanding

**Context**

This data encompasses the results of a bank's marketing campaign involving direct phone calls to homes or mobile phones to encourage people to place term deposits. If the client agrees to place a deposit, the target variable is set to 'yes'; otherwise, it is set to 'no'.

**Target:**

- 0: No deposit placed
- 1: Deposit placed

**Problem Statement**

**Stakeholders:** Marketing Team, Sales and Customer Service, and Management

The process of offering term deposits through campaigns requires significant allocation of time and financial resources. Without prior screening, if the bank decides to reach out to all customers without considering their potential to place a deposit, it can result in a waste of valuable resources such as the bank's money and time spent contacting these customers. Therefore, by using Machine Learning, the efficiency of the bank's campaign process can be improved.

Machine Learning will help the bank evaluate and model complex patterns from historical data, allowing the identification of the most influential factors affecting potential customers' decisions. With this approach, the bank can improve the efficiency of its marketing campaigns, optimize resource usage, and more accurately target candidates who have a high likelihood of investing in term deposits. Here, Machine Learning can help the bank carefully screen potential customers based on data, targeting those with the highest potential to place a deposit. This approach aims to optimize the use of time and money while focusing on customer segments most likely to respond positively to term deposit offers.

**Goals**

Facing these challenges, the bank aims to develop predictive capabilities to forecast whether a prospective customer will agree to place a deposit or not. The goal is to effectively target marketing campaigns at candidates with the highest potential to invest in term deposits. With the assistance of Machine Learning, the bank hopes to improve the efficiency and effectiveness of its marketing strategies, reduce losses, and direct efforts towards the customer segments most likely to respond positively to term deposit offers. Additionally, the bank aims to minimize material and time losses by avoiding the need to contact every potential customer.

#### Analytic Approach

The plan involves conducting an in-depth analysis of the data to identify patterns that can distinguish between prospective customers who are willing to place a deposit and those who are not. Subsequently, a classification model will be built as a predictive tool for the bank, aiding in estimating the probability that a prospective customer will or will not place a deposit.

The analytic approach will involve thorough data exploration to uncover relationships and trends among related variables. Next, feature selection and data adjustment will be performed to prepare it as input for the classification model. This process is designed to improve prediction accuracy and identify key factors influencing customer decisions.

In building the classification model, appropriate Machine Learning techniques such as Logistic Regression or Decision Tree will be used, which can process complex patterns in the data. The model will be tested and evaluated using holdout data that has not been seen before to ensure reliability and good performance in predicting potential customer behavior.

With this analytic approach, the bank hopes to gain a deep understanding of critical factors influencing customer decisions and apply appropriate solutions to enhance the effectiveness of its marketing campaigns.

#### Metric Evaluation

**Type 1 error:** False Positive (Customer predicted to place a deposit but actually does not)
**Consequence:** Wasting campaign time and costs on customers who are unlikely to place a deposit

**Type 2 error:** False Negative (Customer predicted not to place a deposit but actually would)
**Consequence:** Missing out on potential customers

Below is the estimated cost the bank will incur for each false positive and false negative:

**False Positive:** The cost incurred by the bank for each false positive is the campaign cost for that customer. These campaign costs can include labor costs, media costs, and other expenses.

Based on research conducted by McKinsey & Company, the marketing campaign cost for banking products in Indonesia is estimated at Rp500,000 per customer.

Therefore, the cost incurred by the bank for each false positive is Rp500,000.

**False Negative:** The cost incurred by the bank for each false negative is the potential revenue lost from that customer. This potential revenue can include the deposit amount from the customer.

According to OJK Indonesia, the minimum bank deposit is Rp8,000,000. Therefore, the potential revenue lost from each false negative is Rp8,000,000 per customer.

**Comparison with Losing Potential Customers**

Losing potential customers can negatively impact the bank's long-term revenue. This is because the bank will lose the opportunity to offer its products and services to these customers.

According to research conducted by Frederick F. Reichheld & W. Earl Sasser, Jr., a bank that loses one customer could potentially lose revenue of up to Rp50 million per year.

If we calculate the False Positive without machine learning and without the possibility of losing customers (because all customers are contacted):
Assuming the cost incurred as stated above, which is Rp500,000/customer.
Total customers (total test and holdout data without any prior screening): 2813 customers.
If there is no screening, the bank will contact all customers without any consideration/guidance, the bank will incur costs as follows:
2813 customers x Rp500,000/customer = ± Rp1,406,500,000 (± 1.4 billion) without any certainty that the customers will place deposits.

This is less feasible because, roughly speaking, the bank has to spend ± Rp1.4 billion just for the campaign, and the cost incurred by the bank is not proportional to the potential revenue from these customers, and it will also take a lot of time to contact these customers. Therefore, considering the consequences, the main focus in developing this model is to reduce False Negatives and increase False Positives, as the bank will experience greater losses by losing potential customers compared to the campaign and time costs. The primary goal is to improve Recall, maximizing the identification of potential customers who are actually willing to place deposits, even if there is an acceptable increase in false positives. This approach is expected to achieve an optimal balance between campaign cost efficiency and maintaining the desired potential customers.

**Source**:

[McKinsey & Company, "The Data-Driven Organization: How Analytics and Machine Learning Are Transforming Business"](https://www.mckinsey.com/capabilities/quantumblack/our-insights/the-data-driven-enterprise-of-2025)    
[OJK Indonesia, "BERINVESTASI MELALUI DEPOSITO"](https://sikapiuangmu.ojk.go.id/FrontEnd/CMS/Article/252)  
[Frederick F. Reichheld and W. Earl Sasser, Jr., "The Cost of Losing a Customer"](https://hbr.org/1990/09/zero-defections-quality-comes-to-services)  
