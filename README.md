# dynamic banner using keywords + more
the `index.html` contains the banner with the following features:
- gets the targeting parameters to the banner from the URL
- updates content based on targeting parameters
- shows content adn video starts playing when 50% in view (with `IntersectionObserver` and `threshold: 0.5`)
- has two different links, both are tracked with GAM clickurl

## explanation of parameters

| Parameter                  | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| `%%CLICK_URL_ESC%%`        | A GAM macro that dynamically inserts the click URL.          |
| `%%PATTERN:oikotie_card_id%%` | Oikotie ad ID, populated from GAM targeting. |
| `%%PATTERN:oikotie_broker_id%%` | Broker ID, populated from GAM targeting.      |
| `%%PATTERN:oikotie_vendor_ad_id%%` | Vendor ad ID (kohde id/Kohdenumero/kivi-id...), populated from GAM targeting. |
| `%%PATTERN:oikotie_store_tag%%` | Store tag, populated from GAM targeting.      |
| `%%CACHEBUSTER%%`          | Ensures the URL is unique on every request to prevent caching issues.      |

## add to GAM as a Third party tag
```html
<iframe
    src="https://maex5.github.io/banner/?clickurl=%%CLICK_URL_ESC%%&oikotie_card_id=%%PATTERN:oikotie_card_id%%&oikotie_broker_id=%%PATTERN:oikotie_broker_id%%&oikotie_vendor_ad_id=%%PATTERN:oikotie_vendor_ad_id%%&oikotie_store_tag=%%PATTERN:oikotie_store_tag%%&cachebuster=%%CACHEBUSTER%%"
    width="160"
    height="600"
    frameborder="0"
    scrolling="no"
    style="border: none;">
</iframe>
```

## GAM preview
Open any company listing and add this after URL
```
?google_preview=APCQMr4Yi9sY8uW7ugYw8oHxwQaIAYCAgJDAssqnLQ&iu=117157013&gdfp_req=1&lineItemId=6850407285&creativeId=138499664789
```
