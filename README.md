This repository contains two scripts related to the study of molecular markers of antimalarial drug resistance

1. Beta_binomial_percolateR is iterations of a function which take prior genotyping data in the form of prevalence and current genotyping data generated via recent benchwork


Prior information containing count data of both mutant infections, and sample size, were coded via a beta distribution.

Π ~ Beta(α,β)
α = Prior mixed + Prior mutant infections
β = Prior WT infections

Our observed outcome (prevalence) is distributed binomially, generating the following likelihood function.

Y ~ Binomial(Observed mutant infections, Π) 

The posterior distribution of prevalence given our observed data is described via a beta-binomial conjugate prior. 
	P(Π|Y) = Beta(α^1,β^1) 
α^1 = Prior mutant infection + observed mutant infections 
β^1 = Prior WT infections + N observed - observed mutant infections 

All years which had no corresponding information are parameterized via Jeffreys prior, an uninformative prior of the beta distribution.
α uninformative = .5, 
β uninformative = .5


![unnamed](https://github.com/user-attachments/assets/6a6264a2-9bf6-4aee-bd60-6d7c5db81cee)

