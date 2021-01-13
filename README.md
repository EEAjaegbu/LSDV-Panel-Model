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

# RUNNING THE CODE IN R

A) Pooled OLS results

Call:
lm(formula = LWAGE ~ ED, data = PSID)

Residuals:
     Min       1Q   Median       3Q      Max 
-1.92996 -0.26863  0.00931  0.28453  1.83076 

Coefficients:
            Estimate Std. Error t value Pr(>|t|)    
(Intercept) 5.838779   0.030997  188.37   <2e-16 ***
ED          0.065204   0.002358   27.65   <2e-16 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.4243 on 4163 degrees of freedom
Multiple R-squared:  0.1552,	Adjusted R-squared:  0.155 
F-statistic: 764.5 on 1 and 4163 DF,  p-value: < 2.2e-16

B) Fixed effcets Least Squares Dummy Variables(Two way)

Call:
lm(formula = LWAGE ~ ED + ID - 1, data = PSID)

Residuals:
     Min       1Q   Median       3Q      Max 
-1.89454 -0.16071  0.00766  0.17214  1.94475 

Coefficients: (1 not defined because of singularities)
       Estimate Std. Error t value Pr(>|t|)    
ED     0.505235   0.008178  61.782  < 2e-16 ***
ID1    1.417645   0.122665  11.557  < 2e-16 ***
ID2    0.940862   0.133123   7.068 1.89e-12 ***
ID3    0.447851   0.138780   3.227 0.001262 ** 
ID4    1.334617   0.127739  10.448  < 2e-16 ***
ID5   -1.179404   0.163553  -7.211 6.74e-13 ***
ID6    1.030106   0.138780   7.423 1.43e-13 ***
ID7    0.248064   0.138780   1.787 0.073947 .  
ID8    1.539444   0.127739  12.051  < 2e-16 ***
ID9   -1.186562   0.163553  -7.255 4.91e-13 ***
ID10  -1.571617   0.163553  -9.609  < 2e-16 ***
ID11   0.866606   0.138780   6.244 4.75e-10 ***
ID12   0.703409   0.138780   5.069 4.21e-07 ***
ID13   1.102330   0.138780   7.943 2.62e-15 ***
ID14  -1.601607   0.170166  -9.412  < 2e-16 ***

Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.2596 on 3570 degrees of freedom
Multiple R-squared:  0.9987,	Adjusted R-squared:  0.9985 
F-statistic:  4645 on 595 and 3570 DF,  p-value: < 2.2e-16






Reference
Demodar N. Gujariti, Dawn c Porter. Basic Econometrics(fifth Edition)
