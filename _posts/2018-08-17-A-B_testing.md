---
layout: post
title: A/B testing
---

I have got the opportunity to work on a project to help company decide whether to launch a new page on their website or keep the old page.
I’ll do this by a widely practised experiment called A/B testing.

## What is A/B Testing?

A/B tests are used to test changes on a web page by running an experiment where a control group sees the old version, while the experiment 
group sees the new version. A metric is then chosen to measure the level of engagement from users in each group. These results are then 
used to judge whether one version is more effective than the other. 
A/B testing is very much like hypothesis testing with the following hypotheses:

## **Null Hypothesis** : The new version is no better, or even worse, than the old version.
## **Alternative Hypothesis** : The new version is better than the old version.

If we fail to reject the null hypothesis, the results would suggest keeping the old version. If we reject the null hypothesis, 
the results would suggest launching the change.

### Let's start with the experiment:

I was testing around 295000 users some of them were landed on new page and others on old page.

A/B test has few drawbacks one of them is:
Consistency among test subjects in the control and experiment group (imbalance in the population represented in each group can lead 
to situations like Simpson's Paradox)

The dataset I was assigned had equal number of users in each group and the probability of landing on either of the page was 50%. So the 
situations like Simpson's Paradox won't arise here. Good for us!!

I approached A/B testing by performing
 
- Probability

- Hypothesis Testing

- Regression

Performing probability I found conversion rate for new page was less than the old page. But to be sure that the obtained results are 
not just by chance I performed bootstrapping.

One of our class instructors suggests that bootstrapping can be used as a substitute for any statistical test that we would use in
traditional statistics to talk about populations. This includes t-tests, F-tests, chi-squared - you name it, apparently we can do it 
with bootstrapping.

Null hypothesis

Alternative Hypothesis

Using bootstrapping approach and p-value calculation I got the probability value of 0.906 which suggest that we have failed to 
reject the null.

Statistical test that can be performed here was z-test
Requirements of z-test are
Population is variance is known
Sample size is more than 30

Critical Value is larger than Z-score which again suggest us that we have failed to reject the null & that there is 
evidence of conversion for new page is less or equal to the old page.

**Regression approach**

Our main aim is to find if the user has converted or not. Since we have only two outcomes I decided to perform logistic regression.
Looking at the probability value which greater than our alpha level of 5% We have statistical evidence that conversion rate for new page is not different from the new page.
AS now it is very clear that conversion rate for old page is more than new page.


