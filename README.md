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

require_once 'URLScraper.php';

$result = URLScraper::get("https://bertmaurau.be/");

```

Will result in

```

array (size=7)
  'url' => string 'https://bertmaurau.be/' (length=22)
  'domain' => string 'bertmaurau.be' (length=13)
  'title' => string 'Bert Maurau' (length=11)
  'description' => string 'Hello World!' (length=12)
  'image' => string 'https://bertmaurau.be/assets/img/profile.jpg' (length=44)
  'tags_meta' => 
    array (size=5)
      'viewport' => string 'width=device-width, initial-scale=1.0' (length=37)
      'description' => string 'Bert Maurau, a 25 year old, Belgium-based Back-End Web- & Mobile Developer!' (length=75)
      'author' => string 'Bert Maurau' (length=11)
      'keywords' => string 'web,design,html,css,html5,development,bert,maurau,bert maurau,portfolio,profile,website,personal,angularjs,php,mysql,ionic,javascript' (length=133)
      'google-site-verification' => string 'uAKydo4-4PHMWl-c093G0g70pqQjozOWGGqc7PDCcwk' (length=43)
  'tags_og' => 
    array (size=3)
      'title' => string 'Bert Maurau' (length=11)
      'image' => string 'https://bertmaurau.be/assets/img/profile.jpg' (length=44)
      'description' => string 'Hello World!' (length=12)


```