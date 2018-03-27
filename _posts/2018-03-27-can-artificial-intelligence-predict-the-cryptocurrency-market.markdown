---
layout: post
title:  "Can Artificial Intelligence Predict the Cryptocurrency Market?"
date:   2018-03-27 17:01:33 +0100
author: Alex
tags: ['artificial intelligence', 'cryptocurrency', 'sentiment analysis', 'machine learning']
---

![Can Artificial Intelligence Predict Cryptocurrency Market Moves?]({{ "/assets/can-artificial-intelligence-predict-cryptocurrency-market.jpg" | absolute_url }})

## Opinion moves the market.

## Can Artificial Intelligence sense opinion?

## And, can AI predict the market before it moves?

The latter two are the fundamental questions we are trying to answer with the [Trademindx project][trademindx]!

Let’s discuss each of these points in a bit more detail.

## Opinion

What impacts the price of precious metals, currencies, cryptocurrencies, stocks? Some may think it’s the money invested, but this is not the case. It is driven by opinion! To be more precise, it is opinion and consensus.

There’s an excellent post on [Reddit][reddit] which goes into more depth on opinion in the crypto space with almost 20K up-votes and its a punchy write up that is well worth a read!

Since it is generally accepted, let’s just take it is as a baseline assumption for the purposes of discussion: opinion moves the market.

Now, here’s a crazy thought, imagine you could take the whole set of traders participating in particular market. They are all making independent decisions, making up their minds on buy/sell prices, placing orders and executing trades.

What if you could model that set of traders and deduce their overall consensus on opinion? What do you get? A super trader! That trader can clearly predict the market movements correctly. Now it’s just a case of building such a trader with AI technology.

There’s an obvious problem, not all traders are actively commenting on social media or forums and we cannot (unfortunately, yet) plug-in to their brains!

However, we can assume that we are taking a slice of the market and most traders are consuming some sort of information when making trading decisions. We then have to model how that information is being analyzed by the traders and we are golden.

## Sensing Opinion With Artificial Intelligence

We have established that opinion moves the market. The next logical question is to discuss whether AI can be used to measure opinion to a statistical degree of confidence.

In order to attempt to measure opinion, we need to source raw information from a number of sources, apply Natural Language Processing (NLP) to make sense of it, turning it into data that can be processed by a machine. Then, we apply sentiment analysis plus machine learning algorithms to derive trading signals.

So what are the sources we can go to in order to establish opinion?

- News articles
- Twitter feeds
- Reddit posts
- Other social media feeds
- Forum threads
- Even GitHub repository activity
- And of course, market data feeds from cryptocurrency exchanges

Once we get the data, we run it through a sentiment analyzer which allocates a sentiment measure that looks something like this:

{% highlight ruby %}
SentimentConfidence {
id=’5a53bc72ca3ec40fb2bd9bbd’,
ticker=’ETH’,
positiveSentiment=57.0,
negativeSentiment=23.0,
neutralSentiment=20.0,
compoundSentiment=100.0,
numberOfSamples=781
}];
{% endhighlight %}

In the case above, Trademindx has deduced that at that specific moment in time, after analyzing 781 samples of discreet data, Ethereum has an overall positive sentiment — with a 57% degree of confidence! We then repeat this for all other cryptocurrencies that we want to analyze. Not only that, we can track sentiment as it changes in real-time! Cool huh?

Research has shown that sentiment analysis algorithms are approaching high degrees of accuracy. Our sentiment analyzer is based on VADER — Valence Aware Dictionary and sEntiment Reasoner, which has been shown to produce highly accurate results, even in social media contexts.

Our AI can sense opinion!

Market data sources providing volumes and price ticks are still relatively open in the cryptocurrency space with exchanges freely publishing near real-time or even real-time feeds, which is in direct contrast to mature forex and stock markets. So our market data sources are abundant.

#### “In the midst of chaos, there is also opportunity” — Sun Tzu

Furthermore, what makes the cryptocurrency market such an interesting domain to analyze, is the relative immaturity which leads to high volatility.

Market moves are often triggered by announcements, news articles, support by social influencers and even rumours! This often happens very quickly, so if an AI algorithm could sense changing opinion, then this could in turn provide a trading advantage. And of course, a trading advantage has intrinsic monetary value — profit.

## Predicting Cryptocurrency Market Moves

So, we can get an idea of the overall opinion for a cryptocurrency with a degree of confidence but how do we then use that to predict market moves?

Well that’s where it gets a bit complicated.

As well as taking sentiment data, we also take our input data and attempt to build AI models and then refine those models using feedback. This is where machine learning comes in. We back test our models against known market moves and then continuously re-calibrate those models, thereby attempting to improve accuracy. The model starts off vague but gets more refined as time moves on and more data becomes known.

If that sounds confusing, lets go over a more concrete example. So say our current model for Ether, predicts that based on certain characteristics found in our data, we expect the price of Ether to rise within the next 24 hours. We make note of that, wait 24 hours and check if that was the case or not. We then use this information to refine the model. This is what we mean by feedback .This “predict and test” happens all the time — continuously.

At any given time, we take the most up-to-date model, combine it with our sentiment data and use it to form a trading signal — BUY, SELL or HOLD (FOMO, FUD or HODL if you like that sort of thing!).

And we don’t just consider 24 hours as a back testing timeframe but many different timeframes to test.

For our models, we have decided to use Maximum Entropy (MaxEnt) modelling which has been shown to produce more accurate results than Naive Bayes. However, in the future models can be swapped out if others are deemed to be more accurate.

#### entropy noun — lack of order or predictability; gradual decline into disorder

Here is an extract from our whitepaper:

MaxEnt works by extracting a set of weighted features from the input. Each feature corresponds to a constraint on the model. The MaxEnt model is the model with the maximum entropy of all the models that satisfy the constraints. The baseline principle being that if we choose a model with less entropy we would add information constraints to the model that would not be justified by the evidence available to us. Choosing a MaxEnt model is motivated by the desire to preserve as much uncertainty as possible thus removing any bias. More formally, the maximum entropy principle states that:

“…in making inferences on the basis of partial information we must use that probability distribution which has the maximum entropy subject to whatever is known.”
Additionally, the reasons for using MaxEnt are as follows:

- Near state-of-the-art level of accuracy when classifying complex data sets
- Simple features have been proven to successfully approximate complex relationships
- MaxEnt is able to output the accuracy/confidence of the classification
- Of course the inner workings of Trademindx are a bit more complex than that and are still being actively developed but that’s the high level overview!

We envisage day traders and investors using the Trademindx platform, can gain insights into the social sentiment currently in the market before they execute their trades. This may help with decision making and provide increased returns while lowering risk.

Once AI can be built to predict market moves, the possibilities are then torn wide open for algorithmic trading in the cryptocurrency markets by hooking our AI into existing exchange APIs and running different trading strategies based on the trading signals!

Perhaps our AI can even be hooked into more traditional forex and stock markets too. The principles are similar, its just that the cryptomarket is so much more fun right now.

## So can AI predict cryptocurrency market moves?

In this article, we have given a high-level overview of our approach and are open to discussion. We believe it can be done, with sentiment analysis nearing state-of-the-art and the availability of relatively cheap compute in cloud-based environments, the ingredients are there to make this a reality.

What do you think? Please share your thoughts, feedback or questions in the comments below!

If you would like to find out more about the Trademindx project, then [head over to our homepage][trademindx].

[reddit]:https://www.reddit.com/r/CryptoCurrency/comments/7vga1y/i_will_tell_you_exactly_what_is_going_on_here/
[trademindx]: https://trademindx.com
