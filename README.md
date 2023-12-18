# Coinmarketcap Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Coinmarketcap Scraper](https://oxylabs.io/products/scraper-api/web/coinmarketcap?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Coinmarketcap website effortlessly. This brief guide explains how an Coinmarketcap Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Coinmarketcap results by providing your own URLs to our service. We can return the HTML for any Coinmarketcap page you like.

#### Python code example

The example below illustrates how you can get HTML of Coinmarketcap page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://coinmarketcap.com/all/views/all/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/coinmarketcap-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\" dir=\"ltr\"><head><meta charSet=\"utf-8\"/><meta http-equiv=\"x-ua-compati ... </html>",
      "created_at": "2023-12-18 10:41:27",
      "updated_at": "2023-12-18 10:41:28",
      "page": 1,
      "url": "https://coinmarketcap.com/all/views/all/",
      "job_id": "7142463871930917889",
      "status_code": 200
    }
  ]
}
```
With our Coinmarketcap Scraper, you can easily gather public data from any Coinmarketcap web page. Acquire the necessary information about various cryptocurrencies, including their current price, market capitalization, trading volume, and historical data, to analyze market trends and gain insight for your investment strategies. If you need assistance or have any inquiries, feel free to reach out to our support team through live chat or email us at hello@oxylabs.io.