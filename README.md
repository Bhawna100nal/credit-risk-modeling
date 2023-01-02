# credit-risk-modeling
credit risk modeling: Consumer loan data 2007-2014.
Modeled the credit risk associated with consumer loans. Performed exploratory data analysis (EDA), preprocessing of continuous and discrete variables using various techniques depending on the feature. Checked for missing values and cleaned the data. Built the probability of default model using Logistic Regression. Visualized all the results

PD (Probability of default): Logistic regression

LGD (Loss given default): Beta regression

EAD (Exposure at default): Beta regression

PD needs a flag of whether borrower defaulted or not (loan_status column helps).

LGD: How much of the loan was recovered after borrower had defaulted (recoveries column helps)

EAD: Total exposure the moment the borrower defaulted compared to total exosure in the past (total_rec_prncp column helps)

Grade is that of the external agency given as letters from A to G.

DTI is debt-to-income ratio

PD model: All independent features need to be categorical. Grouping multiple categories into one to reduce the number of categories. We need to make continuous variables (Annual income, number of credit inquiries in the last 6 months) discrete using dummy variables.

Fine classing: Dividing the data into finite intervals (Ex: number of months since the loan has been granted can be grouped as less than 1, 1 to 3, 4 to 6...). The grouping of the variables will be based on if the adjacent category discriminates between deafulted and non=defaulted borrowers. If they don't discriminate, they are merged into one.

Coarse classing: After grouping based on discrimination between defaulted and non-defaulted, categories are obatained. There is no need for intervals to be equal.
