# Evaluating the accuracy of equivalent-source predictions using cross-validation

[Leonardo Uieda](https://www.leouieda.com/)<sup>1</sup> and
[Santiago Soler](https://santisoler.github.io/)<sup>2,3</sup>

> <sup>1</sup>Department of Earth, Ocean and Ecological Sciences, School of Environmental Sciences, University of Liverpool, UK<br>
> <sup>2</sup>CONICET, Argentina<br>
> <sup>3</sup>Instituto Geofísico Sismológico Volponi, Universidad Nacional de San Juan, Argentina<br>

Abstract submitted to the EGU2020 General Assembly.

|        |Info|
|-------:|:---|
|Session |TBD|
|Abstract|TBD|
|When    |TBD|
|Where   |TBD|
|Download|doi:TBD|


## Abstract

We investigate the use of cross-validation (CV) techniques to estimate the
accuracy of equivalent-source (also known as equivalent-layer) models for
interpolation and processing of potential-field data.
Our preliminary results indicate that some common CV algorithms (e.g., random
permutations and k-folds) tend to overestimate the accuracy.
We have found that blocked CV methods, where the data are split along spatial
blocks instead of randomly, provide more conservative accuracy estimates.
Beyond evaluating an equivalent-source model's performance, cross-validation
can be used to automatically determine configuration parameters, like source
depth and amount of regularization, that maximize prediction accuracy and avoid
over-fitting.

Widely used in gravity and magnetic data processing,
the equivalent-source technique consists of a linear model (usually point
sources) used to predict the observed field at arbitrary locations.
Upward-continuation, interpolation, gradient calculations, leveling, and
reduction-to-the-pole can be be done, even simultaneously, by using the model
to make predictions (i.e., a forward modelling operation).
The main challenges in applying equivalent-source processing in practice are
the heavy computational load of fitting the model and its sensitivity to
configuration parameters, mainly the source depth and regularization parameter.

These objectives and challenges are shared with the many types of regression
methods in machine learning (ML).
The predictive performance of ML models is usually evaluated through
cross-validation, in which the data are split (usually randomly) into a
training set and a validation set.
Models are fit on the training set and their predictions are evaluated using
the validation set using a goodness-of-fit metric (e.g., mean square error).
Prior research from the statistical modelling of ecological data suggests that
prediction accuracy is usually overestimated when the data are spatially
auto-correlated.
This issue can be mitigated by splitting the data along spatial blocks
rather than randomly.
Indeed, we obtain more conservative accuracy estimates when applying blocked
versions of random permutations and k-fold to synthetic data.

The equivalent-source method used in this study is implemented in the
open-source Python software
Implementations of blocked CV and equivalent-source methods are


## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img
alt="Creative Commons License" style="border-width:0"
src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br>
This content is licensed under a <a rel="license"
href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution
4.0 International License</a>.
