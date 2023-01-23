

**HI!CKATHON 2023**

1/15.2023

# I.	OVERVIEW
## 1.	Project Background and Description
	Describe how this project came about, and the purpose.
The motivation behind this project was to help to alleviate the pain points experienced by owners of real state regarding their energy consumption and the lack of understanding around the subject.

The main points identified were: the lack of understanding about the energy consumption performance, the lack of understanding about the levers that can improve that performance, and the inability to identify the most cost efficient improvements for energy efficiency. In order to mitigate these pain points, the first step was to create a ML solution that serves to predict the performance and identify the key factors impacting performance. The vision is to develop a new app that will leverage the ML predictions, in order to provide a recomendation on the best ecological investments.

## 2.	Project Scope
	Scope answers questions including what will be done, what won’t be done, and what the result will look like.
The scope includes:
- Data Cleaning: ensuring NA columns and other columns are cleaned, and outliers are removed.
- Data Exploration: having an initial understanding of the data and its relationships by making graphics to visualize the variables. 
- Feature Engineering: processing of variables (qualitative and quantitative) to make them usable by the model.
- Model Building, Training: testing of different models (linear regression, regression tree, XGBoost).
- Model Evaluation: evaluation of the model by cross validation, according to the explained variance score.
- Model explainability: studying  the importance of the variables as well as their impact on the energy consumption (in particular thanks to the Shapely values)

The result will look like an explainable model that allows us to determine the main factors that influence energy consumption based on the data we have available. This model will enable us to highlight possible action levers to limit energy consumption.

## 3.	Presentation of the group
	Include your specialization at school, etc.

| First name | Last name | Year of studies & Profile | School   | Skills   | Roles/Tasks    | 
| ---------- | --------- | ------------------------- | ---------| ------   | -----------    | 
| Loris      | Bulliard  | BAC+5 /                   | ENSAE    | Python   | Data Scientist | 
| Eva        | Clergue   | BAC+5 /                   | IP Paris | Python   | Data Scientist | 
| Camille    | Langlois  | BAC+5 /                   | ENSAE    | Python   | Data Scientist | 
| Sophie     | Normand   | BAC+5 /                   | IP Paris | Py+Video | Data + Video   | 
| Jorge      | Ramirez   | BAC+5 /                   | HEC Paris| Business | Pitch          |


## 4.	Task Management
	Describe how you interacted and collaborated as a team, and the effect of every member’s unique background on the project.
Our team colaborated in different ways:
- Through a work plan discussed at the beggining of the exercise with key activities. Moreover, daily touchpoints were executed through the day.
- Technical coordination of activities took place thanks to code integration via GitLAB

Every member had a key role in this project, thanks to the different expertise of the group members. The more technical profiles were able to set up the ML model and feed the business aspect of the project with the results obtained. The more business-oriented profiles were more in charge of the pitch, all in close collaboration with each member of the group.
We also wanted to make a video by filming some scenes and editing them thanks to the artistic qualities of some members of the group.


# II.	PROJECT MANAGEMENT
## 1.	Data Understanding
 	Provided the initial collection of data has already occurred, this step includes identifying and defining the relevant data, exploring the range, scale, formats, contents, and biases of the data, and evaluating the quality and validity of the resulting data.
This step was carried out in particular with the help of our knowledge of the subject. This expertise allowed us to approach the data set with a critical eye. We also made graphics and correlation study in order to understand the behavior of some variables, to study their value ranges and thus to determine if some data were outliers.

## 2.	Data Pre-processing
 	Explain how the selection of data was manipulated and modified to remove redundant features and improve the quality of the data. Describe the preprocessing techniques used, such as data augmentation.
Each variable was studied to understand its meaning and specificity. Thus, by looking at the modalities of each, we were able to eliminate redundant variables. We also focused on the variables that made the most sense from a business perspective.

Then we filled in the missing data thanks to different techniques depending on the variable (replacement by the average, by 0 or by the most frequent modality for instance).
The categorical variables were one-hot-encoded or transformed into ordinal variables.

## 3.	Modeling Development
 	Describe how you selected algorithms, how you calibrated them according to the data and how - in fine - you selected the best AI model using a well-defined set of metrics.
We chose relatively explainable models (linear regression, regression trees), because this is important from a business point of view. Indeed, we prefer to favour highly explainable models, even if it means that the performance might be lower. We have also tried non-explainable models (such as XGBoost) and we have added a layer of explainability using Shapely values. Each model was carefully fine-tuned using a gridsearch in order to select the parameters that best fit the data.
Finally, we selected the model with the best results according to the explained variance score.

## 4.	 Deployment Strategy
 	What best practices/norms did you follow? How do you plan on deploying your IA solution?
We followed the best practice structure for data science projects, but each step would need to be further developed before deploying our solution. 
We tried to respect some standards related to development, but the code should be more standardized.

# III.	CARBON FOOTPRINT LIMITATION
 	Describe the taken measures/actions during the development of your solution in view of limiting the carbon footprint.
Since the solution is intended for a user application, we need a highly explainable model.
We therefore spent a lot of time on variable selection and trained models that do not require exaggerated computational power (by using neural networks for instance, or by doing too much grisearch).

# IV.	CONCLUSION
 	Tell us about the actual results, their limitations as well as future perspectives and improvements.
Our solution allows us to determine the factors that impact (negatively or positively) the energy consumption (since our model is highly explainable).
We have noticed that the altitude, the conductivity of the exterior wall and the conductivity of the ground are factors that positively impact the energy consumption (on average, the higher the building is located, the higher the energy consumption). Other variables such as the surface of the building as well as the percentage of the glazed surface seem to impact the energy consumption in a negative way. 

The limitations of our solution lie mainly in the lack of performance of the model. This is due to a lack of deepening on the different steps preceding the training of the model, and also to the choice of the model which we wanted to be explainable, we thus had to make a compromise and preferred a less powerful but strongly explainable model. 

The future perspectives of the project would be to spend more time on data cleaning, variable selection, and also to fine tune the trained models in order to improve the obtained performance. 
