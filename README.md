# Shaarli Via

Shaarli via is a tiny plugin which offers you the possibility to indicate the original source of a link that you share.

It adds 2 fields in the link edition page for the label and the url of the source.
The source is then displayed using the `link_plugin` placeholder wherever it is placed by the current theme.

A Font Awesome icon is displayed at the left of the original source according to its host:
* `(|mobile.|www.)twitter.com` uses `fa-twitter`
* Any other host uses `fa-share`

Starting with version 0.2, this plugin is able to take original source url from
query string using `original_url` parameter.

Starting with wallabag 2.3, original source url is forwarded when sharing
articles to Shaarli.

## Installation
### Via Git
If you use git you can run the following command from within the `plugins` folder of your Shaarli installation:

```shell
git clone https://github.com/kalvn/shaarli-plugin-via via
```

### Manually
Create the folder `plugins/via` in your Shaarli installation and copy all the files in it.

## Activation
Then, activate the plugin through the plugin administration panel or edit the `data/config.php` file and add `via` in the array `$GLOBALS['config']['ENABLED_PLUGINS']`. For example, if you already have the Wallabag plugin installed, it'll look like this:

```php
$GLOBALS['config']['ENABLED_PLUGINS'] = array (
  'wallabag',
  'via'
);
```

*Please note that it's a very first version which may need improvements.*
