# NLPSpamDetection

For this project of NLP (Maastricht University, FSE, DKE) we created a spam filter that used Naive Bayes and Logistic Regression to classify an email from the Enron-Spam dataset. The data can be found from this link: http://www2.aueb.gr/users/ion/data/enron-spam/

The data was formatted like this:

```
Subject: research dept . move
hello everyone :
attached is the churn relocation request for some office exchanges within
the research group on the 19 th floor . i have grouped them in sets of two
which are the exchanges .
this is a very rush order . we would appreciate your getting to this as
soon as possible - the 15 th of august would be great , if possible .
let me know if there is something that you do not understand . thanks !
shirley
```
Where each email has the subject of the email as the first line. 

Before creating and training the classifiers, we preprocessed the data. We removed punctuation, removed stopwords and tokenization. 

Example ham-mail after preprocessing:

```
'Subject': True, ':': True, 'research': True, 'dept': True, '.': True, 'move': True, 'hello': True, 'everyone': True, 'attached': True, 'churn': True, 'relocation': True, 'request': True, 'office': True, 'exchanges': True, 'within': True, 'group': True, '19': True, 'th': True, 'floor': True, 'grouped': True, 'sets': True, 'two': True, 'rush': True, 'order': True, 'would': True, 'appreciate': True, 'getting': True, 'soon': True, 'possible': True, '15': True, 'august': True, 'great': True, ',': True, 'let': True, 'know': True, 'something': True, 'understand': True, 'thanks': True, '!': True, 'shirley': True 
```


### **Results Naive Bayes:**

Accuracy = 97.47%

| EvaluationMetric | Precision | Recall | F-score |
|   :---:    |   :---:   |  :---: |  :---:  |
|   Macro    |   97.56%  |  97.47%|  97.48% |
|   Micro    |   97.47 % |  97.47%|  97.47 %|




### **Results Logistic Regression:**

Accuracy = 97.47%

| EvaluationMetric | Precision | Recall | F-score |
|   :---:    |   :---:   |  :---: |  :---:  |
|   Macro    |   97.56%  |  97.47%|  97.48% |
|   Micro    |   97.47 % |  97.47%|  97.47 %|
