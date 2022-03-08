## Use of Ensemble Machine Learning Models to Reduce Fatalities in Aviation Industry

**Check out the Jupyter Notebook here:**https://jovian.ai/dwivedi-rishabh95/use-of-ensemble-modelling-to-reduce-fatalities-in-aviation-industry

**A. INTRODUCTION**

The data used in this project comes from [a Kaggle competition](https://www.kaggle.com/c/reducing-commercial-aviation-fatalities), which attempts to reduce the fatalities in aviation industry by using **aircrew’s physiological data who may be distracted, sleepy or in other dangerous cognitive states.**

**B. DESCRIPTION OF THE DATA**

> ### All Data:
This Data consists of  physiological data from eighteen pilots who were subjected to various distracting events.

The training set consist of 6 minutes set of controlled experiment collected in a non-flight environment. When members are subjected to these experiments, The sensors which are attached in different parts of their body transmits the real time data with us, Based on which we predict the behavioral condition of the member at that point of time under different experiences.  

Here 4 sensors are used to prepare traing data--

1. Electrocardiogram
2. Respiration
3. Galvanic Skin Response
4. Electroencephalogram


> ### Electrocardiogram:

•	3-point Electrocardiogram signal. The sensor had a resolution/bit of .012215 µV and a range of -100mV to +100mV. The data are provided in microvolts.


> ### Respiration:

•	A measure of the rise and fall of the chest. The sensor had a resolution/bit of .2384186 µV and a range of -2.0V to +2.0V. The data are provided in microvolts.

> ### Galvanic Skin Response:

•	A measure of electrodermal activity. The sensor had a resolution/bit of .2384186 µV and a range of -2.0V to +2.0V. The data are provided in microvolts.
"The galvanic skin response (GSR, which falls under the umbrella term of electrodermal activity, or EDA) refers to changes in sweat gland activity that are reflective of the intensity of our emotional state, otherwise known as emotional arousal."

> ### Electroencephalogram :

•3-point Electrocardiogram signal. The sensor had a resolution/bit of .012215 µV and a range of -100mV to +100mV. The data are provided in microvolts.


### Following four set of cognitive states of the member in experiments:

**Channelized Attention (CA)** --the state of being focused on one task to the exclusion of all others. 

**Diverted Attention (DA)**-- is the state of having one’s attention diverted by actions or thought processes associated with a decision.

**Startle/Surprise (SS)**-- is induced by having the subjects watch movie clips with jump scares.

**Baseline** --- Normal state




> ### Training Data:
- 4.9 million samples in the training set (1.5Gb in size)
- Experiments performed for each cognitive state to each individual    members are performed.
- Each experiment either gives cognitive state corresponding to that experiment or the Baseline as its state. 

> ### Test Data:
- 19 Million samples in the test set (4.5 Gb in size)
- Testing is done in simulated training vehicles. 
- Prediction of Cognbitive states based on that data is required. 

**C. ATTRIBUTES OF THIS PROJECT**

This competition makes for a particulary interesting Machine Learning project as it:

1. Has a huge dataset memory size (approx 6Gb), Handling of which is itself a challenging task  
2. Involves raw sensor (signal) data
3. Involves processing time series data
4. Requires feature engineering
5. Is a multiclass classification problem
6. All Ensemble models can be tested and applied for better results. 

The techniques necessary to work with this data are applicable to many other types of Machine Learning problems.

**D. Results**


*   RandomForest Classifier with tuned parameters land us on **Top 26% of Kaggle competition leaderboard** with the score of 0.71248 .

*   Data may vary from person to person therefore we are training and testing the data for each member separately.
   
*   **Randomforest** works well compared to other Ensemble models, Xgboost with little more check on parameters may get equally well, therefore more parameter tuning needs to be done , to decrease our log_loss score         

*   **Handling large data** at once can be cumbersome that is also one of the reasons to create member_ids are created to visualize and process the data.


