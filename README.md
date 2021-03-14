# Neural_Network_Charity_Analysis
To design a Deep Learning Neural Network that can help AlphaBet Soup determine which charity organization should receive its donation.


### Overview of the Neural_Network_Charity_Analysis

The purpose of this analysis is to design a Deep Learning Neural Network that can help AlphaBet Soup determine which charity organization should receive its donation. The Deep learning model will leverage and analyze various important input dataset of different charity organizations to determine those that are high risk (based on past performances) and then accurately predict which organization should receive AlphaBet Soup's donation.

Specifically, this work invoved;

  1. Preprocessing of the Data for the Neural Network Model
  2. Compiling, Training, and Evaluating the Model
  3. Optimizing the Model
  4. Generating a written report on the Neural Network Model


To generate this analysis, I utilized the following resources;

  - Data Source: charity_data.csv

  - Softwares: Python, Jupyter Notebook, Tensorflow Library


### Results

The following are extracts from the result of the analysis;

**Data Preprocessing**

 - **Variable(s) Considered For Targets:** The "IS_SUCCESSFUL" variable is the only one that I considered as the target. This is because this is the only variable in our dataset that indicates whether or not the fund received by such NGOs (organization) was justifiably utilized for its intended purpose.

 - **Variable(s) Considered For Features:** The following - "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL CONSIDERATIONS", "ASK_AMT", were the variables considered as features (input data). The snapshot below shows the details of the target and features variables


 - **Variable(s) That Should Be Removed:** The "EIN" variable is the only one that I removed from my input data. This was removed because this data has a close and direct relationship with the NAME variable and as such will be redundant. In addition, since "EIN" is numeric, it could also distort our model as our model may erroneously attach significant importance to each of the the values of this variable  

**Compiling, Training & Evaluating The Model**

 - **Neurons, Layers & Activation Functions Selected:** For the optimized model that generated an accuracy of 79.02%, three hidden layers (as compared to 2 initially used in deliverable 2) were used. 100, 50 & 30 neurons were used for the first, second and third layers respectively for the optimized model(compared to 80 & 30 used for the first and second layers in delivrable 2). In addition 100 epochs were utilzed for the optimized model (compared to 50 utilized for the second deliverable). Finally, the "Relu" activation functions was used for the hidden layers while "Sigmoid" was used for the output layer. The snapshot below shows details of the hidden layers, neurons and activation function used for the optimized model


 - **Were you able to achieve the target performance:** Yes I was able to achieve the target performance. The accuracy score for my optimized model was 79.02%. The snapshot below shows the accuracy of the model


 - **Steps that I took to Optimize The Model Performance:** To achieve the target accuracy result, Firstly, I included the NAME variable as part of my input data. Secondly, As a categorical data, I binned the "NAME" variable by identifying and placing organizations that have applied less than 5 times in to an "OTHERS" bin. Thirdly, I reduced the "OTHERS" bin for "APPLICATION TYPE" to counts of less than 156. Fourthly, I increased the hidden layers for my model to 3 with 100, 50 & 30 neurons respectively and lastly, I increased my number of Epochs to 100 from 50.


### Summary
In summary, looking at our Neural Network model's performance metrics, the model was able to correctly predict the performance of the NGOs (organizations) in our dataset (i.e. whether or not they were successful with funds received) approximately 79% of the time. Considering that our input data included more than 400 different variables with more than 34,000 data points, the deep learning model was able to produce a fairly reliable classifier.

A different model that could be used to solve this classifcation problem is Random Forest Classifier. To justify this, the Random Forest model is structurally very similar to the Neural Network model and it uses a number of weak learner algorithms (decision trees) and combine their output to make a final classification (or regression) decision. Random Forest can easily handle outliers and nonlinear data, and with sufficient number of estimators and tree depth in place, Random Forest should be able to perform at a similar capacity to most Neural Network models. Putting this recommendation to test (refer to section 2 of the AlphabetSoupCharity_Optimization_New jupyter notebook), an accuracy of approximately 78% was generated when Random Forest classifier was used to process thesame dataset.
The image below shows a snapshot of the outcome of the Random Forest classifier on thesame dataset
