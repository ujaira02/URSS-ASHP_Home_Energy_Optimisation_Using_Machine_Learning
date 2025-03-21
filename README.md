# URSS - Home Energy Optimisation: Enhancing Heat Pump Efficiency Through Data-Driven Insights
The Department for Energy Security and Net Zero (DESNZ) has launched the "Electrification of Heat" project to decarbonise domestic heating through air-source heat pumps (ASHPs). This study uses DESNZ and Energy Systems Catapult datasets and Python scientific computing methodologies to develop machine-learning models that predict ASHP energy consumption, efficiency, and cost savings. The goal is to support informed decisions by policymakers, consumers, and energy providers, ultimately reducing electricity costs and carbon emissions in UK households.

### Acknowledgements
Dr Peter Brommer<br>
Warwick Centre for Predictive Modelling<br>
School of Engineering<br>
The University of Warwick

### Download Training Dataset
To download the training dataset from the Department for Energy Security and Net Zero, please go to https://beta.ukdataservice.ac.uk/datacatalogue/studies/study?id=9050#!/access-data and download the two largest CSV files under "**Access Data**". These files should be called:
* "**9050csv_cleansed_data_set1_b693745c14a63a7ed1c6299c5abe1a19**"
* "**9050csv_cleansed_data_set2_130a6915e7f8a17bb83efabdbdb7ec87**". 

Once the files from this repository are also downloaded, move the entire contents of both **9050csv_cleansed_data_...** files into the "**TrainingData**" folder, found in this repository's "**Data**" folder. 

Now open the terminal and use commands to direct yourself to the location of the downloaded "**TrainingData**" folder.

```
(ls -1 | grep -v "^PropertyIds.csv$" | sort | awk 'BEGIN {print "property_id"} {print $0}' > PropertyIds.csv)
```

This code edits the file "**PropertyIds.csv**" within "**TrainingData**", to input all the filenames of the training data properties under the column "**property_id**". For example, the first file may be called "**Property_ID=EOH0001.csv**", so that should be the first entry under "**property_id**".

### How It Works
Once all the files are downloaded, the "**Model.ipynb**" file can be accessed and run. This Jupyter Notebook contains all the necessary instructions within. It is recommended that **Anaconda-Navigator** is used to access the notebook, however if the Python language, jupyter-lab package, and other accompanying packages are already installed on the machine the following terminal code may be used to access "**JupyterLab**" to run the notebook.

```
jupyter-lab
```
<br>
<br>
<br>

_To submit questions or queries, or to receive the model analysis code, please feel free to reach out directly._
