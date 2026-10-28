# ECON-3916-Problem-Set-2

## The Survey That Wasn't Random

### Overview
This project investigates how non-response bias can affect customer satisfaction surveys. I simulated user populations before and after a product redesign and compared the observed survey results with the true population values.

### Phase 1: Simulation and Selection Bias
I simulated 50,000 users in each period, including satisfaction scores, engagement time, and support-ticket history. Users with higher satisfaction were more likely to respond, especially after the redesign.

The observed improvement was approximately 0.704 points, while the true population improvement was only 0.0959 points.

### Phase 2: Bootstrap Confidence Intervals
I used bootstrap resampling to calculate percentile and BCa confidence intervals. I also conducted a coverage simulation to test whether these intervals captured the true population mean.

The results showed that narrow confidence intervals do not guarantee accurate estimates when selection bias is present.

### Phase 3: Hypothesis Testing and Power
I performed Welch's two-sample t-test and calculated Cohen's d. I also used power analysis to estimate the sample size required to detect a small improvement.

A simulation showed that increasing the sample size did not eliminate selection bias.

### Phase 4: Inverse Probability Weighting
With AI assistance, I implemented inverse probability weighting (IPW) using logistic regression and bootstrap confidence intervals.

The IPW-estimated improvement was 0.6794 points, compared with the true improvement of 0.0959 points.

IPW did not fully correct the bias because response probability depended on latent satisfaction, even after controlling for the observed covariates.

### Key Takeaway
A large sample size and narrow confidence intervals do not necessarily produce accurate results. Statistical methods can reduce uncertainty, but they cannot automatically eliminate systematic selection bias.

Future surveys should include active follow-up with nonrespondents to improve representativeness.
