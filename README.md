java c
EN.553.413/613
Applied Stats and Data Analysis
PRACTICE FINAL EXAM
Question 1. For the following scenarios, indicate the most appropriate models that could be applied from the list below.
Models:
(A) simple logistic regression;
(B) multiple logistic regression;
(C) polynomial regression with one predictor;
(D) polynomial regression with two predictors;
(E) single factor ANOVA;
(F) two-factor ANOVA;
(G) polytomous logistic regression;
(H) none of the above
Scenarios:
In all scenarios Y is the response variable; X, Xi are predictor variables.
(i) Y is the time it takes to service a car (in hours), X1 is the brand of the car, X2 is the age of the car (in months);
(ii) Y is whether a participant took a COVID shot or not, and X is the age of the participant (in years);
(iii) Y is the weather tomorrow (sunny, cloudy or raining), X1 is the temperature today (measured in F), X2 is the pressure today (measured in Pa), X3 is the weather today (sunny, cloudy or raining);
(iv) Y is the probability that a customer will buy a car, X1 is the brand of the car, X2 is the price of the car (in thousands of dollars);
(v) Y is the flight delay (in minutes) of a major US airline in 2019, and X is the day of the week (from Sunday to Monday).
Question 2. A company that is involved in importing rice is currently interested in the relationship between package weights and sales, e.g., are heavier packages easier to sell? The company designs a randomized experimental study in which the predictor variable X is the weight of the package (in kilograms) and the response variable Y is the number of packages sold in one month. The number of data points is n = 20. The company then runs a simple linear regression according to the model
Yi = β0 + β1Xi + εi
where the error terms εi are assumed to be independent normal random variables with mean 0 and constant variance σ2(σ2is assumed unknown).
The following quantities were calculated from the data

The following estimates were computed from the data
b0 = −1.0361; b1 = 2.0284; MSE = 0.0315
From the above output, answer the following question.
(a) (5pts): Compute the estimated variance for b1?
(b) (10pts): Setup and conduct two tests (a t-test and an F-test) for the hypothesis that package weights has an effect on number of packages sold. Use a significance level of α = 0.01. State your conclusions.
(c) (5pts): Can a t-test and an F-test be used interchangeably in the simple linear regression setting? Explain in your own words why yes or why no.
(d) (5pts): What is the 95% prediction interval for Yh when the associated value of the predictor variable is Xh = 3 ?
Hint: the following identity may be useful:   
Question 3. Answer the following collection of (unrelated) questions regarding matrices.
(a) Let X be the following matrix

Let y and z be the vectors

Compute the projection of y onto Col(X) (column space of matrix X). Also compute the projection of z onto the Col(X). Explain why your answers make sense from the geometric point of view.
(b) Let x = [X1, X2, X3]⊤ be a random vector in R3 with variance-covariance matrix

Let a random vector Y = (Y1, Y2)⊤ be defined by Y1 = X1 + X2, Y2 = X1 + X2 + X3. Compute the variance-covariance matrix Var[Y ].
(c) Let Y be a vector in Rn, X is a n × q1 matrix and Z is a n × q2 matrix. Suppose that scientist A fits a linear model (using least squares) of the form. Y = Xβ + ε to y and scientist B fits a linear model (also using least squares) of the form. Y = Xβ + Zγ + ε. Scientist A obtains the estimate bA and scientist B obtains the estimates bB and cB (these are estimates of β and γ of the model B, respectively). It turns out bB = bA. What can you reasonably assume about the relationship between X and Z代 写EN.553.413/613 Applied Stats and Data Analysis PRACTICE FINAL EXAMProlog
代做程序编程语言? Justify your answer.
Question 4. Let Y = Xβ + ε be a linear model where ε ∼ Nn(0, σ2In).
Answer the following questions.
(a) Suppose that X has full-column rank and that β is indexed as β = (β0, β1, . . . , βp)⊤. Which of the following hypotheses tests can be formulated as a general linear hypothesis test H0 : Cβ − γ = 0? If the test can be formulated as a general linear hypothesis test, write down a test statistic and specify numerical values where possible.

