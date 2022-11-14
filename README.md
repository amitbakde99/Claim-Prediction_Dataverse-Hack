# Dataverse-Hack

Solution Approach (Leaderboard Rank - 175/375)

Problem Statement - To predict if an existing customer of a car insurance company will raise a claim in the upcoming 6 months or not.

Below are the steps taken to find an optimized model for the given classification problem:

After loading the dataset and doing basic exploration, it is noticed that the event(claim raised by a customer) count is around 6%. Further, there are no missing values in the dataset.

From basic EDA, it is found out that there are more categorical and binary features in the dataset compared to the numerical feature. Further, there is no significant linear relationship between any feature and target variable.

The dataset is split into train and validation sets(70:30). The categorical variables are encoded using the label encoder.

Tree-based models generally works well for this type of class imbalance problem. So, the Decision tree is used.

F1 score has been chosen as the evaluation metric as per the contest requirement. But, depending on the business setup, we can either use recall/precision as the evaluation metric. A detailed cost-benefit analysis of acquiring a customer vs claim payment needs to be done to solve the problem.

After getting the optimal hypermeters the model is fitted with the entire training dataset.

F1 score on the validation set is 0.15374.
