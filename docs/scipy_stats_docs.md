# Statistical functions (scipy.stats)

This module contains a large number of probability distributions, summary and frequency statistics, correlation functions and statistical tests, masked statistics, kernel density estimation, quasi-Monte Carlo functionality, and more.

Statistics is a very large area, and there are topics that are out of scope for SciPy and are covered by other packages. Some of the most important ones are:

statsmodels: regression, linear models, time series analysis, extensions to topics also covered by scipy.stats.

Pandas: tabular data, time series functionality, interfaces to other statistical languages.

PyMC: Bayesian statistical modeling, probabilistic machine learning.

scikit-learn: classification, regression, model selection.

Seaborn: statistical data visualization.

rpy2: Python to R bridge.

## Probability distributions

Each univariate distribution is an instance of a subclass of rv_continuous (rv_discrete for discrete distributions):

rv_continuous([momtype, a, b, xtol, ...])

A generic continuous random variable class meant for subclassing.

rv_discrete([a, b, name, badvalue, ...])

A generic discrete random variable class meant for subclassing.

rv_histogram(histogram, *args[, density])

Generates a distribution given by a histogram.

### Continuous distributions

alpha

An alpha continuous random variable.

anglit

An anglit continuous random variable.

arcsine

An arcsine continuous random variable.

argus

Argus distribution

beta

A beta continuous random variable.

betaprime

A beta prime continuous random variable.

bradford

A Bradford continuous random variable.

burr

A Burr (Type III) continuous random variable.

burr12

A Burr (Type XII) continuous random variable.

cauchy

A Cauchy continuous random variable.

chi

A chi continuous random variable.

chi2

A chi-squared continuous random variable.

cosine

A cosine continuous random variable.

crystalball

Crystalball distribution

dgamma

A double gamma continuous random variable.

dpareto_lognorm

A double Pareto lognormal continuous random variable.

dweibull

A double Weibull continuous random variable.

erlang

An Erlang continuous random variable.

expon

An exponential continuous random variable.

exponnorm

An exponentially modified Normal continuous random variable.

exponweib

An exponentiated Weibull continuous random variable.

exponpow

An exponential power continuous random variable.

f

An F continuous random variable.

fatiguelife

A fatigue-life (Birnbaum-Saunders) continuous random variable.

fisk

A Fisk continuous random variable.

foldcauchy

A folded Cauchy continuous random variable.

foldnorm

A folded normal continuous random variable.

genlogistic

A generalized logistic continuous random variable.

gennorm

A generalized normal continuous random variable.

genpareto

A generalized Pareto continuous random variable.

genexpon

A generalized exponential continuous random variable.

genextreme

A generalized extreme value continuous random variable.

gausshyper

A Gauss hypergeometric continuous random variable.

gamma

A gamma continuous random variable.

gengamma

A generalized gamma continuous random variable.

genhalflogistic

A generalized half-logistic continuous random variable.

genhyperbolic

A generalized hyperbolic continuous random variable.

geninvgauss

A Generalized Inverse Gaussian continuous random variable.

gibrat

A Gibrat continuous random variable.

gompertz

A Gompertz (or truncated Gumbel) continuous random variable.

gumbel_r

A right-skewed Gumbel continuous random variable.

gumbel_l

A left-skewed Gumbel continuous random variable.

halfcauchy

A Half-Cauchy continuous random variable.

halflogistic

A half-logistic continuous random variable.

halfnorm

A half-normal continuous random variable.

halfgennorm

The upper half of a generalized normal continuous random variable.

hypsecant

A hyperbolic secant continuous random variable.

invgamma

An inverted gamma continuous random variable.

invgauss

An inverse Gaussian continuous random variable.

invweibull

An inverted Weibull continuous random variable.

irwinhall

An Irwin-Hall (Uniform Sum) continuous random variable.

jf_skew_t

Jones and Faddy skew-t distribution.

johnsonsb

A Johnson SB continuous random variable.

johnsonsu

A Johnson SU continuous random variable.

kappa4

