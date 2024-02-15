# Novel-method-for-prediction-of-combinatorial-phase-variable-gene-expression-states

Algorithm, input file outlined in "Novel method for prediction of combinatorial phase-variable gene expression states" for the combination of sweep and single colony data, including a script for generating sweep ON (%) data from PSAnalyse. 

**Abstract**

Short sequence repeat mediated phase variation results in diverse phenotype presentation in many bacteria including Campylobacter and Neisseria species. Current methods for identifying the expression states of phase-variable genes involve taking a high number of single colonies. This approach is subject to bias, sampling effects and high workloads that reduce the ability to perform intermediary sampling. The use of high concentration colony sweeps provides a work around but reduces the resolution of combinatorial expression profiles (termed phasotypes). A parsimonious approach combining both single colony and sweep data was developed to overcome these limitations. The critical methodological advance is the use of an algorithm that utilises the experimental data from the two sample types and a parsimonious, iterative mathematical analysis that outputs the phasotype distribution with the highest likelihood of underpinning the experimental data sets. The advantages of this unified method are increased resolution and accuracy of gene expression state combinations as compared to conventional single colony sampling, reduced requirement for sampling large numbers of colonies leading to reduced costs, and a higher capacity for collecting samples and replicates.

•Inputting of sweep and single colony data into an algorithm for a rapid determination of the combinatorial phase variation states (phasotypes) for repeat-mediated phase-variable bacterial genes

•This method reduces the number of single colony samples required to produce accurate estimates of phasotypes

•This method will reduce the costs of phasotype analyses and increase potential to analyse more time points or sample sites leading to an improved understanding of how phase variation contributes to bacterial host persistence and the ability to cause disease



**Algorithm Installation and requirements**

The .py scripts where written in Python version (3.10) and require no further library or package installation. The scripts were built and developed in Red Hat Enterprise Linux (RHEL) Linux operating system and have also been tested on MAC OS. 

**Algorithm use**

The Algorithm for combining sweep and single colony data uses an input (.csv comma delimited) file containing the phaso-states of each single colony and a set of ON (%) - see * *"Example_Input.csv"* *: 

**Step 1)** 
Assemble input file containing single colony and sweep data. 

```
Gene               ,CapA ,cj1421 ,cj1422
Sweep Data          ,50    ,70  ,40
Single_Colony_1     ,1     ,1   ,1
Single_Colony_2     ,1     ,1   ,0
Single_Colony_3     ,0     ,1   ,0
```
**Step 2)** 

Directly run the algorithm (* *"Algorithm_V1.1.py"* *) on the input file (* *"Example_Input.csv"* *)
```
python3 Algorithm_V1.1.py path_to_directory/Example_Input.csv

```

**Further Scripts**

Included in this repository is a script aimed at autogenerating ON (%) data, this can be highly time consuming to generate by hand - even with tools such as PSAnalyse as ON % data was not a focus of previous experiments. This script take a PSAnalyse output file (https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0159634) and outputs the ON state for each GeneScan sample while correcting for slippage (which can be done on single colony data following step 2 in https://methods-x.com/article/S2215-0161(23)00388-6/fulltext#seccesectitle0013).

**Step 1)** 
The .py scripts where written in Python version (3.10) and require no further library or package installation.

To run simply call the script in python with the PSAnalyse file:

```
python3 Gene_ON_State.py path_to_directory/Example_Input.csv

```
To adjust the slippage rates and gene ON length data, edit within the script the dictionaries: track data (state) and prev_slip (state) and post_slip(state). 

The output file is autogenerated using the path and name of the input file. 
















