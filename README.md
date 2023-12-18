# Nasdaq Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Nasdaq Scraper](https://oxylabs.io/products/scraper-api/web/nasdaq?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Nasdaq website effortlessly. This brief guide explains how an Nasdaq Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Nasdaq results by providing your own URLs to our service. We can return the HTML for any Nasdaq page you like.

#### Python code example

The example below illustrates how you can get HTML of Nasdaq page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.nasdaq.com/market-activity'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/nasdaq-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\n<!DOCTYPE html>\n<html  lang=\"en\" dir=\"ltr\" prefix=\"content: http://purl.org/rss/1.0/modules/content ... </html>",
      "created_at": "2023-12-18 10:37:26",
      "updated_at": "2023-12-18 10:37:29",
      "page": 1,
      "url": "https://www.nasdaq.com/market-activity",
      "job_id": "7142462862273860609",
      "status_code": 200
    }
  ]
}
```
With our Nasdaq Scraper, you can easily pull public data from any Nasdaq webpage. Gather necessary financial details, including stock prices, dividend yields, or company profiles, to effectively evaluate the market and gain a competitive edge. If you need assistance, our support team is available through live chat, or you may email us at hello@oxylabs.io.