# newTutorial-
learning how to use github with Git bash and R Markdown


# Non-parametric bootstrap

NPsimXsample <- replicate(k, sample(Day1Waiting, replace = TRUE))
NPsimYsample <- replicate(k, sample(Day2Waiting, replace = TRUE))

# Compute mean differences of n1 & n2 simulated observations k times:

NPsimMeanDifs <- apply(NPsimXsample, 2, mean) - apply(NPsimYsample, 2, mean)

# find the two relevant quantiles of k simulated mean differences


quantile(NPsimMeanDifs, c(0.025,0.975))    # i.e. 95% Confidence Interval

