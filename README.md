# KCMS Dev Switch

[![Packagist](https://img.shields.io/packagist/v/kubeeapp/wp-stage-switcher.svg?style=flat-square)](https://packagist.org/packages/kubeeapp/wp-stage-switcher)
[![Packagist Downloads](https://img.shields.io/packagist/dt/kubeeapp/wp-stage-switcher.svg?style=flat-square)](https://packagist.org/packages/kubeeapp/wp-stage-switcher)

Allows you to switch between different environments from the admin bar.

![KCMS Dev Switch](https://cdn.kubeeapp.io/app/uploads/kcms-ds.png)

## Requirements

You'll need to have `ENVIRONMENTS` and `WP_ENV` defined in your WordPress config.

The `ENVIRONMENTS` constant must be a serialized array of `'environment' => 'url'` elements:

```php
$envs = [
  'development' => 'http://example.dev',
  'staging'     => 'http://staging.example.com',
  'production'  => 'http://example.com'
];
define('ENVIRONMENTS', serialize($envs));
```

Note: the `serialize()` call is not needed on PHP 7.0 or newer.

`WP_ENV` must be defined as the current environment:

```php
define('WP_ENV', 'development');
```

If you use [KCMS](https://github.com/kubeeapp/kcms), `WP_ENV` is already defined in the config.

## Installation

This plugin must be installed via Composer. Add kcms-ds to your project's dependencies:

```sh
composer require kubeeapp/kcms-ds
```

Or manually add it to your `composer.json`:

```json
"require": {
  "php": ">=7.2",
  "kubeeapp/cms": "5.1.1",
  "kubeeapp/kcms-ds": "~2.0"
}
```

## Support

Use the [kubeeapp Discourse](http://discourse.kubeeapp.io/) to ask questions and get support.