Kappa 4 parameter distribution.

kappa3

Kappa 3 parameter distribution.

ksone

Kolmogorov-Smirnov one-sided test statistic distribution.

kstwo

Kolmogorov-Smirnov two-sided test statistic distribution.

kstwobign

Limiting distribution of scaled Kolmogorov-Smirnov two-sided test statistic.

landau

A Landau continuous random variable.

laplace

A Laplace continuous random variable.

laplace_asymmetric

An asymmetric Laplace continuous random variable.

levy

A Levy continuous random variable.

levy_l

A left-skewed Levy continuous random variable.

levy_stable

A Levy-stable continuous random variable.

logistic

A logistic (or Sech-squared) continuous random variable.

loggamma

A log gamma continuous random variable.

loglaplace

A log-Laplace continuous random variable.

lognorm

A lognormal continuous random variable.

loguniform

A loguniform or reciprocal continuous random variable.

lomax

A Lomax (Pareto of the second kind) continuous random variable.

maxwell

A Maxwell continuous random variable.

mielke

A Mielke Beta-Kappa / Dagum continuous random variable.

moyal

A Moyal continuous random variable.

nakagami

A Nakagami continuous random variable.

ncx2

A non-central chi-squared continuous random variable.

ncf

A non-central F distribution continuous random variable.

nct

A non-central Student's t continuous random variable.

norm

A normal continuous random variable.

norminvgauss

A Normal Inverse Gaussian continuous random variable.

pareto

A Pareto continuous random variable.

pearson3

A pearson type III continuous random variable.

powerlaw

A power-function continuous random variable.

powerlognorm

A power log-normal continuous random variable.

powernorm

A power normal continuous random variable.

rdist

An R-distributed (symmetric beta) continuous random variable.

rayleigh

A Rayleigh continuous random variable.

rel_breitwigner

A relativistic Breit-Wigner random variable.

rice

A Rice continuous random variable.

recipinvgauss

A reciprocal inverse Gaussian continuous random variable.

semicircular

A semicircular continuous random variable.

skewcauchy

A skewed Cauchy random variable.

skewnorm

A skew-normal random variable.

studentized_range

A studentized range continuous random variable.

t

A Student's t continuous random variable.

trapezoid

A trapezoidal continuous random variable.

triang

A triangular continuous random variable.

truncexpon

A truncated exponential continuous random variable.

truncnorm

A truncated normal continuous random variable.

truncpareto

An upper truncated Pareto continuous random variable.

truncweibull_min

A doubly truncated Weibull minimum continuous random variable.

tukeylambda

A Tukey-Lamdba continuous random variable.

uniform

A uniform continuous random variable.

vonmises

A Von Mises continuous random variable.

vonmises_line

A Von Mises continuous random variable.

wald

A Wald continuous random variable.

weibull_min

Weibull minimum continuous random variable.

weibull_max

Weibull maximum continuous random variable.

wrapcauchy

A wrapped Cauchy continuous random variable.

The fit method of the univariate continuous distributions uses maximum likelihood estimation to fit the distribution to a data set. The fit method can accept regular data or censored data. Censored data is represented with instances of the CensoredData class.

CensoredData([uncensored, left, right, interval])

Instances of this class represent censored data.

### Multivariate distributions

multivariate_normal

A multivariate normal random variable.

matrix_normal

A matrix normal random variable.

dirichlet

A Dirichlet random variable.

dirichlet_multinomial

A Dirichlet multinomial random variable.

wishart

A Wishart random variable.

invwishart

An inverse Wishart random variable.

multinomial

A multinomial random variable.

special_ortho_group

A Special Orthogonal matrix (SO(N)) random variable.

ortho_group

An Orthogonal matrix (O(N)) random variable.

unitary_group

A matrix-valued U(N) random variable.

random_correlation

A random correlation matrix.

multivariate_t

A multivariate t-distributed random variable.

multivariate_hypergeom

A multivariate hypergeometric random variable.

normal_inverse_gamma

Normal-inverse-gamma distribution.

