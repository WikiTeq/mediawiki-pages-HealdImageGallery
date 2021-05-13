# HEALD Image Gallery

Stylizes the Mediawiki image gallery as a responsive navigational element.

![image](https://user-images.githubusercontent.com/62721134/118121928-70bfaf00-b3f2-11eb-9961-08b056dcebe7.png)

# Usage 

Just wrap Mediawiki's `<gallery>` tag with `<div class="heald-gallery"></div>`:

```html
<div class="heald-gallery <!-- noheader noicon noborder -->">
<gallery mode="packed" heights="320px">
File:Test2.jpg|link=Category:Keywords|[[:File:Test2.jpg|William Rush, ''North East or Franklin Public Square, Philadelphia'', 1824.]]
File:Test3.jpg|link=Category:Places|[[:File:Test3.jpg|Alexander Jackson Davis, ''Garden Arch at Montgomery Place'', c. 1850.]]
File:Test1.jpg|link=Category:People|[[:File:Test1.jpg|Anonymous, ''Deborah Norris [Logan] Portrait'', n.d.]]
</gallery>
<div>
```
Optional classes:
* `noicon` - removes the icons
* `noheader` - removes the header text
* `noborder` - removes the borders

Parameters to the `<gallery>` tag:
* `mode` - set this to "packed"
* `heights` - set to something safe

**Note**: Limited to a 3 image gallery.

# Requirements

* PageExchange

# Setup

* Add the following to the bottom of your LocalSettings.php: 
```php
$wgPageExchangePackageFiles[] = 'https://raw.githubusercontent.com/WikiTeq/mediawiki-pages-ImageGallery-heald/master/page-exchange.json';
```
* Navigate to `Special:Packages` and install the package.
* (Optional) Run `php maintenance/runJobs.php`.

