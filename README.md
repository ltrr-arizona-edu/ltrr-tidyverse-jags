# The standard Docker + R + RStudio + tidyverse image with JAGS added

The base image is one of the standard versioned ones from Rocker
https://www.rocker-project.org/
augmented with the standard distributed Debian package for JAGS
(Just Another Gibbs Sampler for Bayesian MCMC); see:
https://tracker.debian.org/pkg/jags
The rjags and coda packages get pre-installed into this by the
mechanism that Rocker likes to use (install2.r).

Usage is similar to the base image, for example
docker run -e PASSWORD=donotshootthealbatross -v $(pwd):/home/rstudio --rm -p 8787:8787 mmunro/ltrr-tidyverse-jags:0.1.1