random_table

Contingency tables from independent samples with fixed marginal sums.

uniform_direction

A vector-valued uniform direction.

vonmises_fisher

A von Mises-Fisher variable.

scipy.stats.multivariate_normal methods accept instances of the following class to represent the covariance.

Covariance()

Representation of a covariance matrix

### Discrete distributions

bernoulli

A Bernoulli discrete random variable.

betabinom

A beta-binomial discrete random variable.

betanbinom

A beta-negative-binomial discrete random variable.

binom

A binomial discrete random variable.

boltzmann

A Boltzmann (Truncated Discrete Exponential) random variable.

dlaplace

A Laplacian discrete random variable.

geom

A geometric discrete random variable.

hypergeom

A hypergeometric discrete random variable.

logser

A Logarithmic (Log-Series, Series) discrete random variable.

nbinom

A negative binomial discrete random variable.

nchypergeom_fisher

A Fisher's noncentral hypergeometric discrete random variable.

nchypergeom_wallenius

A Wallenius' noncentral hypergeometric discrete random variable.

nhypergeom

A negative hypergeometric discrete random variable.

planck

A Planck discrete exponential random variable.

poisson

A Poisson discrete random variable.

poisson_binom

A Poisson Binomial discrete random variable.

randint

A uniform discrete random variable.

skellam

A Skellam discrete random variable.

yulesimon

A Yule-Simon discrete random variable.

zipf

A Zipf (Zeta) discrete random variable.

zipfian

A Zipfian discrete random variable.

An overview of statistical functions is given below. Many of these functions have a similar version in scipy.stats.mstats which work for masked arrays.

## Summary statistics

describe(a[, axis, ddof, bias, nan_policy])

Compute several descriptive statistics of the passed array.

gmean(a[, axis, dtype, weights, nan_policy, ...])

Compute the weighted geometric mean along the specified axis.

hmean(a[, axis, dtype, weights, nan_policy, ...])

Calculate the weighted harmonic mean along the specified axis.

pmean(a, p, *[, axis, dtype, weights, ...])

Calculate the weighted power mean along the specified axis.

kurtosis(a[, axis, fisher, bias, ...])

Compute the kurtosis (Fisher or Pearson) of a dataset.

mode(a[, axis, nan_policy, keepdims])

Return an array of the modal (most common) value in the passed array.

moment(a[, order, axis, nan_policy, center, ...])

Calculate the nth moment about the mean for a sample.

lmoment(sample[, order, axis, sorted, ...])

Compute L-moments of a sample from a continuous distribution

expectile(a[, alpha, weights])

Compute the expectile at the specified level.

skew(a[, axis, bias, nan_policy, keepdims])

Compute the sample skewness of a data set.

kstat(data[, n, axis, nan_policy, keepdims])

Return the n th k-statistic ( 1<=n<=4 so far).

kstatvar(data[, n, axis, nan_policy, keepdims])

Return an unbiased estimator of the variance of the k-statistic.

tmean(a[, limits, inclusive, axis, ...])

Compute the trimmed mean.

tvar(a[, limits, inclusive, axis, ddof, ...])

Compute the trimmed variance.

tmin(a[, lowerlimit, axis, inclusive, ...])

Compute the trimmed minimum.

tmax(a[, upperlimit, axis, inclusive, ...])

Compute the trimmed maximum.

tstd(a[, limits, inclusive, axis, ddof, ...])

Compute the trimmed sample standard deviation.

tsem(a[, limits, inclusive, axis, ddof, ...])

Compute the trimmed standard error of the mean.

variation(a[, axis, nan_policy, ddof, keepdims])

Compute the coefficient of variation.

find_repeats(arr)

Find repeats and repeat counts.

rankdata(a[, method, axis, nan_policy])

Assign ranks to data, dealing with ties appropriately.

tiecorrect(rankvals)

Tie correction factor for Mann-Whitney U and Kruskal-Wallis H tests.

trim_mean(a, proportiontocut[, axis])

Return mean of array after trimming a specified fraction of extreme values

