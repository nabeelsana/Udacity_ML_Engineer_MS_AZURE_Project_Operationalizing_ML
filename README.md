## Project Title: Operationalizing Machine Leaning Pipeline

As part of Udacity Machine Learning with Microsoft Azure Nano Degree program, we have to submit thus project to demonstrate operationalizing of Machine Learning pipeline. 

We have performed two experiments: 

i) Creating and operationalizing a pipeline using AutoML and Studio interface

ii) Creating and operationalizing a pipeline using Python SDK interface.

We then published best models obtained. Publishing the model provided a REST endpoint and primary key which enables usto rerun the pipeline using HTTP library. 

We then consumed model using Swagger service. Once the model was deployed we used a python script to interact with the endpoint using a python script by providing URI and primary key. Model end point returned output in expected format so we were sure that our deployment was successful.


##Future improvement in the project

We can suggest following improvments that may result in better model or faster model deployment: 

i) Use more powerful computer cluster such as GPU instanced with more nodes. This may enable increase in concurrent iterations.

ii) Data has class imbalance with many more rejections then approvals. We might address it by procuring more data. 

iii) We need to assess Classifiers that AutoML has not tested and hyperparameters that are not configured. We might further wish to train our data  using those model and parameters by using hyperdrive run and experiment with a different set of parameters.



## Screen Recording
[Link to Screen Cast on Youtube!](https://www.youtube.com/watch?v=D8KvGWe-mns)


## Architectural Diagram

EXPERIMENT 1: PIPELINE AUTOMATION USING AUTOMATED ML AND STUDIO INTERFACE 

![PLA](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/1.PNG)


EXPERIMENT 2: PIPELINE AUTOMATION USING AZURE SDK
![PLA2](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/2.PNG)

## Key Steps

Experiment 1: PIPELINE AUTOMATION USING AUTOMATED ML AND STUDIO INTERFACE

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/3.PNG)

We used Studio inteface and ran AutoML to train models on bank marketing data set. We have shown that data set was registered. 
Once the experiment run completed, we viewed the Details tab, this tab had detail of best model trained. In this case it was 
VotingEnsemble with 94.7% score of AUC_Weighted metric.  Next few screen shots show these steps with headings

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/4.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/5.PNG)

In the next step, We selected best model and deployed it using Azure Container Instance with Authentication enabled. 
However we kept Application Insight disabled. As will be enable it in next step.

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/6.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/7.PNG)

In order to enable Application Insight service we downloaded Config.Json file into local directory. This file is available from 
Studio. We then used script logs.py which executed command to enable Application Insight. We ran it using GitBash facility.
Once it ran successfully it generated logs. We view in the studio interface to confirm that Application Insight was enabled.
In the screen shot below, there is Application Insight link and we have also include screen shot to show how it looks.

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/8.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/9.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/10.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/11.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/12.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/13.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/14.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/15.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/16.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/17.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/18.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/19.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/20.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/21.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/22.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/24.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/25.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/26.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/27.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/28.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/29.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/30.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/31.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/32.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/33.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/34.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/35.PNG)

![](https://github.com/nabeelsana/Udacity_ML_Engineer_MS_AZURE_Project_Operationalizing_ML/blob/master/starter_files/36.PNG)
