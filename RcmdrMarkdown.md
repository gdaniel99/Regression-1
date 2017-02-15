<!-- R Commander Markdown Template -->

Replace with Main Title
=======================

### Your Name

### 2017-02-15








```r
> names(White_wines) <- make.names(names(White_wines))
```


```r
> compareCoefs(prestige.mod2, reg1)
```

```

Call:
1: lm(formula = prestige ~ education + log2(income), data = Prestige)
2: lm(formula = child ~ parent, data = Galton.train)
               Est. 1     SE 1   Est. 2     SE 2
(Intercept)  -95.1940  10.9979  23.8537   2.9989
education      4.0020   0.3115                  
log2(income)   7.9278   0.9961                  
parent                           0.6474   0.0439
```


```r
> compareCoefs(prestige.mod1, prestige.mod2, reg1)
```

```

Call:
1: lm(formula = prestige ~ education + log2(income) + women, data = 
  Prestige)
2: lm(formula = prestige ~ education + log2(income), data = Prestige)
3: lm(formula = child ~ parent, data = Galton.train)
                Est. 1      SE 1    Est. 2      SE 2    Est. 3      SE 3
(Intercept)  -110.9658   14.8429  -95.1940   10.9979   23.8537    2.9989
education       3.7305    0.3544    4.0020    0.3115                    
log2(income)    9.3147    1.3265    7.9278    0.9961                    
women           0.0469    0.0299                                        
parent                                                  0.6474    0.0439
```


```r
> whwi <- 
+   read.table("/Users/gdaniel99/RStudio Stuff/Regression-1/White_wines.csv", 
+   header=TRUE, sep=",", na.strings="NA", dec=".", strip.white=TRUE)
```


```r
> RegModel.1 <- 
+   lm(quality~alcohol+chlorides+citric.acid+density+fixed.acidity+free.sulfur.dioxide+pH+residual.sugar+sulphates+total.sulfur.dioxide+volatile.acidity,
+    data=whwi)
> summary(RegModel.1)
```

```

Call:
lm(formula = quality ~ alcohol + chlorides + citric.acid + density + 
    fixed.acidity + free.sulfur.dioxide + pH + residual.sugar + 
    sulphates + total.sulfur.dioxide + volatile.acidity, data = whwi)

Residuals:
    Min      1Q  Median      3Q     Max 
-3.8348 -0.4934 -0.0379  0.4637  3.1143 

Coefficients:
                       Estimate Std. Error t value Pr(>|t|)    
(Intercept)           1.502e+02  1.880e+01   7.987 1.71e-15 ***
alcohol               1.935e-01  2.422e-02   7.988 1.70e-15 ***
chlorides            -2.473e-01  5.465e-01  -0.452  0.65097    
citric.acid           2.209e-02  9.577e-02   0.231  0.81759    
density              -1.503e+02  1.907e+01  -7.879 4.04e-15 ***
fixed.acidity         6.552e-02  2.087e-02   3.139  0.00171 ** 
free.sulfur.dioxide   3.733e-03  8.441e-04   4.422 9.99e-06 ***
pH                    6.863e-01  1.054e-01   6.513 8.10e-11 ***
residual.sugar        8.148e-02  7.527e-03  10.825  < 2e-16 ***
sulphates             6.315e-01  1.004e-01   6.291 3.44e-10 ***
total.sulfur.dioxide -2.857e-04  3.781e-04  -0.756  0.44979    
volatile.acidity     -1.863e+00  1.138e-01 -16.373  < 2e-16 ***
---
Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

Residual standard error: 0.7514 on 4886 degrees of freedom
Multiple R-squared:  0.2819,	Adjusted R-squared:  0.2803 
F-statistic: 174.3 on 11 and 4886 DF,  p-value: < 2.2e-16
```


```r
> RegModel.2 <- 
+   lm(quality~alcohol+chlorides+citric.acid+density+fixed.acidity+free.sulfur.dioxide+pH+residual.sugar+sulphates+total.sulfur.dioxide+volatile.acidity,
+    data=whwi)
> summary(RegModel.2)
```

```

Call:
lm(formula = quality ~ alcohol + chlorides + citric.acid + density + 
    fixed.acidity + free.sulfur.dioxide + pH + residual.sugar + 
    sulphates + total.sulfur.dioxide + volatile.acidity, data = whwi)

Residuals:
    Min      1Q  Median      3Q     Max 
-3.8348 -0.4934 -0.0379  0.4637  3.1143 

Coefficients:
                       Estimate Std. Error t value Pr(>|t|)    
(Intercept)           1.502e+02  1.880e+01   7.987 1.71e-15 ***
alcohol               1.935e-01  2.422e-02   7.988 1.70e-15 ***
chlorides            -2.473e-01  5.465e-01  -0.452  0.65097    
citric.acid           2.209e-02  9.577e-02   0.231  0.81759    
density              -1.503e+02  1.907e+01  -7.879 4.04e-15 ***
fixed.acidity         6.552e-02  2.087e-02   3.139  0.00171 ** 
free.sulfur.dioxide   3.733e-03  8.441e-04   4.422 9.99e-06 ***
pH                    6.863e-01  1.054e-01   6.513 8.10e-11 ***
residual.sugar        8.148e-02  7.527e-03  10.825  < 2e-16 ***
sulphates             6.315e-01  1.004e-01   6.291 3.44e-10 ***
total.sulfur.dioxide -2.857e-04  3.781e-04  -0.756  0.44979    
volatile.acidity     -1.863e+00  1.138e-01 -16.373  < 2e-16 ***
---
Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1

Residual standard error: 0.7514 on 4886 degrees of freedom
Multiple R-squared:  0.2819,	Adjusted R-squared:  0.2803 
F-statistic: 174.3 on 11 and 4886 DF,  p-value: < 2.2e-16
```


