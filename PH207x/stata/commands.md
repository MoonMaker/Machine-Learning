# Distribution - Binomial, Poisson and Normal

## Suppose X ~ Binomial(n,p)
binomialp(n,k,p) - returns the probability of observing k successess - P(X=k)
binomial(n,k,p) - returns the probability of observing k or fewer successes - P(X<=k)
binomialtail(n,k,p) - return the probability of observing floor(k) or more successes - P(X>=k)

## Suppose X ∼ Poisson(m).
poissonp(m,k) - returns the probability of observing floor(k) or fewer successes - P(X=k)
poisson(m,k) - returns the probability of observing floor(k) or fewer successes - P(X<=k)
poissontail(m,k) - returns the probability of observing floor(k) or more successes - P(X>=k)

## Suppose Z ~ Normal(0,1)
normal(z) - return the cumulative standard normal distribution - P( Z<z )
normalden(z) - returns the standard normal density

## Distribution Table in Stata
`clear all
set obs 5
gen k=_n-1
gen p = binomialp(2000,k,0.00065)
list k p`

+--------------+
| x          p |
|--------------|
| 0   .2724166 |
| 1    .354372 |
| 2   .2303763 |
| 3   .0997948 |
| 4   .0324057 |
+--------------+