gstd(a[, axis, ddof, keepdims, nan_policy])

Calculate the geometric standard deviation of an array.

iqr(x[, axis, rng, scale, nan_policy, ...])

Compute the interquartile range of the data along the specified axis.

sem(a[, axis, ddof, nan_policy, keepdims])

Compute standard error of the mean.

bayes_mvs(data[, alpha])

Bayesian confidence intervals for the mean, var, and std.

mvsdist(data)

'Frozen' distributions for mean, variance, and standard deviation of data.

entropy(pk[, qk, base, axis, nan_policy, ...])

Calculate the Shannon entropy/relative entropy of given distribution(s).

differential_entropy(values, *[, ...])

Given a sample of a distribution, estimate the differential entropy.

median_abs_deviation(x[, axis, center, ...])

Compute the median absolute deviation of the data along the given axis.

## Frequency statistics

cumfreq(a[, numbins, defaultreallimits, weights])

Return a cumulative frequency histogram, using the histogram function.

quantile(x, p, *[, method, axis, ...])

Compute the p-th quantile of the data along the specified axis.

percentileofscore(a, score[, kind, nan_policy])

Compute the percentile rank of a score relative to a list of scores.

scoreatpercentile(a, per[, limit, ...])

Calculate the score at a given percentile of the input sequence.

relfreq(a[, numbins, defaultreallimits, weights])

Return a relative frequency histogram, using the histogram function.

binned_statistic(x, values[, statistic, ...])

Compute a binned statistic for one or more sets of data.

binned_statistic_2d(x, y, values[, ...])

Compute a bidimensional binned statistic for one or more sets of data.

binned_statistic_dd(sample, values[, ...])

Compute a multidimensional binned statistic for a set of data.

## Hypothesis Tests and related functions

SciPy has many functions for performing hypothesis tests that return a test statistic and a p-value, and several of them return confidence intervals and/or other related information.

The headings below are based on common uses of the functions within, but due to the wide variety of statistical procedures, any attempt at coarse-grained categorization will be imperfect. Also, note that tests within the same heading are not interchangeable in general (e.g. many have different distributional assumptions).

One Sample Tests / Paired Sample Tests
One sample tests are typically used to assess whether a single sample was drawn from a specified distribution or a distribution with specified properties (e.g. zero mean).

ttest_1samp(a, popmean[, axis, nan_policy, ...])

Calculate the T-test for the mean of ONE group of scores.

binomtest(k, n[, p, alternative])

Perform a test that the probability of success is p.

quantile_test(x, *[, q, p, alternative])

Perform a quantile test and compute a confidence interval of the quantile.

skewtest(a[, axis, nan_policy, alternative, ...])

Test whether the skew is different from the normal distribution.

kurtosistest(a[, axis, nan_policy, ...])

Test whether a dataset has normal kurtosis.

normaltest(a[, axis, nan_policy, keepdims])

Test whether a sample differs from a normal distribution.

jarque_bera(x, *[, axis, nan_policy, keepdims])

Perform the Jarque-Bera goodness of fit test on sample data.

shapiro(x, *[, axis, nan_policy, keepdims])

Perform the Shapiro-Wilk test for normality.

anderson(x[, dist])

Anderson-Darling test for data coming from a particular distribution.

cramervonmises(rvs, cdf[, args, axis, ...])

Perform the one-sample Cramér-von Mises test for goodness of fit.

ks_1samp(x, cdf[, args, alternative, ...])

Performs the one-sample Kolmogorov-Smirnov test for goodness of fit.

goodness_of_fit(dist, data, *[, ...])

Perform a goodness of fit test comparing data to a distribution family.

chisquare(f_obs[, f_exp, ddof, axis, ...])

Perform Pearson's chi-squared test.

power_divergence(f_obs[, f_exp, ddof, axis, ...])

Cressie-Read power divergence statistic and goodness of fit test.

