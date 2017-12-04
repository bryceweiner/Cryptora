# Cryptogram (beta 0.6.0)

Cryptogram is an easy-to-use Telegram bot service that can retrieve cryptocurrency data and news on demand for you, or your Telegram group.

## How it was built

Cryptogram was built using the [python-telegram-bot](https://github.com/python-telegram-bot/python-telegram-bot) framework, a powerful, easy-to-use platform for building Telegram bots in Python. Up-to-date prices are retrieved from [CoinMarketCap](http://coinmarketcap.com) using the CoinMarketCap API, while historical data is retrieved using a webscraper implemented in BeautifulSoup4. News articles are retrieved from [CoinDesk](http://coindesk.com) through its RSS feed. 
 
## Using Cryptogram

Using Cryptogram is super simple. In any Telegram chat, simply type `@Crypto_Messenger_Bot` and then your command - you do not need to add the bot to any group chat. You will receive the requested information in-line, and you can tap on a result to share it with your chat if you wish. You can also create a new private chat with Cryptogram if you'd like to interact with it separately.

## Features

*Refer to "Supported Commands" to see how to use these features.*

- **Look up cryptocurrencies.** Find the price (and other useful data) of thousands of cryptocurrencies, just by typing the name or the shorthand abbreviation.
- **Get historical data.** Find the low, high, opening, and closing price of thousands of cryptocurrencies on a given date, as well as the market capitalization.
- **Calculations made easy.** Instantly convert cryptocurrency amounts to U.S. dollars, and vice versa.
- **Browse the latest cryptocurrency news.** Read and share the 10 latest headlines from Coindesk.com.
- **View the rankings.** See the top cryptocurrencies and their prices at any given moment, sorted by market capitalization.

## Supported Commands

In a Telegram chat, type `@Crypto_Messenger_Bot` and then any of these commands to use Cryptogram:

- `[cryptocurrency]` – Type the name of any cryptocurrency, and Cryptogram will retrieve essential information (price, market cap, circulating supply, and 24 hour percent change) and display it in a list. You can also type the cryptocurrency's shorthand abbreviation. For example, you can type `bitcoin` or `BTC` to get essential information about Bitcoin. The bot is not case sensitive, so you can type in any valid cryptocurrency name or its symbol in lower case or upper case.

- `news` - Cryptogram will retrieve the latest 10 articles from CoinDesk.com and display them in a list. You can choose to share the article with your chat, or you can peruse through the headlines. 

- `historical [cryptocurrency] [date]` - Type this command (replace `[cryptocurrency]` with your desired cryptocurrency, and `[date]` with a date formatted in `MM/DD/YYYY` format), and Cryptogram will retrieve the high, low, opening, and closing price on that date, if data for the cryptocurrency is available.

- `top [x]` - Type this command (replace `[x]` with any number less than or equal to 50) to see the top *x* cryptocurrencies, ranked by their market capitalization.

- `[x] [cryptocurrency]` - Type this command (replace `[x]` with any number, and `[cryptocurrency]` with your desired cryptocurrency) to instantly convert an amount of cryptocurrency to U.S. dollars.

- `$[x] [cryptocurrency]` - Type this command (replace `[x]` with any number, and `[cryptocurrency]` with your desired cryptocurrency) to instantly convert an amount of U.S. dollars to the desired cryptocurrency.

## Acknowledgements

A special thank you to Michael Yousif (@mjyousif) and Augustine Osagie (@osagie98) for testing my bot in its beta stages and providing inspiration for new features and ideas.

Thanks to @Kylmakalle for providing an easy starter code pack to deploy the bot on Heroku.

And finally, thank you to the python-telegram-bot development team for building an easy to use Python wrapper for Telegram bots!