(b) Suppose Y = (Y1, Y2, . . . , Yn)⊤. Let b be the ordinary least square estimates of β for the model Y = Xβ + ε and e = Y − Xb. Are the three quantities

pairwise independent? Justify your answer. Above, 1 is an n-by-1 vector of 1’s.
Question 5. Let U1, U2, . . . , Un1 be indepedent and identically distributed random variables with Ui being normally distributed with mean µ1 and variance σ2. Similarly, let V1, V2, . . . , Vn2 be i.i.d. normal random variables with mean µ2 and variance σ2, and W1, W2, . . . , Wn3 be i.i.d. normal random variables with mean µ3 and variance σ2. Also assume that the Ui’s, Vj ’s and Wk’s are all independent.
(a) Let y = [U1, U2, . . . , Un1, V1, V2, . . . , Vn2, W1, W2, . . . , Wn3]⊤. Write y as a linear model y = Xβ + ε where β = [µ1, µ2, µ3]⊤.
(b) Find the least square estimate βˆ = [ˆµ1, µˆ2, µˆ3]⊤ of β.
(c) Write down (and simplify as much as you can), the expression for the sum of square error for the model in part (a).
(d) Write down, and simplify as much as you can, the expression for the test statistic for testing the hypoth-esis H0 : µ1 = µ2 = µ3 against the alternative hypothesis that HA : µ1 ≠ µ2, or µ2 ≠ µ3, or µ1 ≠ µ3. What is the distribution of the resulting test statistic assuming H0 is true ? Hint: If µ1 = µ2 = µ3, then the model in part (a) reduces to y = 1µ + ε where 1 ∈ Rn1+n2+n3is a vector of 1’s and µ ∈ R.
Question 6. The prostate dataset comes from a study on 97 men with prostate cancer who were due to receive a surgery. The variables are as follows
❼ lcavol: log(cancer volume)
❼ lweight: log(prostate weight)
❼ age: age
❼ lbph: log(benign prostatic hyperplasia amount)
❼ svi: seminal vesicle invasion
❼ lcp: log(capsular penetration)
❼ gleason: Gleason score
❼ pgg45: percentage Gleason scores 4 or 5
❼ lpsa: log(prostate specific antigen)
Consider the following output.
data(prostate)
x <- BestSub(prostate[,1:8],prostate[,9],num = 1)
x
       p 1 2 3 4 5 6 7 8 SSEp                                    r2                   r2.adj                        Cp                AICp                SBCp       PRESSp
1 2 1 0 0 0 0 0 0 0 58.91478 0.5394320 0.5345839 27.406210 -44.36603 -39.21661 61.66596
2 3 1 1 0 0 0 0 0 0 51.74218 0.5955040 0.5868977 14.747299 -54.95846 -47.23433 55.22594
3 4 1 1 0 0 1 0 0 0 46.56844 0.6359499 0.6242063 6.173546 -63.17744 -52.87859 50.97617
4 5 1 1 0 1 1 0 0 0 45.59547 0.6435561 0.6280585 6.185065 -63.22555 -50.35199 51.17882
5 6 1 1 1 1 1 0 0 0 44.43668 0.6526150 0.6335279 5.816804 -63.72263 -48.27437 50.99282
6 7 1 1 1 1 1 0 0 1 43.77597 0.6577801 0.6349654 6.466493 -63.17571 -45.15273 51.31739
7 8 1 1 1 1 1 1 0 1 43.10756 0.6630054 0.6365002 7.100428 -62.66823 -42.07054 51.57752
8 9 1 1 1 1 1 1 1 1 43.05842 0.6633896 0.6327886 9.000000 -60.77886 -37.60646 52.50892
(a) What is the best model with 5 estimated parameters ? (The intercept is counted as one parameter). You should list names of predictor variables.
(b) What is the ’best’ model as selected by the adjusted R2coefficient? By Mallow’s Cp criterion? You should list names of predictor variables.
(c) Do we maximize or minimize the criterions R2, AICp, SBCp, P RESSp? Explain why R2is not a good criteria for the model selection.





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
