# llm-argument-mining
## Folder Documentation
1. ASP_input
2. ASP_output
3. annotated dataset
4. models
5. web-dash

 **1. The "ASP_input" Folder**: This directory stores input files for Answer Set Programming (ASP). The files within this folder are expected to be of the `.pl` Prolog file type.

**2. The "ASP_output" Folder**: This directory contains the results generated by the Answer Set Programming. The output files are expected to be in `.txt` text format.

Inside both the `ASP_input` and `ASP_output` folders, files are organized based on different models. Each model corresponds to a specific algorithm or language model, the files are further categorized accordingly as below.

  + M-arg Models:
    + M-arg Models: relation_AAF
  + Conventional Models:
    - Support Vector Machine: SVM
    + Logistics Regression: LR
    + Decision Tree: Decision_Tree
    + Naive Bayes: Naive_Bayes
      
  + Large Language Models:
    + Text Davincii 003: gpt_davinci
    + GPT 3.5 turbo: gpt_35
    + GPT 3.5 version 0613: gpt_35_0613


**3. The "annotated dataset" folder** stored all datasets from M-arg(`Mestre-etal-2021-arg`). 

**4. The "models" folder** will store model files of Conventional Models as a `.joblid` type.
  
  + Support Vector Machine model:
    + SVM_model.joblib
  + Logistics Regression model:
    + logistics_regression_model.joblib
  + Decision Tree model:
    + tree_model.joblib
  + Naive Bayes model:
    + Naive_Bayes_model.joblib
  

**5. The "web-dash" folder** is a folder that stores all necessary files to open the local host to visualize the node graph. Inside this folder has<br />

  + Procifile: is a config to set a web server on Heroku
  + mvp1data.csv: to store full data of predicted relation of the `Large Language Models` such as Text Davincii 003, GPT 3.5 turbo, and GPT 3.5 version 0613
  + mvp2data.csv: will contain the content of a prediction of the first 100 pairs in each topic from `Conventional Models`(Support Vector Machine, Logistics Regression, Decision Tree, and Naive Bayes).
  + requirements.txt: is all requirement library to run this local host website
  + setup.py: contains a line of code for running an interacted local host website


## File Documentation 
1. Prediction.ipynb
1. Statistics.ipynb
1. Marked_aaccepted.ipynb
1. Model_selection.ipynb
  
**1. "Prediction.ipynb"** contains a line of code that sends a prompt through the `GPT model API` and is stored in mvp1data.csv.

**2. "Statistics.ipynb"** contains content showing dataset statistics after prediction as a First Minimum Viable Product.

**3. "Marked_aaccepted.ipynb"** will be separated into two main sections. <br />
  + Before Answer Set Programming: This section will select the first 100 pairs of sentences in each topic and create a     dictionary to map a number and sentence. Convert into the .pl (Prolog) file type which will be stored in The `"ASP_input"` Folder
  + After Answer Set Programming: This section contains content of converting the result from the Answer Set Programming as .txt (text) format in The Folder name `"ASP_output"` and stored in the CSV file name `"mvp2data.csv"`.

**4. "Model_selection.ipynb"** will be the content of training `Conventional Models` on data from the CSV file name `"mvp2data.csv"`.


