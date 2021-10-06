# Machine Learning Project Checklist


## Frame the problem

This first step is where the objective is defined. Géron refers to objectives in business terms, but this isn't strictly necessary. However, an understanding of how the machine learning system's solution will ultimately be used is important. This step is also where comparable scenarios and current workarounds to a given problem are discussed, as well as assumptions being contemplated, and the degree of need for human expertise determined. Other key technical items to frame in this step include determining which type of machine learning problem (supervised, unsupervised, etc.) applies, and adopting appropriate performance metric(s).

* Create a copy of the data for exploration (sampling it down to a manageable size if necessary).
*  Create a Jupyter notebook to keep a record of your data exploration.
*  Study each attribute and its characteristics:
++ Name
++ Type (categorical, int/float, bounded/unbounded, text, structured, etc.)
 * % of missing values
 * Noisiness and type of noise (stochastic, outliers, rounding errors, etc.)
 * Possibly useful for the task?
 * Type of distribution (Gaussian, uniform, logarithmic, etc.)
* For supervised learning tasks, identify the target attribute(s).
* Visualize the data.
* Study the correlations between attributes.
* Study how you would solve the problem manually.
* Identify the promising transformations you may want to apply.
* Identify extra data that would be useful (go back to “Get the Data” on page 506).
* Document what you have learned.


 
## Get the data

This step is data-centric: determine how much data is needed, what type of data is needed, where to get the data, assess legal obligations surrounding data acquisition... and get the data. Once you have the data, ensure it is appropriately anonymized, make certain you know what type of data it actually is (time series, observations, images, etc.), convert the data to a format you require of it, and create training, validation, and testing sets as warranted.



 
## Explore the data

This step in the checklist is akin to what is often referred to as Exploratory Data Analysis (EDA). The goal is to try and gain insights from the data prior to modeling. Recall that in the first step assumptions about the data were to be identified and explored; this is a good time to more deeply investigate these assumptions. Human experts can be of particular use in this step, answering questions about correlations which may not be obvious to the machine learning practitioner. Studying features and their characteristics is done here, as is general visualization of features and their values (think of how much easier it is, for example, to quickly identify outliers by box plot than by numerical interrogation). Documenting the findings of your exploration for later use is good practice.

* Create a copy of the data for exploration (sampling it down to a manageable size if necessary).
*  Create a Jupyter notebook to keep a record of your data exploration.
*  Study each attribute and its characteristics:
** Name
** Type (categorical, int/float, bounded/unbounded, text, structured, etc.)
** % of missing values
** Noisiness and type of noise (stochastic, outliers, rounding errors, etc.)
** Possibly useful for the task?
** Type of distribution (Gaussian, uniform, logarithmic, etc.)
* For supervised learning tasks, identify the target attribute(s).
* Visualize the data.
* Study the correlations between attributes.
* Study how you would solve the problem manually.
* Identify the promising transformations you may want to apply.
* Identify extra data that would be useful (go back to “Get the Data” on page 506).
* Document what you have learned.

## Prepare the data

Time to apply data transformations you identified as being worthy in the previous step. This step also includes any data cleaning you would perform, as well as both feature selection and engineering. Any feature scaling for value standardization and/or normalization would occur here as well.

 
## Model the data

Time to model the data, and whittle the initial set of models down to what appear to be the most promising bunch. (This is similar to the first modeling step in Chollet's process: good model → "too good" model, which you can read more about here) Such attempts may involve using samples of the full dataset to facilitate training times for preliminary models, models which should cut across a wide spectrum of categories (trees, neural networks, linear, etc.). Models should be built, measured, and compared to one another, and the types of errors made for each model should be investigated, as should the most significant features for each algorithm used. The best performing models should be shortlisted, which can then be fine-tuned afterwards.

 
## Fine-tune the models

The shortlisted models should now have their hyperparameters fine-tuned, and ensemble methods should be investigated at this stage. Full datasets should be used during this step, should dataset samples have been used in the previous modeling phase; no fine-tuned model should be selected as the "winner" without having been exposed to all training data or compared with other models which have also been exposed to all training data. Also, you didn't overfit, right?

 
## Present the solution

Time to present, so hopefully your visualization skills (or those of someone on the implementation team) are up to par! This is a much less technical step, though ensuring proper documentation of the technical aspects of the system at this point is also important. Answer questions for interested parties: Do interested parties understand the big picture? Does the solution achieve the objective? Have you conveyed assumptions and limitations? This is essentially a sales pitch, so ensure the takeaway is confidence in the system. Why do all this work if the result isn't understood and adopted?

*source: Géron, Aurélien
