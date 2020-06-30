### NLP - How Trump's Tweets impact China Market

#### The Motivation of the Project
This project is a basic investigation of the natural language process. Analyze how Trump's Tweets will impact China Market by checking what would happen in markets after Trump said positive, neutral or negative things about China. I get the idea from https://www.youtube.com/watch?v=wlnx-7cm4Gg&t=890s

#### A brief summary:
1.  Get Trump's twitter data from Twitter Developer (a token is required, so you need to sign up an account at https://developer.twitter.com/en)
2. Clean twitter data, including:
> - Extract main sentences by regularization
> - Find all root words (e.g. turn 'took' into 'take')
> - Delete stop words (e.g. deleting 'a', 'the')
> - Filter tweets with keywords: I use China and Chinese, only the tweets Have one of the keywords will be used in further research
> - Adjust time value: The time recode in twitter is neither US time nor China time. Turn it into China time, and if it is later than 15 p.m. (stock market close at this time), the date will lag for 1 day. (like, tonight's twitter will only influence tomorrow's market)
> - Analyzing the sentiment of a tweet (by third-party package). If there are more than 2 related tweets, the sentiment of that day would be weighted by retweets value.
3. Download Shanghai market data, by yahoo finance.
4. Analyze the correlation between two data:
> - correlation between sentiments and return of that day
> - set classes of sentiment and return, find the correlation between two class
 
#### Preliminary result
1. kind of no strong correlation.
2. An interesting thing is that I did similar steps in March (data from Dec to Mar), the correlation is strong than now.

#### Problems (need to develop):
1. The data set is small. A free account of twitter developer could fetch only 3200 tweets from a person, including replies. That's only 2 or 3 months data, cuz Trump used twitter tooooo much.
2. The tweet on weekends was not considered. (there might be lots of news could impact markets at weekends)
3. The analyzing part is simple and superficial.
4. Using daily data now, minutes data would be much better.
5. Sentiment analysis is given by a third-party package, which is not precise, sometimes.

#### Possible Future Work
1. I personally find it is an interesting NLP project, and the idea could used to other places, like how CNN's news impact market.
2. The key point is how to combine markets and tweets, by quantitative methods. Otherwise, it is completely a data science project.

![](https://tva1.sinaimg.cn/large/007S8ZIlgy1gga3nysv48j30vs0u042p.jpg)
