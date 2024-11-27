## Purpose of this analysis:
Determine columns that were obsolete in this data set and how alterations of binning columns helped improve accuracy of the models.

## What variable(s) are the target(s) for your model?
The target variable is the 'IS_SUCCESSFUL' column from application_df

## What variable(s) are the features for your model?
Everything besides the 'IS_SUCCESSFUL' column

## What variable(s) should be removed from the input data because they are neither targets nor features?
'EIN' and 'NAME' were dropped

# Compiling, Training, and Evaluating the Model

## How many neurons, layers, and activation functions did you select for your neural network model, and why?
I used 80, 30, 10 neurons over three layers. I randomly chose relu, relu, sigmoid based on the first attempt.

## Were you able to achieve the target model performance?
Yes it ended up returning an accurancy of .7595 which was right above the .75 mark.

## What steps did you take in your attempts to increase model performance?
I kept the same amount of neurons, with addition to the 10 on a third layer. 
I only dropped 'EIN' and kept 'NAME' and binned name for those under 100 to be replaced as 'other'.

## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
My original model returned Accuracy: 0.7292128205299377 and the optmized one returned Accuracy: 0.7595335245132446.
To achieve a more accurate return I'd recommend consolidating binning more of the data and increasing the neurons and layers. I'd run it again without both EIN and NAME and let it run against just application type and classificaiton. With more consolidated data and less columns it can better analyze a consolidated chunk of data.
