# Project Three: StockMarketResearch Channel Questions - Christopher Demeke

# Tech Questions
--------------
## What tech stack should we use and why?
*   Database and Model: Mongoose or Sequelize
    - Users
    - Portfolios:       
    - Transactions Type:     Keep it simple with just "buy" and "sell"
    - Holdings                   
    - Stock Information
    - Stock Prices - can be recived in realtime and use functions to calculate each stock Value, ROI(%), and ROI($)
    - Game Metrics:     Rank, Points, etc...
        
    - Research for Mongoose(NoSQL) - to store Portfolio data, this will be very flat.  We can keep the portfolios seprate from the stock data. 
        - I Mongo for portfolio becuase we do not want a predefined schema, becuase we want the user to add and remove any number of stocks at will.  We don't want a rigid structure.
        - I found the following examples:  [plum](https://github.com/jadnco/plum), [Commandiv Stack](https://www.mongodb.com/blog/post/building-a-secure-stock-trading-app-with-mongodb-atlas)
        - There isn't much on stack over flow [stackoverflow questions 1](https://dba.stackexchange.com/questions/160772/is-mongodb-a-good-fit-to-track-a-stock-portfolio)

    - Research for Sequlize(SQL)
        - This can work if we have a seperate tranaction table for every user.  Functions would have to use realtime data and these tables to calculate portfolio values.
        - We can create tables for Users, All Stocks, Stock Price, Transactions(each user get own transactions table), Holdings, Game Metrics.
        - I had a hard time finding examples of thie implemention [Better-Future](https://github.com/saravena/Better-Future)
        

    - The data (stock prices etc.) being retrieved from an API may not need to be stored.  We will need access realtime values for buy/selling functions. We may only need stock data in realtime transactions, portfolio value calculating, and charting.
    - We may need SQL if we want to store and chart historical data, unless we can find a plugin? If not we can use https://www.highcharts.com/products/highstock/ or other products.

*   API and Methods
    -   GET, POST, DELETE  /api/users  (I added delete b/c of GDPR)
    -   GET, PUT,   /api/users/:id
    -   GET, POST   /api/portfolios
    -   GET          /api/transctions
    -   GET, POST   /api/transctions/:id
    -   GET, POST   /api/portfolios/:id/transctions
    -   GET, PUT   /api/users/game


*   JavaScript framework - React.JS
    - Will need reusable components, virtual DOM, developer tools.
        - I would like to use React becuase we will utilize a lot of forms, charts, and realtime portolio valuation functions.

*   -Express - Node  - (WHY: Javascript, Javascript, Javascript!) I like Javascript.

###     I have friends that completed TopStepTrader Combines and spoke highly about it.
####    I looked up a job application for TopStepTrader Full-Stack Web Developer to see Requirements, for insight.
*   Experience with common web-based languages and frameworks, e.g., Ruby on Rails (preferred), Django Python, JavaScript, (Angular2 with TypeScript ideal)
*   Focus on readability, maintainability, and scalability when writing code
*   Strong familiarity with SQL databases
*   Strong familiarity with API design (REST, SOAP, etc.) / integrations
*   Strong OOP design principles
*   Use existing technologies, rather than building from scratch
*   HTML/CSS knowledge
*   NoSQL experience-especially Redis
*   Parallel / distributed computing experience
*   Financial knowledge
*   Continuous integration knowledge

## What deployment options are there? What are the benefits of the deployment options?
*   It may be overkill but, AWS will give us the best project three experience. Also I really want to learn more about how to deploy.

## Who are the competitors? What do they do well? What problems do they have?
Its a little hard to define the competition since the ideas is still bit abstract.
### Competitors         
*   [TopStep Trader](https://www.topsteptrader.com/)
*   [Ninja Trader](https://ninjatrader.com/)
*   [Tradinb View](https://www.tradingview.com/)
*   [Trading Sim](https://tradingsim.com/)
*   [Investopedia](https://www.investopedia.com/simulator/)
*   [Oanda](https://www.oanda.com/forex-trading/)

## What APIs may benefit for a stock market game? 
(neeed to research these further)
*   https://iextrading.com/developer/   - Says Free API
*   https://www.alphavantage.co/        - Says Free API
*   https://www.programmableweb.com/news/96-stocks-apis-bloomberg-nasdaq-and-etrade/2013/05/22
*   http://www.xignite.com/             - I don't think this one is free

##  What industry related algorithms would we need to use?
[Common Types of Trading Algorithms](https://blog.quantopian.com/common-types-of-trading-algorithms/)
*   Mean Reversion - What goes up must come down
*   Valuation - Bargain Shopping
*   Seasonality - Sell in May and go away
*   Sentiment - Buy the rumor, sell the news
*   Fundamental Investing
*   Technical Investing

[Basics of algorithmic trading: Concepts and examples](https://www.investopedia.com/articles/active-trading/101014/basics-algorithmic-trading-concepts-and-examples.asp#ixzz5IFUrgs9m)
*   Trend-following Strategies  
*   Arbitrage Opportunities
*   Index Fund Rebalancing
*   Mathematical Model Based Strategies
*   Trading Range (Mean Reversion)
*   Volume Weighted Average Price (VWAP)
*   Time Weighted Average Price (TWAP)
*   Percentage of Volume (POV)
*   Implementation Shortfall

[Technical Inicators](https://www.fidelity.com/learning-center/trading-investing/technical-analysis/technical-indicator-guide/overview)
 *   Simple Moving Average (SMA)
 *   Moving Average Convergence/Divergence (MACD)
 *   Commodity Channel Index (CCI)
 *   Relative Strength Index (RSI)
 *   Stochastic
 *   Bollinger Bands
 *   Pivot Points
 *   PSAR
 *   Ichimoku Kinko Hyo.

# App Idea Questions
------------------
##  Benefits of a self contained economy/fictional world?
*   Real Data will create the best expeierence and learning experience.

## Benefits of real-world scenarios?
*   Real World  Learning for wealth building
*   Can compare to real traders and fund
*   Keeps things interesting (You never know what will happen)
*   Users can research on their own and and not in the framework of our simulation

## What are the features of a game? How does the theme of a stock market change that?
*  Social               Compare earning with friends
*  Build Reputation     Compare your portfolio to a reputable fundmangers - Earn game determined Star Rating on your portfolio.
*  Win Money            Earn the ability to trade on margin
*  Win Money            Combine competitions like the comptetitors

## What legalities play into a stock market game? Into a web application?
* Why did they shutdown all those fantasy footbal leagues, they used real world data and made money?




### User Workflow
* User Sign Up / Log In
* User gets to start 10,000 
* If user starts to loose money they can get loans from other users/friends
* 
