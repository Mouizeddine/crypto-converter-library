# crypto-prices-converter

**crypto-prices-converter** is an npm package that provides a simple way to retrieve cryptocurrency prices and convert them into different fiat currencies. It supports various cryptocurrencies, including Bitcoin, Ethereum, Binance Coin (BNB), Ripple (XRP), and more. The package requires the currency names to be specified in the format of lowercase ISO 4217 currency codes (e.g., "usd" for United States Dollar).

# Installation

To install **crypto-prices-converter**, use npm:

```bash
npm install crypto-prices-converter
```

# Usage

To use the package, you need to require the **crypto-prices-converter** module:

```js
const { convertCurrency, convertCrypto } = require("crypto-prices-converter");
```

The **getCryptoPrice** function allows you to retrieve the price of a cryptocurrency in a specific fiat currency. It takes two parameters: the cryptocurrency symbol and the fiat currency code. Here's an example:

```js
console.log(getCryptoPrice("bitcoin", 2, "usd"));
```

The package provides two functions: **convertCurrency** and **convertCrypto**.

**convertCurrency(currencyCode, quantity, cryptoName)**
This function converts a specified quantity of a cryptocurrency into the specified fiat currency. It takes three parameters: the target fiat currency code, the quantity of the cryptocurrency, and the name of the cryptocurrency. Here's an example:

```js
const { convertCurrency } = require("crypto-prices-converter");

(async () => {
  try {
    const cryptoQuantity = await convertCurrency("usd", 2, "bitcoin");
    console.log(cryptoQuantity);
  } catch (err) {
    console.error(err);
  }
})();
```
This example converts 2 Bitcoins into US Dollars (USD) and logs the converted quantity to the console.

**convertCrypto(cryptoName, quantity, currencyCode)**
This function converts a specified quantity of a cryptocurrency into the specified fiat currency. It takes three parameters: the name of the cryptocurrency, the quantity of the cryptocurrency, and the target fiat currency code. Here's an example:

```js
const { convertCrypto } = require("crypto-prices-converter");

(async () => {
  try {
    const totalCryptoPrice = await convertCrypto("bitcoin", 2, "usd");
    console.log(totalCryptoPrice);
  } catch (err) {
    console.error(err);
  }
})();
```
This example calculates the total price of 2 Bitcoins in US Dollars (USD) and logs the result to the console.

# Repository

For more information and updates, you can visit the GitHub repository of **crypto-prices-converter**:

**https://github.com/Mouizeddine/crypto-converter-library**

Feel free to explore the repository, contribute, or submit any issues or feature requests.
