2024-08-11 05:06

Status: #adult 

Tags:[[Statistics]] [[Stat Quest]]
# Recall Session
To calculate the mean (μ), variance, and standard deviation. You must have a full population data set.
--
If you only have a sample of a full population, then you must estimate the mean(x̄), variance and standard deviation.
--
[[Standard Deviation]] is just the square root of the [[Population Variance]] 
## Formula Key
$$
\sum x=SumOfValues
$$
$$
\sum x^2 = SumOfValues^2
$$
$$
x=Any Given Data Point
$$
$$
\mu = PopulationMean
$$
$$
\overline{x}=Estimated Population Mean
$$
$$
n=Sample Size
$$
$$
N=PopulationSize
$$
$$
\sigma = StandardDeviation
$$
$$
\sigma_s=StandardDeviationOfSample
$$
$$
\sigma_p=StandardDeviationOfPopulation
$$
$$
\sigma^2 = Variance
$$
$$
\sigma_s^2=VarianceOfSample
$$
$$
\sigma_p^2 = VarianceOfPopulation
$$

## Calculating the [[Population Variance]]

$$\frac{\sum(x-\mu)^2}{N}$$
## Calculating the [[Standard Deviation]]
$$\sqrt\frac{\sum(x-\mu)^2}{N}$$


## Estimating the [[Population Variance]]
$$\frac{\sum(x-\overline{x})^2}{n-1}$$
## Estimating the [[Standard Deviation]]
$$\sqrt\frac{\sum(x-\overline{x})^2}{n-1}$$



# Practice

Assume that we have measured the amount of Green Apples in each individual store in a grocery chain. There are 20 Stores in all. Below is the collected data.
--

| Store | Apples |
| ----- | ------ |
| 1     | 12     |
| 2     | 15     |
| 3     | 38     |
| 4     | 33     |
| 5     | 35.    |
| 6     | 36     |
| 7     | 34     |
| 8     | 39     |
| 9     | 41     |
| 10    | 35.    |
~~
$$ N=10 $$
--
$$ \sum x=318 $$
--
$$\sum x^2=11006 $$
--
$$ \mu=\frac{\sum x}{N} ...\mu=31.8 $$
--
$$ \sigma_p=\sqrt{\frac{\sum(x-31.8)^2}{N}} ... \sigma_p=9.453 $$
--
$$ \sigma_p^2=89.359 $$
--
Now, assuming we only have the first five. Let's ***estimate*** based on a sample of the population.
--

| Store | Apples |
| ----- | ------ |
| 1     | 12     |
| 2     | 15     |
| 3     | 38     |
| 4     | 33     |
| 5     | 35     |
~~
$$ n=5 $$
--
$$ \sum x=133 $$
--
$$ \sum x^2=4127 $$
--
$$ \overline{x}=\frac{\sum x}{n}...\overline{x}=26.6 $$
--
$$ \sigma_s=\sqrt{\frac{\sum(x-26.6)^2}{n-1}}...\sigma_s=12.137 $$
--
$$ \sigma_x^2=147.307 $$
--
# Application in [[R]] 

```R
#built in data sets can be accessed with
data()
#access help files in cmd with 
?argument
#OR
help(argument)

#Mean SumOfValues(^2) StandardDeviation(SampleVsPop) Variance(SampleVsPop)

#finding the mean eg. \overline x OR \mu
mean(dataset$VariableName)
#If there are empty cells 'N/A cells' use optional arg to avoid an error
mean(dataset$VariableName, na.rm = TRUE)
#To Estimate Standard Variation based on sample of population
sd(dataset$VariableName)

#To Calculate Population Standard Deviation first assign the formula to a variable like so
population_sd <- sqrt(sum((dataset$VariableName - mean(dataset$VariableName))^2) / length(dataset$VariableName))
#then print
print(population_sd)


```
# References
[How to calculate the above with calculator](https://youtu.be/YByf1x4hBBc?si=129t-PsLvC7hrZxY)

[Stat Quest Video](https://youtu.be/SzZ6GpcfoQY?si=wnBhy204A_Srkq-d)

[Using my calculator (pg. 75)](https://education.ti.com/en/guidebook/details/en/ED3059C9A7F74958BD6CC2EDD8517352/30xiitg)
	 Remove the ^ to view ... !^[[30xiitg-eng_.pdf]]

[Learn R in 39 minutes](https://www.youtube.com/watch?v=yZ0bV2Afkjc)
