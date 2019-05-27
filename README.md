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
Where each email has the subject of the email as the first line and the rest of the message on the next lines. 

Before creating and training the classifiers, we preprocessed the data. We removed punctuation, removed stopwords and tokenization. We chose to leave in punctuation such as `?` and `!` since excess use of these symbols is often a characteristic for spam-mails. To create word embeddings, we create a dictionary for each word in the mail. 

Example ham-mail after preprocessing:

```
'Subject': True, 'research': True, 'dept': True, 'move': True, 'hello': True, 'everyone': True, 'attached': True, 'churn': True, 'relocation': True, 'request': True, 'office': True, 'exchanges': True, 'within': True, 'group': True, '19': True, 'th': True, 'floor': True, 'grouped': True, 'sets': True, 'two': True, 'rush': True, 'order': True, 'would': True, 'appreciate': True, 'getting': True, 'soon': True, 'possible': True, '15': True, 'august': True, 'great': True, ',': True, 'let': True, 'know': True, 'something': True, 'understand': True, 'thanks': True, '!': True, 'shirley': True
```


### **Results Naive Bayes:**

Accuracy = 97.47%

| EvaluationMetric | Precision | Recall | F-score |
|   :---:    |   :---:   |  :---: |  :---:  |
|   Macro    |   97.56%  |  97.47%|  97.48% |
|   Micro    |   97.47 % |  97.47%|  97.47 %|


The NB confusion matrix looks as follows:

|                  |    Spam   |   Ham   | 
|      :---:       |   :---:   |  :---:  |
|      Spam        |    357    |    18   |
|       Ham        |    374    |    1    | 

### **Results Logistic Regression:**

Accuracy = 94.85%

| EvaluationMetric | Precision | Recall | F-score |
|   :---:    |   :---:   |  :---: |  :---:  |
|   Macro    |   95.07%  |  94.95%|  94.97% |
|   Micro    |   94.85 % |  94.85%|  94.85% |

The LR confusion matrix looks as follows:

|                  |    Spam   |   Ham   | 
|      :---:       |   :---:   |  :---:  |
|      Spam        |    12    |    61   |
|       Ham        |    7    |    54    |

These rates don't count up to the test set of 750 txt files. So, our LR is not reliable.


### Conclusion
The desired outcomes were not reached due to the fact that the Logistic Regression classifier was not implemented in a correct way. This lead to unfinished experiments on the LR classifier, as well as no comparison-experiments between the two classifiers.
Nonetheless, the Naïve Bayes classifier itself gave some very good results, that could be explained due to the simplicity of the dataset. Hence, we can only give a conclusion on the Naïve Bayes classifier, namely that pre-processing on stopwords does not improve performance and NB is a very good baseline for 'simple' spam emails.
From this project, not many new things can be learned in regards to the well-researched topic of Naïve Bayes in spam detection classifiers. Nonetheless, we are still pleased with how our own NB-classifier turned out.
