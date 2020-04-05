
# Kaggle Mail Classification
_This work is related to __in-class Kaggle Competition in Machine Learning class at CentraleSupélec__ and was done by C. Morand-Duval, R. Chen, I. Zizi and A. Ohleyer._ [Find the full report here](Report.pdf)<br>
[Link to the challenge](https://www.kaggle.com/c/ml-f19/)


## CONTEXT
We often face the problem of searching meaningful emails among thousands of promotional emails. This challenge focuses on creating a multi-class classifier that can classify an email into one of the four classes based on the metadata extracted from the email.

## DATA
- date - unix style date format, date-time on which the email was received, e.g. Sat, 2 Jul 2016 11:02:58 +0530
- org - organisation of the sender, e.g. centralesupelec, facebook, and google.
- tld - top level domain of the organisation, eg. com, ac.in, fr, and org.
- ccs - number of emails cced with this email, e.g. 0, 2, and 10.
- bcced - is the receiver bcc'd in the email. Can take two values 0 or 1.
- mail_type - type of the mail body, e.g. text/plain and text/html.
- images - number of images in the mail body, e.g. 0, 1, and 100.
- urls - number of urls in the mail body, e.g. 0, 1, and 50.
- salutations - is salutation used in the email? Either 0 or 1.
- designation - is designation of the sender mentioned in the email. Either 0 or 1.
- chars_in_subject - number of characters in the mail subject, e.g. 0, 1, and 10.
- chars_in_body - number of characters in the mail body, e.g. 10 and 10000.
- abel - label of this email. 0 is for update, 1 is for social, 2 is for forum and 3 is for promotional. Label is only present in train.csv. test.csv has all other features.
 

## Feature Engineering
- Pre-processing
- Exploratory Data Analysis
- Feature Selection

## Model Tuning and comparison
- RandomForest
- SVM
- Neurl Networks
- Gradient Boosting Classifier
- Stacking: Majority Voters
s are: the act type, the payment method, the channel id

## Conclusion
The final model designed to classify emails is a Random Forest Algorithm using 175 features. It yields an F1-score of __0.95585__ on Kaggle and uses specific features, namely ccs, images, urls, characters in subject, character in body, year, month, day, hour, minute, second, weekday, time zone, mail_type_2, multiple company names, mail_type_2 frequency, time zone frequency and the sum of binary organisation and top-level domain features. The model was tested using grid search cross validation and 5-folds cross validation to avoid over-fitting.
