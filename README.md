# Novel-method-for-prediction-of-combinatorial-phase-variable-gene-expression-states

Algorithm, input file outlined in "Novel method for prediction of combinatorial phase-variable gene expression states" for the combination of sweep and single colony data, including a script for generating sweep ON (%) data from PSAnalysis. 

**Abstract**

Short sequence repeat mediated phase variation results in diverse phenotype presentation in many bacteria including Campylobacter and Neisseria species. Current methods for identifying the expression states of phase-variable genes involve taking a high number of single colonies. This approach is subject to bias, sampling effects and high workloads that reduce the ability to perform intermediary sampling. The use of high concentration colony sweeps provides a work around but reduces the resolution of combinatorial expression profiles (termed phasotypes). A parsimonious approach combining both single colony and sweep data was developed to overcome these limitations. The critical methodological advance is the use of an algorithm that utilises the experimental data from the two sample types and a parsimonious, iterative mathematical analysis that outputs the phasotype distribution with the highest likelihood of underpinning the experimental data sets. The advantages of this unified method are increased resolution and accuracy of gene expression state combinations as compared to conventional single colony sampling, reduced requirement for sampling large numbers of colonies leading to reduced costs, and a higher capacity for collecting samples and replicates.

•Inputting of sweep and single colony data into an algorithm for a rapid determination of the combinatorial phase variation states (phasotypes) for repeat-mediated phase-variable bacterial genes

•This method reduces the number of single colony samples required to produce accurate estimates of phasotypes

•This method will reduce the costs of phasotype analyses and increase potential to analyse more time points or sample sites leading to an improved understanding of how phase variation contributes to bacterial host persistence and the ability to cause disease



**Installation and requirements**

The .py scripts where written in Python version (3.10) and require no furtehr library or package installation. The scripts were built and developed in Red Hat Enterprise Linux (RHEL) Linux operating system and have also been tested on MAC OS. 

**Use**

The Algorithm for combining sweep and single colony data uses a readme (.csv commer delimintated) file containing the phaso-states of each single colony and a set of ON (%) expression states as below:

```
Gene               ,CapA ,cj1421 ,cj1422
Sweep Data          ,50    ,70  ,40
Single_Colony_1     ,1     ,1   ,1
Single_Colony_2     ,1     ,1   ,0
Single_Colony_3     ,0     ,1   ,0
```


