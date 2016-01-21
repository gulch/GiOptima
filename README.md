# GiOptima

- Image smart resize
- Convert to WEBP format
- Extends Imagick Class

# giOptima
Package for image smart resize with convert to WEBP optionaly.

## Install

You will need [Composer](http://getcomposer.org) installed.

Add to your **composer.json** file this git repo
```bash
"repositories":[
    {
	      "type": "git",
	      "url": "http://github.com/gulch/gioptima"
    }
]
```
and add to **require** section
```bash
"require": {
    "gulch/gioptima": "dev-master"
}
```
and finally run
```bash
composer update
```

## Usage

```php
require 'vendor/autoload.php';

use gulch\GiOptima;

$i = new GiOptima('/path/to/image.jpg');
// Resize to 400x300
$i->smartResize(400,300);
// Save image
$i->writeImage('/path/to/resized-image.jpg');

// convert to WEBP image format
$i->convertToWEBP();
$i->writeImage('/path/to/resized-image.webp');
```
