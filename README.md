# dynamic banner using keywords

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
## explanation of parameters

| Parameter                  | Description                                                                 |
|----------------------------|-----------------------------------------------------------------------------|
| `%%CLICK_URL_ESC%%`        | A GAM macro that dynamically inserts the click URL.          |
| `%%PATTERN:oikotie_card_id%%` | Oikotie ad ID, populated from GAM targeting. |
| `%%PATTERN:oikotie_broker_id%%` | Broker ID, populated from GAM targeting.      |
| `%%PATTERN:oikotie_vendor_ad_id%%` | Vendor ad ID (kohde id/Kohdenumero/kivi-id...), populated from GAM targeting. |
| `%%PATTERN:oikotie_store_tag%%` | Store tag, populated from GAM targeting.      |
| `%%CACHEBUSTER%%`          | Ensures the URL is unique on every request to prevent caching issues.      |
