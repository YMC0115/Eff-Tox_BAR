# About this document
This document serves as a brief guide for the use of the R analysis program included in the study "Bayesian phase II adaptive randomization by jointly modeling efficacy and toxicity as time-to-event outcomes".

# The brief guide to use the R code
The document folder Eff-Tox_BAR.zip contains 5 R functions "runtrial.r, modelsparameter.r, function.r, trial.r, cat.r" and a result document.
In the runtrial.r, you need to give a setting as follows:
1. w=1000;                  #number of simulation(1000)
2. run=2500;burnin=500;     #number iterations and burnin in the MCMC procedure   
3. fn="bivariate";          #bivariate (parameters in the model of Efficacy and Toxicity),sensitivity1-2,vague,informative
4. scenario=1;              #bivariate:1-6,sensitivity1:1-4, sensitivity2:1-4,vague:1-4,informative:1-4 
5. file path, for example, path = file.path('D:/Rcode/Eff-Tox_BAR')
 
After running the function EffTox in runtrial.r, the results will be displayed in a result.txt file. The results contain the following:
1. Scenario: the scenario name and number;
2. Time Spend: the amount of time spent for each treatment group;
3. #of pts: the number of patients who are assigned to the ith arm and classified as bad and good prognostic group after follow-up, i=  1,2,3;
4. #of TOX: the number of pts who experience drug toxicity
5. #of EFF: the number of pts who experience drug efficacy  
6. selection prob: the selection probability of each arm
7. selection prob(0.025): Lower 95% creditable set (CI) of the selection probability
8. selection prob(0.975): Upper 95% creditable set (CI) of the selection probability
