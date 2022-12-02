
# Predicting Number of Days Until Payment of a Invoice using ML
The task was to build a model that helps estimating when an invoice will be paid.
The given Dataset had features like Description of the invoice, Vendor Name, Date and Time when invoice was created, its Due date, Total Amount, 
Settled Amount, Outstanding Date and Number of Days had to be predicted.

Cassandra is a Data Science event of UDYAM, organised by Electronics Engineering Society IIT(BHU) Varanasi

28th March 2022 to 08 April 2022 


## 🔗 Links
[kaggle competion link here](https://www.kaggle.com/competitions/cassandra-udyam-2022)

Teamname : BinaryBeasts

## Tools and Techniques Used
- Data Exploration using Matplotlib(kde plot)
- Feature Engineering:
### Approches Applied
- Found 'Created' column irrelevant to the target
- dropped 'Description' as test data had many categories, which were absent in train data
- Calculated number of days between invoice date and due date and then dropped both invoice_date and due_date columns
- 'Settled' and 'Outstanding were corelated so dropped 'Settled'.
- Encoded 'Vendor_Name' with their frequency multiplied by their rank as per descending order of their frequency so that each vendor gets a unique code
- dropped rows having negative 'Number_of_Days_until_Payment' ; as there were only 9 such rows (outliers)

### Insights Drawn
- 'Amount' data was very imbalnced and therefore 'settled' and 'outsdatnding' data was imbalanced, hence Xgboost was preferred, since it is unaffected by imbalanced data
- there was a lot of randomness in 'number of days until payment' for each vendor therefore mean n median target encoded new feature didnt work well


## As a result we were shortlisted in Top 10 teams