Paired sample tests are often used to assess whether two samples were drawn from the same distribution; they differ from the independent sample tests below in that each observation in one sample is treated as paired with a closely-related observation in the other sample (e.g. when environmental factors are controlled between observations within a pair but not among pairs). They can also be interpreted or used as one-sample tests (e.g. tests on the mean or median of differences between paired observations).

ttest_rel(a, b[, axis, nan_policy, ...])

Calculate the t-test on TWO RELATED samples of scores, a and b.

wilcoxon(x[, y, zero_method, correction, ...])

Calculate the Wilcoxon signed-rank test.

Association/Correlation Tests
These tests are often used to assess whether there is a relationship (e.g. linear) between paired observations in multiple samples or among the coordinates of multivariate observations.

linregress(x, y[, alternative, axis, ...])

Calculate a linear least-squares regression for two sets of measurements.

pearsonr(x, y, *[, alternative, method, axis])

Pearson correlation coefficient and p-value for testing non-correlation.

spearmanr(a[, b, axis, nan_policy, alternative])

Calculate a Spearman correlation coefficient with associated p-value.

pointbiserialr(x, y, *[, axis, nan_policy, ...])

Calculate a point biserial correlation coefficient and its p-value.

kendalltau(x, y, *[, nan_policy, method, ...])

Calculate Kendall's tau, a correlation measure for ordinal data.

chatterjeexi(x, y, *[, axis, y_continuous, ...])

Compute the xi correlation and perform a test of independence

weightedtau(x, y[, rank, weigher, additive, ...])

Compute a weighted version of Kendall's 
.

somersd(x[, y, alternative])

Calculates Somers' D, an asymmetric measure of ordinal association.

siegelslopes(y[, x, method, axis, ...])

Computes the Siegel estimator for a set of points (x, y).

theilslopes(y[, x, alpha, method, axis, ...])

Computes the Theil-Sen estimator for a set of points (x, y).

page_trend_test(data[, ranked, ...])

Perform Page's Test, a measure of trend in observations between treatments.

multiscale_graphcorr(x, y[, ...])

Computes the Multiscale Graph Correlation (MGC) test statistic.

These association tests and are to work with samples in the form of contingency tables. Supporting functions are available in scipy.stats.contingency.

chi2_contingency(observed[, correction, ...])

Chi-square test of independence of variables in a contingency table.

fisher_exact(table[, alternative, method])

Perform a Fisher exact test on a contingency table.

barnard_exact(table[, alternative, pooled, n])

Perform a Barnard exact test on a 2x2 contingency table.

boschloo_exact(table[, alternative, n])

Perform Boschloo's exact test on a 2x2 contingency table.

Independent Sample Tests
Independent sample tests are typically used to assess whether multiple samples were independently drawn from the same distribution or different distributions with a shared property (e.g. equal means).

Some tests are specifically for comparing two samples.

ttest_ind_from_stats(mean1, std1, nobs1, ...)

T-test for means of two independent samples from descriptive statistics.

poisson_means_test(k1, n1, k2, n2, *[, ...])

Performs the Poisson means test, AKA the "E-test".

ttest_ind(a, b, *[, axis, equal_var, ...])

Calculate the T-test for the means of two independent samples of scores.

mannwhitneyu(x, y[, use_continuity, ...])

Perform the Mann-Whitney U rank test on two independent samples.

bws_test(x, y, *[, alternative, method])

Perform the Baumgartner-Weiss-Schindler test on two independent samples.

ranksums(x, y[, alternative, axis, ...])

Compute the Wilcoxon rank-sum statistic for two samples.

brunnermunzel(x, y[, alternative, ...])

Compute the Brunner-Munzel test on samples x and y.

mood(x, y[, axis, alternative, nan_policy, ...])

Perform Mood's test for equal scale parameters.

ansari(x, y[, alternative, axis, ...])

Perform the Ansari-Bradley test for equal scale parameters.

cramervonmises_2samp(x, y[, method, axis, ...])

Perform the two-sample Cramér-von Mises test for goodness of fit.

epps_singleton_2samp(x, y[, t, axis, ...])

Compute the Epps-Singleton (ES) test statistic.

