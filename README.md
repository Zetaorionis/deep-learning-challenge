# deep-learning-challenge


## Overview of the Analysis
In this analysis, the purpose is to simulate a real-world use of machine learning and neural networks. In this challenge we are referencing Alphabet soup as the pseudo client.

Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. In this challenge, use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

To conduct the analysis, a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years was used. Within this dataset are several columns that capture metadata about each organization:
* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding.
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special considerations for application
* ASK_AMT—Funding amount requested.
* IS_SUCCESSFUL—Was the money used effectively.


## Results
* Data Preprocessing
	* Target for this model is the IS_SUCCESSFUL variable.
	* The following variables were chosen as the models Features: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE,           ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS and ASK_AMT.
    * Variables EIN and NAME were removed, the model has no use for identification data and can potentially cause an issue if        kept.

* Compiling, Training, and Evaluating the Model
    * 110 neurons, 3 layers and activation functions relu and sigmoid were used in the first run. 
    * Model did not achieve a target predictive accuracy higher than 75%. Even when trying to optimize the model, accuracy           remained below 75%.
    * To try and improve performance, a keras Tuner was used to automate optimization. After running 60 trials the models failed to acheieve a accuracy higher than 75% as well as the original model. However, with the tuner, the top three models all prefered tanH as it's activation.
 
      
## Summary

Currently, the models are subpar and I would not reccommend any use. There seems to noise in the data, I also recommend revaluating the preprocessing, properly balencing the weights of the targets and, if avalible, request more data.
