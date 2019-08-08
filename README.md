# ainights-automatedml
AI nights Automated Machine Learning train-the-trainer content

Automated machine learning (automated ML) builds high quality machine learning models for you by automating model and hyperparameter selection. Bring a labelled dataset that you want to build a model for, automated ML will give you a high quality machine learning model that you can use for predictions.

If you are new to Data Science, automated ML will help you get jumpstarted by simplifying machine learning model building. It abstracts you from needing to perform model selection, hyperparameter selection and in one step creates a high quality trained model for you to use.

If you are an experienced data scientist, automated ML will help increase your productivity by intelligently performing the model and hyperparameter selection for your training and generates high quality models much quicker than manually specifying several combinations of the parameters and running training jobs. Automated ML provides visibility and access to all the training jobs and the performance characteristics of the models to help you further tune the pipeline if you desire.

The presentation can be found in this repository [here](https://github.com/amynic/ainights-automatedml/blob/master/Automated%20ML%20-%20AI%20Nights%202019.zip). (.zip file)

To learn more about automated ML, see documentation [here](https://docs.microsoft.com/en-us/azure/machine-learning/service/concept-automated-ml).

Try the sample notebooks [here](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/automated-machine-learning).

## Prerequisites
Azure subscirption and Azure ML workspace. See instructions on how to create a worksapce [here](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-create-portal-experiments).

## Automated ML using Azure Portal UI: Car price prediction

Follow the instructions in the [documentation](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-create-portal-experiments) for a full overview of the user interface.

1. Navigate to the left pane of your workspace. Select Automated Machine Learning under the Authoring (Preview) section.
![Automated ML tab](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/how-to-create-portal-experiments/nav-pane.png)

1. Enter your experiment name, then select a compute from the list of your existing computes or [create a new compute](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-create-portal-experiments#create-an-experiment).

1. Select a data file from your storage container, or upload a file from your local computer to the container.
Car price dataset downloadable from [this location](https://automlpmdemows6960037818.blob.core.windows.net/sample-data/Automobile price data.csv).

1. Preview data and keep all columns selected for training.

1. Select the training job type: **regression**
1. Select target column: **price**

1. Open “**Advanced settings**”, set training job time to 15 minutes (for the workshop).

1. Hit "**Start**" and wait for the training job to start. You’ll be able to see the models which are created during the run, click on any of the models to open the detailed view of that model, where you can analyze the [graphs and metrics](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-understand-automated-ml).

1. Once the run is completed, click **deploy the best model** to create a deployed endpoint from the model.

1. Once deployed, follow [instructions](https://docs.microsoft.com/en-us/power-bi/service-machine-learning-integration) to consume from Power BI.


## Automated ML using Python code in Jupyter Notebook: Energy Demand
Follow the instructions to run automated ML from a Jupyter notebook using Azure ML service Notebook VM. A more comprehensive tutorial can be found [here](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-auto-train-forecast).

1. Open your Machine Learning service workspace and go to "**Notebook VMs**"

1. Create a new Notebook VM following the instructions [here](https://docs.microsoft.com/en-us/azure/machine-learning/service/tutorial-1st-experiment-sdk-setup#azure).
![Create Notebook VM](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/tutorial-1st-experiment-sdk-setup/add-workstation.png)

1. After VM has started (~10mins) click on **Jupyter** to open the Jupyter notebook client.
![Open Notebook VM](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/tutorial-1st-experiment-sdk-setup/start-server.png)

1. Open the energy demand notebook: Click on root folder > Samples-x.x.xx > how-to-use-azureml > automated-machine-learning > forecasting-energy-demand > /auto-ml-forecasting-energy-demand.ipynb

1. Follow instructions in notebook executing each cell.
