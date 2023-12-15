# Yandex Scraper

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[Yandex Scraper](https://oxylabs.io/products/scraper-api/serp/yandex) allows you to collect localized data from Yandex search results pages (SERPs) in real time without any blocks on a large scale.

Follow this guide to scrape Yandex search results using our [Scraper API](https://oxylabs.io/products/scraper-api). 

### How it works

You can receive Yandex search results by providing URLs to our service or using [scraping parameters](https://developers.oxylabs.io/scraper-apis/serp-scraper-api/yandex) to let us form them on our end. The API returns an HTML or structured JSON of any Yandex page.

#### Python code example

The example below shows how to get a result from a Yandex SERP in HTML format.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
   'source': 'yandex',
   'url': 'https://yandex.com/search/?text=nike&'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('YOUR_USERNAME', 'YOUR_PASSWORD'), #Your credentials go here
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with results.
pprint(response.json())
```

Code samples for other programming languages are [here](https://github.com/oxylabs/yandex-scraper/tree/main/code%20examples).

#### Output example

```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html lang=\"en\">\n<head>...</script></body>\n</html>\n",
      "created_at": "2023-01-16 09:36:39",
      "updated_at": "2023-01-16 09:36:42",
      "page": 1,
      "url": "https://yandex.com/search/?text=nike&",
      "job_id": "7020685239269769217",
      "status_code": 200
    }
  ]
}
```

Use Oxylabs' Yandex Scraper and let us handle infrastructure management and web unblocking, allowing you to concentrate on the essentials – data and its analysis.

If you have any inquiries, reach out to us at hello@oxylabs.io or use live chat through our website.
