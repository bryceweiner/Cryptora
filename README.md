# Cryptora 3

Cryptora is an easy-to-use Telegram bot service that can retrieve cryptocurrency data and news on demand.

The changes in Version 3 include:

- Significantly cleaned up and rewritten code for faster performance, improved readability, and less code duplication
- Minor bugs fixed all around, including coin logos not showing up
- Fully updated and ready for the new CoinMarketCap Professional API
- Now sources up to 50 news articles from a variety of cryptocurrency news sites, not just the latest 10 headlines from CoinDesk
- Allows users to send the list of the top cryptocurrencies by market capitalization and global statistics to a chat, rather than just viewing it
- Allows users to retrieve Coinbase Pro (formerly GDAX) prices for Ethereum Classic

... and much more!

## Features

*Refer to "Supported Commands" to see how to use these features.*

- **Look up cryptocurrencies.** Find the price (and other useful data) of thousands of cryptocurrencies, just by typing the name or the shorthand abbreviation.
- **Get historical data.** Find the low, high, opening, and closing price of thousands of cryptocurrencies on a given date, as well as the market capitalization.
- **See global statistics.** See statistics across all cryptocurrencies, including the global market cap, Bitcoin's percentage share of the global market cap, the number of active currencies, and more.
- **Get real-time exchange data from Coinbase Pro.** See the trading price of Bitcoin, Litecoin, Ethereum, Ethereum Classic, and Bitcoin Cash on Coinbase Pro (formerly GDAX), one of the leading cryptocurrency exchanges.
- **Calculations made easy.** Instantly convert cryptocurrency amounts to U.S. dollars, and vice versa.
- **Browse the latest cryptocurrency news.** Read and share news from a variety of cryptocurrency news sites.
- **View the rankings.** See the top cryptocurrencies and their prices at any given moment, sorted by market capitalization.

## Using Cryptora

Using Cryptora is easy. In any Telegram chat, simply type `@CryptoraBot` and then any of the commands below. The requested information will pop up as a list on your screen, and you can tap on a result to share it with your chat. You can also create a new private chat with Cryptora if you'd like to interact with it separately.

To locally host Cryptora, you must create a `tokens.txt` file that holds your CoinMarketCap and Telegram Bot API keys. The format is below:

```
CMC_TOKEN==your CoinMarketCap API key here
BOT_TOKEN==your Telegram Bot API key here
```
Once this file is created, Cryptora will automatically parse and use the keys where necessary.

## Supported Commands

In a Telegram chat, type `@CryptoraBot` and then any of these commands to use Cryptora:

- `[cryptocurrency]` – Type the name of any cryptocurrency, and Cryptora will retrieve essential information (price, market cap, circulating supply, and 24 hour percent change) and display it in a list. You can also type the cryptocurrency's symbol. For example, you can type `bitcoin` or `BTC` to get essential information about Bitcoin. The bot is not case sensitive, so you can type in any valid cryptocurrency name or its symbol in lower case or upper case. You can also type multiple cryptocurrencies, separated by commas, and send a list of cryptocurrency prices, percent changes, or market capitalizations in a single message. Cryptora automatically filters out duplicate and invalid entries. So, typing `xrp, iota, xmr, nano, bitcoin` will get you a list of their prices, market capitalizations, and percent changes that you can share with a chat.

- `news` - Retrieve the latest headlines from a variety of cryptocurrency news sites, and display them in a list. You can choose to share the article with your chat, or you can browse the latest cryptocurrency headlines. 

- `global` - Retrieve global statistics from CoinMarketCap, including the total market capitalization, the total 24 hour volume, bitcoin's dominance, and the number of active cryptocurrencies and markets.

- `coinbase pro` - Retrieve the trading price of Bitcoin, Bitcoin Cash, Litecoin, Ethereum, and Ethereum Classic from the Coinbase Pro trading exchange.

- `[cryptocurrency] [date]` - Type this command, replacing `[cryptocurrency]` with your desired cryptocurrency, and `[date]` with a date formatted in `MM/DD/YYYY` format (or `Month Day, Year` format), and Cryptora will retrieve the high, low, opening, and closing price - as well as the market capitalization - of the cryptocurrency on that date, if data is available. Relative dates work as well, so typing `ethereum two weeks ago` or `ethereum yesterday` will get you information about ethereum two weeks ago and yesterday, respectively.

- `top [x]` - Type this command (replace `[x]` with any number less than or equal to 50) to see the top *x* cryptocurrencies, ranked by their market capitalization.

- `[x] [cryptocurrency]` - Type this command (replace `[x]` with any number, and `[cryptocurrency]` with your desired cryptocurrency) to instantly convert an amount of cryptocurrency to U.S. dollars.

- `$[x] [cryptocurrency]` - Type this command (replace `[x]` with any number, and `[cryptocurrency]` with your desired cryptocurrency) to instantly convert an amount of U.S. dollars to the desired cryptocurrency.


## How it was built

Cryptora was built using the [python-telegram-bot](https://github.com/python-telegram-bot/python-telegram-bot) framework. Data is retrieved from [CoinMarketCap](https://coinmarketcap.com), using a combination of API access and webscraping. News articles are retrieved from [CryptoCompare](https://cryptocompare.com). The bot is hosted on RedHat OpenShift.

## Acknowledgements

Cryptora's feature set would not have been possible without the following Python packages: Dateparser, BeautifulSoup4, Datefinder, and coinbase-pro. Thank you to the developers who have created and maintained these super useful modules.
