# Coding_with_Cvs_consise_notebook
This repository consists of fresh work only
The MCV catalogue and the negatives list sent by Emille have been inquired about with SNAD
Then we proceed with only the observations with no less than 100 points in the light curve(Just to avoid candidates with fewer points which may lead to flat objects)
Then, after understanding the difference correlation matrices, we started training the model with this data
Our model has been trained using 1497 negatives and 128 positives
We have started with 140 positives and 1500 random negatives from the negative list; among them, only the mentioned number of candidates passed, having a minimum of 100 points in light curves
So, we have 1625 objects in total now; during training, we used five random seeds and one seed twice, so we got 6 models.
Newly fetched snad data(Include the FINK observation from 1st January'26 to 2nd March'26)
Then, from this data, we took the objects that have always been flagged as CVs or Unknowns
Then, from this list, we took all CVs and 1200 random unknowns
Then we fetched the light curves from SNAD space and took the observations with a minimum of 100 points in the light curve.
Then this newly fetched dataset was passed through previously saved models.
And we just collected the objects that were predicted  as MCV(as we trained using MCVs) by all 6 models, and again we queried the FINK api to collect their VSX class
