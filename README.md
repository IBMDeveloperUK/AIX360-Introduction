# Explaining Machine Learning Models

## Details 
In many applications, trust in an AI system will come from its ability to ‘explain itself.’ But when it comes to understanding and explaining the inner workings of an algorithm, one size does not fit all. Different stakeholders require explanations for different purposes and objectives, and explanations must be tailored to their needs. While a regulator will aim to understand the system as a whole and probe into its logic, consumers affected by a specific decision will be interested only in factors impacting their case – for example, in a loan processing application, they will expect an explanation for why the request was denied and want to understand what changes could lead to approval.

AI Explainability 360 (AIX360) is an open source toolkit that includes algorithms that span the different dimensions of ways of explaining along with proxy explainability metrics.

In this workshop you will explore different kinds of explanations suited to different users. You will learn:

- how to build several machine learning models
- how to evaluate these models and their output

## Getting Started with Jupyter Notebooks

Jupyter notebooks are an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and explanatory text.

In this workshop we will use IBM Watson Studio to run a notebook. For this you will need an IBM Cloud account. The following steps will show you how sign up and get started. When you have the notebook up and running we will go through the notebook.

## IBM Cloud

- Go to your [IBM Cloud account](http://ibm.biz/explainai_mg) or [sign up](http://ibm.biz/explainai_mg)

1. When you have used Watson Studio before, you can skip the next few steps. Go straight to the Resources list and click on Watson Studio and then click on `Get Started`. This will open a new Tab with Cloud Pak For Data that includes Watson Studio.

2. When you have just created an account, click `Create Resource` at the top of the Resources page. You can find the resources under the hamburger menu at the top left:

  ![](https://github.com/IBMDeveloperUK/python-geopandas-workshop/blob/master/images/Create_resource.png)

  - Search for Watson Studio and click on the tile:

  ![](https://github.com/IBMDeveloperUK/jupyter-notebooks-101/blob/master/images/studio.png)

  - Select the Lite plan and click `Create`.
  - Go back to the Resources list and click on your Watson Studio service and then click `Get Started`. This will open a new Tab with Cloud Pak For Data that includes Watson Studio.

  ![](https://github.com/IBMDeveloperUK/jupyter-notebooks-101/blob/master/images/launch.png)

## IBM Watson Studio

### 1. Create a new Project

- You should now be in Watson Studio.
- Create a new project by clicking on `Get Started` and `New Project`, or `Create Project`
- Give your Project a name.
1. If you have used Watson Studio before you can select an Object Storage from the drop-down menu
2. If this is your first time using Watson Studio you have to create Object Storagefor free that is used to store the notebooks and data. Follow the instructions and **do not forget to click refresh when returning to the Project page.**
- click `Create`.  


### 2. Load and run a notebook

- Within the new project now add a new notebook. Click `Add to project` and choose `Notebook`:

![](https://github.com/IBMDeveloperUK/python-geopandas-workshop/blob/master/images/notebook.png)

- Choose new notebook `From URL`. Give your notebook a name and copy the URL `https://github.com/IBMDeveloperUK/AIX360-workshop/blob/master/notebooks/aix360-workshop.ipynb`
- Select the `Default Python 3.6 XS` enviroment and click `Create Notebook`.
- The notebook will load.

You are now ready to follow along with the workshop in the notebook!

### 3. Load and run a second notebook

1. Data
- To run this notebook you will need to download [this data](https://community.fico.com/s/explainable-machine-learning-challenge?tabset-3158a=2) first
- Then go to the `Assets` tab of your project
- Click on `Add to project` at the top of the page and click `Data`
- On the right of the screen you can now upload the file `heloc_dataset.csv` to your project. If your downloaded file has a different name, first change it to `heloc_dataset.csv`
2. Access token
- The second thing that is needed is an `access token` to access the file from a notebook
- Go to the `Settings` tab from the project page and scroll down to `Access tokens`
- Click on `New token` and click create. The name is not important
3. Stop kernel
- Go to your project page and click on the `Environments` tab at the top
- Check if there is an active runtime. If there is click on the 3 dots at the right of the name and click 'Stop'
- Now you can run a different notebook as within a free account you can only run one notebook at a time
- As above, click `Add to project` and choose `Notebook`
- Choose new notebook `From URL`. Give your notebook a name and copy the URL `https://github.com/IBMDeveloperUK/AIX360-workshop/blob/master/notebooks/HELOC-watson-studio.ipynb`
- Select the `Default Python 3.6 XS` enviroment and click `Create Notebook`.
- The notebook will load and you are now ready to follow along


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