ks_2samp(data1, data2[, alternative, ...])

Performs the two-sample Kolmogorov-Smirnov test for goodness of fit.

kstest(rvs, cdf[, args, N, alternative, ...])

Performs the (one-sample or two-sample) Kolmogorov-Smirnov test for goodness of fit.

Others are generalized to multiple samples.

f_oneway(*samples[, axis, equal_var, ...])

Perform one-way ANOVA.

tukey_hsd(*args[, equal_var])

Perform Tukey's HSD test for equality of means over multiple treatments.

dunnett(*samples, control[, alternative, ...])

Dunnett's test: multiple comparisons of means against a control group.

kruskal(*samples[, nan_policy, axis, keepdims])

Compute the Kruskal-Wallis H-test for independent samples.

alexandergovern(*samples[, nan_policy, ...])

Performs the Alexander Govern test.

fligner(*samples[, center, proportiontocut, ...])

Perform Fligner-Killeen test for equality of variance.

levene(*samples[, center, proportiontocut, ...])

Perform Levene test for equal variances.

bartlett(*samples[, axis, nan_policy, keepdims])

Perform Bartlett's test for equal variances.

median_test(*samples[, ties, correction, ...])

Perform a Mood's median test.

friedmanchisquare(*samples[, axis, ...])

Compute the Friedman test for repeated samples.

anderson_ksamp(samples[, midrank, method])

The Anderson-Darling test for k-samples.

Resampling and Monte Carlo Methods
The following functions can reproduce the p-value and confidence interval results of most of the functions above, and often produce accurate results in a wider variety of conditions. They can also be used to perform hypothesis tests and generate confidence intervals for custom statistics. This flexibility comes at the cost of greater computational requirements and stochastic results.

monte_carlo_test(data, rvs, statistic, *[, ...])

Perform a Monte Carlo hypothesis test.

permutation_test(data, statistic, *[, ...])

Performs a permutation test of a given statistic on provided data.

bootstrap(data, statistic, *[, n_resamples, ...])

Compute a two-sided bootstrap confidence interval of a statistic.

power(test, rvs, n_observations, *[, ...])

Simulate the power of a hypothesis test under an alternative hypothesis.

Instances of the following object can be passed into some hypothesis test functions to perform a resampling or Monte Carlo version of the hypothesis test.

MonteCarloMethod([n_resamples, batch, rvs, rng])

Configuration information for a Monte Carlo hypothesis test.

PermutationMethod([n_resamples, batch, ...])

Configuration information for a permutation hypothesis test.

BootstrapMethod([n_resamples, batch, ...])

Configuration information for a bootstrap confidence interval.

Multiple Hypothesis Testing and Meta-Analysis
These functions are for assessing the results of individual tests as a whole. Functions for performing specific multiple hypothesis tests (e.g. post hoc tests) are listed above.

combine_pvalues(pvalues[, method, weights, ...])

Combine p-values from independent tests that bear upon the same hypothesis.

false_discovery_control(ps, *[, axis, method])

Adjust p-values to control the false discovery rate.

The following functions are related to the tests above but do not belong in the above categories.

## Random Variables

make_distribution(dist)

Generate a UnivariateDistribution class from a compatible object

Normal([mu, sigma])

Normal distribution with prescribed mean and standard deviation.

Uniform(*[, a, b])

Uniform distribution.

Binomial(*, n, p, **kwargs)

Binomial distribution with prescribed success probability and number of trials

Mixture(components, *[, weights])

Representation of a mixture distribution.

order_statistic(X, /, *, r, n)

Probability distribution of an order statistic

truncate(X[, lb, ub])

Truncate the support of a random variable.

abs(X, /)

Absolute value of a random variable

exp(X, /)

Natural exponential of a random variable

log(X, /)

Natural logarithm of a non-negative random variable

## Other statistical functionality

### Transformations

boxcox(x[, lmbda, alpha, optimizer])

Return a dataset transformed by a Box-Cox power transformation.

