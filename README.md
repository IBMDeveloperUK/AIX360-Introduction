# Explaining Machine Learning Models

## Details 
In many applications, trust in an AI system will come from its ability to ‘explain itself.’ But when it comes to understanding and explaining the inner workings of an algorithm, one size does not fit all. Different stakeholders require explanations for different purposes and objectives, and explanations must be tailored to their needs. While a regulator will aim to understand the system as a whole and probe into its logic, consumers affected by a specific decision will be interested only in factors impacting their case – for example, in a loan processing application, they will expect an explanation for why the request was denied and want to understand what changes could lead to approval.

AI Explainability 360 (AIX360) is an open source toolkit that includes algorithms that span the different dimensions of ways of explaining along with proxy explainability metrics.

In this workshop you will explore different kinds of explanations suited to different users in the context of a credit approval process enabled by machine learning. The three types of users that we will look at are a data scientist, who evaluates the machine learning model before deployment, a loan officer, who makes the final decision based on the model's output, and a bank customer, who wants to understand the reasons for their application result.

You will learn:
- how to build several machine learning models, including a simple neural network
- how to evaluate these models and their output

## Getting Started with Jupyter Notebooks

Jupyter notebooks are an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and explanatory text.

In this workshop we will use IBM Watson Studio to run a notebook. For this you will need an IBM Cloud account. The following steps will show you how sign up and get started. When you have the notebook up and running we will go through the notebook.

## IBM Cloud

- Go to your [IBM Cloud account](http://ibm.biz/explainai_mg) or [sign up](http://ibm.biz/explainai_mg)

- When you are signed up click `Create Resource` at the top of the Resources page. You can find the resources under the hamburger menu at the top left:

![](https://github.com/IBMDeveloperUK/python-geopandas-workshop/blob/master/images/Create_resource.png)

- Search for Watson Studio and click on the tile:

![](https://github.com/IBMDeveloperUK/jupyter-notebooks-101/blob/master/images/studio.png)

- Select the Lite plan and click `Create`.
- Go back to the Resources list and click on your Watson Studio service and then click `Get Started`.

![](https://github.com/IBMDeveloperUK/jupyter-notebooks-101/blob/master/images/launch.png)

## IBM Watson Studio

### 1. Create a new Project

- You should now be in Watson Studio.
- Create a new project by clicking on `Get Started` and `New Project`, or `Create Project`
- Give your Project a name.
- Select an Object Storage from the drop-down menu or create a new one for free. This is used to store the notebooks and data. **Do not forget to click refresh when returning to the Project page.**
- click `Create`.  

### 2. Load and run a notebook

- Add a new notebook. Click `Add to project` and choose `Notebook`:

![](https://github.com/IBMDeveloperUK/python-geopandas-workshop/blob/master/images/notebook.png)

- Choose new notebook `From URL`. Give your notebook a name and copy the URL `https://github.com/IBMDeveloperUK/AIX360-workshop/blob/master/notebooks/aix360-workshop.ipynb`
- Select the `Default Python 3.6 XS` enviroment and click `Create Notebook`.
- The notebook will load.

You are now ready to follow along with the workshop in the notebook!

## Optional: Anaconda local install

Optional local install on Mac:

Install [Anaconda](https://docs.anaconda.com/anaconda/install/)

Open terminal and create a new environment:

`> conda create --name aix360 python=3.7`

`> conda activate aix360`

Just in case: `> conda env remove --name aix360`

Or use the environment with all packages you need from the yml file (this one includes probably too many, will need to clean it up):

`> conda env create -f environment.yml`

Add kernel to Jupyter notebooks:

`> python -m ipykernel install --user --name aif360 --display-name "Python37 (aif360)"`

Start notebooks: 
`> jupyter notebook`
