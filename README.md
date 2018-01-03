# url-scraper

Plain and simple, could use some more fine-tuning, better error handling, proper class structure etc.. But this was just a quick code for another project and wanted to share this.

Just a simple PHP URL scraper that will fetch:

 - Title
 - Description
 - Image
 - Meta Tags
 - OG Tags

## Usage

```php
// include the class
require_once __DIR__ . '/URLScraper.php';

// get the results
$result = URLScraper::get("https://bertmaurau.be/");  

echo json_encode($result, JSON_PRETTY_PRINT);
```

Will result in

```json

{
	"url": "https:\/\/bertmaurau.be\/",
	"domain": "bertmaurau.be",
	"title": "Bert Maurau",
	"description": "Hello World!",
	"image": "https:\/\/bertmaurau.be\/assets\/img\/profile.jpg",
	"tags_meta": {
		"viewport": "width=device-width, initial-scale=1.0",
		"description": "Bert Maurau, a 25 year old, Belgium-based Back-End Web- & Mobile Developer!",
		"author": "Bert Maurau",
		"keywords": "web,design,html,css,html5,development,bert,maurau,bert maurau,portfolio,profile,website,personal,angularjs,php,mysql,ionic,javascript"
	},
	"tags_og": {
		"title": "Bert Maurau",
		"image": "https:\/\/bertmaurau.be\/assets\/img\/profile.jpg",
		"description": "Hello World!"
	}
}


```
