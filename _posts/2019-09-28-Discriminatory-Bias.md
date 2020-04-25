---
layout: post
title: Is predicting better predicting fairly?
categories: ai-ml-bias
author: Monique Wong

---
### Describing Discriminatory Bias in Machine Learning

Most of us have an idea of what discriminatory bias means. It’s when characteristics such as gender, age, race, religious beliefs or sexual orientation changes the way we make decisions about a person.

Machine learning may seem like a daunting concept. For now, let’s think of it as a way for a computer to recognize patterns in a lot of data in order to help us make decisions.

At first blush, the former seems like the domain of lawyers and social justice activists while the latter belongs in the world of statistics and computer science. The way these two concepts come together is not obvious. I assure you though, that the relationship between these concepts has important implications on whether organizations should embrace machine learning.

## A fictional example

Let’s imagine that on a fictional town of Zuon, there are two dominant population groups: Purple Rectangles and Orange Circles.

Purple Rectangles live in relative comfort. They live in beautiful homes nested in safe communities. Purple Rectangle children grow up happy, healthy and are productive members of society.

Orange Circles live on the outskirts of Zuon. These neighborhoods are not as friendly. Orange Circle children grow up afraid, untrusting and are unsure of how they fit into society. Some Orange Circle children learn to steal to provide for food and shelter. Often, they don’t finish high school. Many fall into a career of crime.

![zuon-1](/assets/zuon-1.png)

The mayor of Zuon believes that safe communities are the key to a higher quality of life. He begins to police the outskirts of Zuon more heavily. Children are arrested for stealing to deter early criminal tendencies. Not seeing the results, he hires a team of data scientists to predict the likelihood that a convicted criminal will re-offend. This way, he thought, he can do a better job of keeping potentially violent lawbreakers off the streets.

The data scientists work away and come up with a solution. The solution takes into account a dizzying number of factors from the age of the convicted person’s first crime to the criminal history of the person’s parents to make the prediction. This tool is then used to help Zuon judges make decisions like length of jail time.

![zuon-2](/assets/zuon-2.png)


Over the years, more and more Orange Circles end up in prison for ever longer periods of time. The system is objective (it’s based on math and data!) and is well-intended (who doesn’t want more criminals off the streets?). What went wrong?

![zuon-3](/assets/zuon-3.png)

It turns out that discrimination doesn’t have to be ill-intended. No one in Zuon was discriminating against shape or colour. With machine learning, we accidentally created a predictive model that is discriminatory. The model resulted in very different outcomes for Purple Rectangles compared to Orange Circles.

## How did this happen?

There are several causes for discriminatory bias in machine learning algorithms.

1) Data scientists are not telling the machine to optimize for fairness: When we ask a computer to do everything it can to accomplish a goal, it does that without consideration. So, when we ask it to assess the likelihood of a person re-offending while minimizing the errors it makes, it does only that. There is no consideration for whether it’s classifying one group as significantly more prone to crime than another. There is no “fairness” objective programmed into the machine although it is possible.

2) The data that data scientists use reflects a biased world: The data that we give to a computer to learn from is based on a reality that can be discriminatory towards certain groups. In Zuon, the neighborhoods where Orange Circles lived are more heavily policed so the chances of Orange Circles being caught are higher if both a Purple Rectangle and an Orange Circle commit a crime. The data reflects higher incarceration rates for Orange Circles. The algorithm learns society’s biases and perpetuates them in its predictions.

3) Data scientists select features that reduce error, not bias: A data scientist chooses what data an algorithm uses based on the performance of the model. The effect of feature selection on bias is often unclear. Zuon’s predictive model doesn’t explicitly label defendants as Purple Rectangles or Orange Circles but uses family criminal history and age of first arrest as inputs. With Zuon’s societal inequities, more Orange Circles come from families of crime and were first arrested at an early age compared to Purple Rectangles. Indirectly, the features selected creates a model that is biased against Orange Circles.

In the real world, these behaviours can lead to the unequal treatment of people based on gender, age, race, religion or sexual orientation based on the outcomes of a self-learning algorithm.

## Real-life examples

The story of Zuon is not as fictional as it seems. A similar predictive model being used across several states in the U.S. COMPAS stands for Correctional Offender Management Profiling for Alternative Sanctions and is an algorithm used to assess a criminal defendant’s likelihood of becoming a recidivist, someone who will re-offend.

ProPublica, a non-profit investigative journalist, analyzed COMPAS for discriminatory bias. When comparing actual recidivism rates to COMPAS predictions for 10,000 criminal defendants, the algorithm is as likely to correctly predict recidivism for black versus white defendants. However, black defendants were more often inaccurately predicted to have a high risk of recidivism whereas white defendants were more often inaccurately predicted to have a low risk of recidivism. COMPAS continues to be used in courts today to help judges determine sentencing.

COMPAS is not the only discriminatory application of machine learning. Examples of discriminatory bias have been discovered with Amazon’s recruiting system, Facebook’s advertisements and in mortgage lending.

## Last thoughts

As data scientists and decision makers, we have a responsibility to use technology wisely. While machine learning can certainly improve performance and quality of life, we need to be aware of and plan for its flaws. Christian Lou Lange, a Nobel Peace Prize winner once said: “Technology is a useful servant but a dangerous master.” Let us be thoughtful and use machine learning to move society forward instead of further entrench society’s inequities.

## Sources of inspiration:

- https://www.propublica.org/article/how-we-analyzed-the-compas-recidivism-algorithm
- https://towardsdatascience.com/is-your-machine-learning-model-biased-94f9ee176b67
- https://pair-code.github.io/what-if-tool/ai-fairness.html
- https://www.technologyreview.com/s/612876/this-is-how-ai-bias-really-happensand-why-its-so-hard-to-fix/
- https://medium.com/@ericakochi/how-to-prevent-discriminatory-outcomes-in-machine-learning-3380ffb4f8b3
- https://towardsdatascience.com/machine-learning-and-discrimination-2ed1a8b01038
- https://towardsdatascience.com/understanding-and-reducing-bias-in-machine-learning-6565e23900ac
- https://www.theguardian.com/technology/2017/apr/13/ai-programs-exhibit-racist-and-sexist-biases-research-reveals