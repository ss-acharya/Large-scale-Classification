# Large-scale-Classification

## Background 

Vaccine Adverse Event Reporting System (VAERS) is a national early warning system to detect possible safety problems in U.S.-licensed vaccines (https://vaers.hhs.gov/index.html). Anyone after receiving a vaccination can report an adverse event to VAERS. Healthcare professionals are required to report certain adverse events and vaccine manufacturers are required to report all adverse events that come to their attention. VAERS data is textual. It is, for analysis purposes, translated into an exhaustive set of discrete MedDRA codes (https://www.meddra.org/). The analysts use the MedDRA non-mutually-exclusive categorizations to summarize the vaccine recipient responses to initiate actions for safety, etc.


## Problem Statement

Identify all symptoms from the textual survey responses of Covid vaccine recipients. For example, a response such as “Got vaccine yesterday. Feeling dizzy and anxious. Feverish?” may be ideally inferred to have the symptoms (a) anxiety (b) dizziness (c) fever.


## Methods

The representative dataset with textual response of the vaccine recipients is used for model development. An exhaustive set of symptoms corresponding to each textual response coded using MedDRA framework is provided by the expert coders. The textual responses were vectorized using BERT. A logistic regression model for each symptom code (with enough responses) was undertaken. The data was divided into test and train subsets. The model was developed on the training subset. Standard metrics of model performance on the test data were generated for evaluation. 


## Results

Excellent model performance was observed based on standard metrics for symptom codes with number of positive records over the threshold (i.e., 100). The model performance was repeatable across different samples, and generalized well.


## Summary

The models were developed towards deployment in a specific situation requiring immediate analysis without heavy dependence on expert coders. The models hold promise for deployment to enable expedited analysis for initiating initial action. For symptom codes with fewer than threshold records, a weekly perusal of the record count was advised enabling new model development as records became available.


## Discussion

E-mail: sankarshansacharya@gmail.com

Project Link: [https://github.com/ss-acharya/large-scale-classification](https://github.com/ss-acharya/large-scale-classification)
