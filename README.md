# [Inferences about population dynamics from count data using multistate models: a comparison to capture-recapture approaches]
(https://onlinelibrary.wiley.com/doi/full/10.1002/ece3.942)

### Elise F. Zipkin, T. Scott Sillett, Evan H. Campbell Grant, Richard B. Chandler, J. Andrew Royle 

### Ecology and Evolution

### Please contact the first author for questions about the code or data: Elise F. Zipkin (ezipkin@msu.edu)
________________________________________________________________________________________________________________________________________

## Abstract ##
Wildlife populations consist of individuals that contribute disproportionately to growth and viability. Understanding a population's spatial and temporal dynamics requires estimates of abundance and demographic rates that account for this heterogeneity. Estimating these quantities can be difficult, requiring years of intensive data collection. Often, this is accomplished through the capture and recapture of individual animals, which is generally only feasible at a limited number of locations. In contrast, N-mixture models allow for the estimation of abundance, and spatial variation in abundance, from count data alone. We extend recently developed multistate, open population N-mixture models, which can additionally estimate demographic rates based on an organism's life history characteristics. In our extension, we develop an approach to account for the case where not all individuals can be assigned to a state during sampling. Using only state-specific count data, we show how our model can be used to estimate local population abundance, as well as density-dependent recruitment rates and state-specific survival. We apply our model to a population of black-throated blue warblers (Setophaga caerulescens) that have been surveyed for 25 years on their breeding grounds at the Hubbard Brook Experimental Forest in New Hampshire, USA. The intensive data collection efforts allow us to compare our estimates to estimates derived from capture–recapture data. Our model performed well in estimating population abundance and density-dependent rates of annual recruitment/immigration. Estimates of local carrying capacity and per capita recruitment of yearlings were consistent with those published in other studies. However, our model moderately underestimated annual survival probability of yearling and adult females and severely underestimates survival probabilities for both of these male stages. The most accurate and precise estimates will necessarily require some amount of intensive data collection efforts (such as capture–recapture). Integrated population models that combine data from both intensive and extensive sources are likely to be the most efficient approach for estimating demographic rates at large spatial and temporal scales.

## Data
The count data are summarized from capture-recapure data at Hubard Brook from 1998-2010 by Scott sillett.

female.csv - Female warbler counts (yearling, older, unknow) from 1996-2010, with an annual sampling events in up to three elevations
male.csv - Male warbler counts (yearling, older, unknow) from 1996-2010, with an annual sampling events in up to three elevations

## Code
The warbler model is a 2-stage (yearling and adult), 2 sex model. 

Wrapper_warbler.R - Start with this file. The code loads and formats warbler count data and then fits a structured Dail-Madsen model using the associated JAGS code "warbler.R". The code produces a summary of the parameter estimates for the model and model diagnostics (e.g., traceplots and R-hat statisic).

Summarize and plot results.R - Examines results from the model and creates a plot of the posterior distribution of parameter estimates similar to the one in Figure 3.
