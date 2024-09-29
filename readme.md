# SYNTHETIC  DATA  GENERATION  WITH  DIFFERENTIAL  PRIVACYVIA  BAYESIAN  NETWORKS
Given a dataset, we try to create a synthetic dataset by making it differentially private using bayesian networks to get low dimension distributions and then getting noisy  conditional probabilities, which produces approximated bayesian network the synthetic dataset that we wanted to create for the release to the public. 
# Assumptions for the Input Dataset
1. The input dataset is a table in first normal form ([1NF](https://en.wikipedia.org/wiki/First_normal_form)).
2. When implementing differential privacy, DataSynthesizer injects noises into the statistics within **active domain** that are the values presented in the table.
# Methodology
- For a given dataset we first gets done with preprocessing it to get it into the required format(as mentioned in abstract attribute form) 
- Preprocessing involves-Making data into categorical and making it numerical which is named as encoded data which has attributes with bins as their numerical values first the data is made categorical (numerical data with values with over a range are categorized into ranges and given nubering starting from 0(bins) to the range sets ) all the missing and nan of a particular attribute are assigned with a bin number nxt to the last one of the attribute.(eg.age has attributes as [0,9],[10,18].....and the categories and are numerised as [0,1,2...] (bins)).
-After preprocessing the data by infering the details of the number of tumples,num of attributes.....etc the privbayes algo is started where the bayesian network(N) is created.
- Now using this network and the description file(saved in json format) is used to create synthetic data in the DataGenerator.
-Sampling is done in the data generator and is saved to synthetic data file.
# Output
- The synthetic data is generated and description file is also generated which is saved during datadescriber.
# Installation:

- Before running the file it is important for you to install the following libraries for smooth functioning of the code file:
  - pandas
  - numpy
  - scipy 
  - matplotlib
  - json
  - math (pre-installed)
  - random (pre-installed)
  -And also the one mentioned in the first cell of the code.

- You can install the above libraries using the following command
``` 
pip install library_name 
```
or (if you use `anaconda`)
``` 
conda install library_name 
```
- Also, make sure that you have `GPU` working on your computer with jupyter notebook, since the code would not be able to run without `GPU`.

# Running the file

- If you have `GPU` connected with your jupyter notebook, then just open the .ipynb file and run its cells. You have to put the dataset in the same folder as the code file. (`-or-` you can yourself check some of the paths in the code and organize the files as you like)
- If you don't have `GPU` connected with your jupyter notebook, then you can upload the code file to `google colab` and then select the `GPU` in the runtime options and then run the code. Before running the file, upload the dataset file using the upload option of google colab.
 

# Note
Use your own dataset(in csv format) and convert it into the required format(description file in json format) and pass as original_data attribute in the functions given in the code.

# Resources:
- Link to the original research paper:https://journalprivacyconfidentiality.org/index.php/jpc/article/view/776/723
- And some Insights from the work(research paper and code) of Zhang J, Cormode G, Procopiuc CM, Srivastava D, Xiao X on PrivBayes: Private Data Release via Bayesian Network.

