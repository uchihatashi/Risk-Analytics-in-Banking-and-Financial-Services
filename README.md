## Problem Statement
### Introduction
In this case study, we try to understand and solve how real business problems are solved using EDA. And understanding of risk analytics in banking and financial services and understanding how data is used to minimize the risk of losing money while lending to customers.

### Business Understanding
You work for a consumer finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant's profile. Two types of risks are associated with the bank's decision:

- If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company
- If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company

The data given below contains the information about past loan applicants and whether they ‘**defaulted** or not. The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc.

In this case study, you will use EDA to understand how **consumer attributes** and **loan attributes** influence the tendency of default.

<img src="https://github.com/uchihatashi/Risk-Analytics-in-Banking-and-Financial-Services/blob/main/Loan%20Data%20Set.jpg" alt="Loan Data Set"/>

When a person applies for a loan, there are two types of decisions that could be taken by the company:
1. **Loan accepted:** If the company approves the loan, there are 3 possible scenarios described below:

	1. **Fully paid:** Applicant has fully paid the loan (the principal and the interest rate).

	2. **Current:** Applicant is in the process of paying the instalments, i.e. the tenure of the loan is not yet completed. These candidates are not labelled as 'defaulted'.

	3. **Charged-off:** Applicant has not paid the instalments in due time for a long period of time, i.e. he/she has defaulted on the loan.

2. **Loan rejected:** The company had rejected the loan (because the candidate does not meet their requirements etc.). Since the loan was rejected, there is no transactional history of those applicants with the company and so this data is not available with the company (and thus in this dataset)

### Business Objectives
This company is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures. Borrowers can easily access lower interest rate loans through a fast online interface. 

Like most other lending companies, lending loans to‘risky’ applicants is the largest source of financial loss (called credit loss). The credit loss is the amount of money lost by the lender when the borrower refuses to pay or runs away with the money owed. In other words, borrowers who default cause the largest amount of loss to the lenders. In this case, the customers labelled as 'charged-off' are the 'defaulters'.

If one is able to identify these risky loan applicants, then such loans can be reduced thereby cutting down the amount of credit loss. Identification of such applicants using EDA is the aim of this case study.

In other words, the company wants to understand the **driving factors (or driver variables)** behind loan default, i.e. the variables which are strong indicators of default.  The company can utilise this knowledge for its portfolio and risk assessment. 

To develop your understanding of the domain, you are advised to independently research a little about risk analytics (understanding the types of variables and their significance should be enough).

### Structure:

	-- data
	 	-- Data_Dictionary.xlsx
	 	-- master_loan.csv
	 	-- loan.csv (in the given link)
	 -- Lending Club Case Study.pdf
	 -- Lending Club Case Study.ipynb


### Data Understanding

1. Download the dataset from below. It contains the complete loan data for all loans issued through the time period 2007 t0 2011.
- https://drive.google.com/file/d/1NGEAOLql7Ols9B4RYMEa6bG_eQRJnYa6/view?usp=sharing

2. Data dictionary which describes the meaning of these variables from the given dataset.



## Summary:

##### Based our analysis done we can conclude the below mentioned points:
- Small Business Applicants have high chances of getting charged off.
- Charged off proportion increases with grades moving from “A” towards “G”.
- Charged off proportion increases as Interest Rate Increases.
- Higher the public bankruptcy record greater the charged-off proportion.
- Those who already have Derogatory Public Records have higher charged off chances than others.
- Charged off applicants are more who had taken loan for 36 months as compared to 60 months.
- The percentage of Charged Off loans increases substantially as we go up the loan amount 

##### Suggestions:
- Reducing the number of approvals where purpose is small business
- Loan approval should be avoided for those who already have Public Bankruptcy Records.
- Start charging higher interest rates for loans with debt to income ratio greater than 20
- Max amount committed to grade C to G should be reduced since they contribute the most to loan defaulting compared to grade A and B.
- Lower annual income applicants should be avoided for big loan amounts with higher interest Rates.