boxcox_normmax(x[, brack, method, ...])

Compute optimal Box-Cox transform parameter for input data.

boxcox_llf(lmb, data, *[, axis, keepdims, ...])

The boxcox log-likelihood function.

yeojohnson(x[, lmbda])

Return a dataset transformed by a Yeo-Johnson power transformation.

yeojohnson_normmax(x[, brack])

Compute optimal Yeo-Johnson transform parameter.

yeojohnson_llf(lmb, data)

The yeojohnson log-likelihood function.

obrientransform(*samples)

Compute the O'Brien transform on input data (any number of arrays).

sigmaclip(a[, low, high])

Perform iterative sigma-clipping of array elements.

trimboth(a, proportiontocut[, axis])

Slice off a proportion of items from both ends of an array.

trim1(a, proportiontocut[, tail, axis])

Slice off a proportion from ONE end of the passed array distribution.

zmap(scores, compare[, axis, ddof, nan_policy])

Calculate the relative z-scores.

zscore(a[, axis, ddof, nan_policy])

Compute the z score.

gzscore(a, *[, axis, ddof, nan_policy])

Compute the geometric standard score.

### Statistical distances

wasserstein_distance(u_values, v_values[, ...])

Compute the Wasserstein-1 distance between two 1D discrete distributions.

wasserstein_distance_nd(u_values, v_values)

Compute the Wasserstein-1 distance between two N-D discrete distributions.

energy_distance(u_values, v_values[, ...])

Compute the energy distance between two 1D distributions.

### Sampling

Random Number Generators (scipy.stats.sampling)
Generators Wrapped
For continuous distributions
NumericalInverseHermite
NumericalInversePolynomial
TransformedDensityRejection
SimpleRatioUniforms
RatioUniforms
For discrete distributions
DiscreteAliasUrn
DiscreteGuideTable
Warnings / Errors used in scipy.stats.sampling
scipy.stats.sampling.UNURANError
Generators for pre-defined distributions
FastGeneratorInversion
FastGeneratorInversion
evaluate_error
ppf
qrvs
rvs
support

### Fitting / Survival Analysis

fit(dist, data[, bounds, guess, method, ...])

Fit a discrete or continuous distribution to data

ecdf(sample)

Empirical cumulative distribution function of a sample.

logrank(x, y[, alternative])

Compare the survival distributions of two samples via the logrank test.

### Directional statistical functions

directional_stats(samples, *[, axis, normalize])

Computes sample statistics for directional data.

circmean(samples[, high, low, axis, ...])

Compute the circular mean of a sample of angle observations.

circvar(samples[, high, low, axis, ...])

Compute the circular variance of a sample of angle observations.

circstd(samples[, high, low, axis, ...])

Compute the circular standard deviation of a sample of angle observations.

### Sensitivity Analysis

sobol_indices(*, func, n[, dists, method, ...])

Global sensitivity indices of Sobol'.

### Plot-tests

ppcc_max(x[, brack, dist])

Calculate the shape parameter that maximizes the PPCC.

ppcc_plot(x, a, b[, dist, plot, N])

Calculate and optionally plot probability plot correlation coefficient.

probplot(x[, sparams, dist, fit, plot, rvalue])

Calculate quantiles for a probability plot, and optionally show the plot.

boxcox_normplot(x, la, lb[, plot, N])

Compute parameters for a Box-Cox normality plot, optionally show it.

yeojohnson_normplot(x, la, lb[, plot, N])

Compute parameters for a Yeo-Johnson normality plot, optionally show it.

### Univariate and multivariate kernel density estimation

gaussian_kde(dataset[, bw_method, weights])

Representation of a kernel-density estimate using Gaussian kernels.

Warnings / Errors used in scipy.stats
DegenerateDataWarning([msg])

Warns when data is degenerate and results may not be reliable.

ConstantInputWarning([msg])

Warns when all values in data are exactly equal.

NearConstantInputWarning([msg])

Warns when all values in data are nearly equal.

FitError([msg])

Represents an error condition when fitting a distribution to data.