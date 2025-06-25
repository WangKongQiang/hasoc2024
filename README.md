# HASOC 2021
Offensive and problematic content including insulting, hurtful, derogatory or obscene user contributions are pervasive in social media. Societies need to develop adequate response mechanisms in order to find a balance between freedom of expression on one side and the ability to live without oppressive remarks on the other side. A requirement for any response is robust technology for identifying problematic content automatically. HASOC provides a forum for developing and testing text classification systems for various languages
  
## Sub-task A: Identifying Hate, offensive and profane content
This task focus on Hate speech and Offensive language identification offered for English, German, and Hindi. Sub-task A is coarse-grained binary classification in which participating system are required to classify tweets into two classes, namely: Hate and Offensive (HOF) and Non- Hate and offensive (NOT).

* NOT :
Non Hate-Offensive - This post does not contain any Hate speech, profane, offensive content.
* HOF :
Hate and Offensive - This post contains Hate, offensive, and profane content.

Model | Accuracy
------------- | -------------
Gaussian NM  | 50%
Logistic Regression  | 80%
KNN | 78%
SVC | 84%
Random Forest  | 82%
LSTM | 78%
BERT  | 78%


## Sub-task B: Discrimination between Hate, profane and offensive posts
This sub-task is a fine-grained classification offered for English, German, and Hindi. Hate-speech and offensive posts from the sub-task A are further classified into three categories:

* HATE :
Hate speech:- Posts under this class contain Hate speech content.
* OFFN :
Offenive:- Posts under this class contain offensive content.
* PRFN :
Profane:- These posts contain profane words.

Model | Accuracy
------------- | -------------
Gaussian NM  | 45%
KNN | 64%
SVC | 66%
Decision Tree | 53%
Random Forest  | 69%
LSTM | 60%
BERT  | 61%
Proposed Model  | 63%

### Proposed Model:
<img width="700px" src="https://user-images.githubusercontent.com/68152189/141431807-39d55624-2500-4860-8415-8c8600c3b1df.png">

Model | Accuracy
------------- | -------------
BERT_A  | 78%
BERT_OFFN/HATE  | 79% (2 epochs)
Profanity  | 92%


## Results


Sub-Task    |     Classifier      |   Macro F1-score  
------------|---------------------|--------------------
A  | DistilBERT | 75%
B  | DistilBERT | 57%


## Publication 
code and dataset for 
English Benchmark Hate Speech and Offensive Content Detection Based on Layer-by-Layer Classification.

## Code Files: 

* <a href="./Preprocess.ipynb"> Preprocess.ipynb </a> : Preprocessing the data.
* <a href="./dataAnalysis.ipynb"> dataAnalysis.ipynb </a> : Analysing the data.
* <a href="./Subtask A/ml_techniques_A.ipynb">ml_techniques_A.ipynb </a> : Applying ML models to classify the data and find the accuracy for Subtask A.
* <a href="./Subtask B/ml_techniques_B.ipynb">ml_techniques_B.ipynb </a> : Applying ML models to classify the data and find the accuracy for Subtask B.
* <a href="./Subtask A/DL_LSTM for task A.ipynb">DL_LSTM for task A.ipynb </a> : Applying DL LSTM model to classify the data and find the accuracy for Subtask A.
* <a href="./Subtask B/DL_LSTM for task B.ipynb">DL_LSTM for task B.ipynb </a> : Applying DL LSTM model to classify the data and find the accuracy for Subtask B.
* <a href="./Subtask A/BERT_A.ipynb">BERT_A.ipynb</a> : Applying DistilBERT model to classify the data and find the accuracy for Subtask A.
* <a href="./Subtask B/BERT_B.ipynb">BERT_B.ipynb</a> : Applying DistilBERT model to classify the data and find the accuracy for Subtask B.
* <a href="./Subtask B/Proposed Model">Proposed Model (Folder)</a> : Files related to the Proposed Model:
  * <a href="./Subtask B/Proposed Model/profanity_check.ipynb">profanity_check.ipynb</a> : Survey of various pre-trained models/libraries for profanity check.
  * <a href="./Subtask B/Proposed Model/ProposedModel.ipynb">ProposedModel.ipynb</a> : Implementation of the proposed model.
