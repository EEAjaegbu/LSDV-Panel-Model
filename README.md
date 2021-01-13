# LSDV-Panel-ModelThe least Square Dummy Varaiable Fixed Effects Panel Model

# Panel Data
Panel data or longitudinal data refer to a data set containing observations on multiple phenomena over multiple time periods. Thus it has two dimensions: spatial (crosssectional) and temporal (time series).

# (Gujariti) why Panel Data
1. Since panel data relate to individuals, firms, states, countries, etc., over time, there is bound to be heterogeneity in these units. The techniques of panel data estimation can take such heterogeneity explicitly into account by allowing for subject-specific variables, as we shall show shortly. We use the term subject in a generic sense to include
microunits such as individuals, firms, states, and countries.

2. By combining time series of cross-section observations, panel data gives “more informative data, more variability, less collinearity among variables, more degrees of freedom
and more efficiency.”

3. By studying the repeated cross section of observations, panel data are better suited to study the dynamics of change. Spells of unemployment, job turnover, and labor mobility
are better studied with panel data.

4. Panel data can better detect and measure effects that simply cannot be observed in pure
cross-section or pure time series data. For example, the effects of minimum wage laws


# The Fixed Effects Least Squares Dummy Variale
The least-squares dummy variable (LSDV) model allows for heterogeneity among subjects by allowing each entity to have its own intercept value, as shown in model (16.4.1). Again,
we continue with our airlines example.

Yit = β1i + β2Qit + β3X1it + β4X2it + uit 
                  i = 1, 2 . . . , N
                  t = 1, 2, . . . , T

The term “fixed effects” is due to the fact that, although the intercept may differ across subjects, each entity’s intercept does not vary over time, that is, it is time-invariant.





Reference
Demodar N. Gujariti, Dawn c Porter. Basic Econometrics(fifth Edition)
