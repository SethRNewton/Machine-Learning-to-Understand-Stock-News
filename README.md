Severe price movements in stock following news about a company are common. Sentiment
analysis of news articles is now widely available, especially for financial news. Sentiment analysis
uses a trained language model to score a body of text in terms of its positivity. Out of curiosity, I
gathered sentiment analysis of news articles for many stocks over a two year time frame and
plotted it against the change in stock price the following day after the news was released. For
the vast majority of news, no discernable pattern was observed. However, when the news was
filtered for only very positive news (positive sentiment score > 0.10 out of 1), a weak correlation
was observed.

Stock traders often use indicators such as exponential moving averages, relative strength index,
moving average convergence/divergence, etc. to try and predict stock price movements.
Furthermore, they consider the movement of the overall market in their trading decisions. The
overall market movement can be reflected in stock indices such as the S&P 500 or Dow Jones
Industrial index. I wanted to explore the idea of using sentiment analysis scores, stock price
indicators, and index data together in a machine learning model to see if I classify stocks into
three categories: likely to increase in value over the next day, likely to stay relatively stable, or
likely to decrease in value.The data was gathered using two different APIs: the EOD Historical Data (https://eodhd.com/)
API and the TDAmeritrade API (has now changed to Schwab). News about specific stocks,
along with sentiment analysis scores, were gathered from EOD while daily price quotes were
gathered from TD Ameritrade. Quotes for the symbols SPY and DJI were used for the S&P 500
and Dow Jones Industrial index, respectively, to give broad market context to individual stock
movements.

Data were limited to a two year timespan, from June, 2021 to May, 2023. Results were filtered
for positive sentiment analysis scores > 0.1, resulting in ~108,000 news stories to process.
