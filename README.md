# deep-learning-challenge


## Analysis of Alphabet Soup Applicants
This repository is dedicated to creating a neural network that is used to analyse applicants to the Alphabet Soup foundation for donations for their projects. Using a chunk of the historical data, the model is trained, and then some data is reserved for testing to confirm the accuracy of the model. 


## Results
Based on the neural network model, I would definintely not use this method primarily as the main source of finding whether or not an applicant should be approved for funding. Even with a 95% accuracy, it should always be reviewed by someone to dig deeper. The method of using a neural network is a great prelimiary source of information, but that's all it should be treated as in this instance. We have no control of the decision making, or how it decided to accept or reject applicants.


### Data Preprocessing
The "IS_SUCCESSFUL" column is the target column of the dataset, confirming whether or not the application was approved. For the final most accurate (73.7%) neural network, the features that were used to train and test the model were 'APPLICATION_TYPE', 'CLASSIFICATION', 'ORGANIZATION', 'SPECIAL_CONSIDERATIONS', 'INCOME_AMT','AFFILIATION', 'ASK_AMT_binned','USE_CASE'.
The "EIN","NAME" columns were dropped from the dataframe, as EIN was unrelated, and the name shouldn't impact the training data.


### Compiling, Training, and Evaluating the Model
After doing some research and testing in the file, I found the sweet spot for efficiency and accuracy was 3 Layers with 8, 8, 7 nodes. The first two using PReLU, and the last using sigmoid before the output layer uses relu. This was mostly chosen down to trial and error. I was unable to achieve the target of 75% and not too sure why. I think it's likely because the provided dataset doesn't provide any insight into the financial data of the applicant (eg, Ongoing operations costs, debt, etc) that could give vital insight into whether or not the loan should be approved. Using two hidden layers instead of three certainly does improve performance, but since I couldn't reach 75%, this was the closest I could get.


## Summary
As stated above, I think with the accuracy being under 75%, it would not be a great idea to use this neural network for anything more than a preliminary indication for someone else to look over and confirm.
