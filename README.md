# Oracle DB driver for Laravel 5.4 via OCI8

## Laravel-OCI8

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Software License][ico-license]](LICENSE.md)
[![Build Status][ico-travis]][link-travis]
[![Coverage Status][ico-scrutinizer]][link-scrutinizer]
[![Quality Score][ico-code-quality]][link-code-quality]
[![Total Downloads][ico-downloads]][link-downloads]

Laravel-OCI8 is an Oracle Database Driver package for [Laravel](http://laravel.com/). Laravel-OCI8 is an extension of [Illuminate/Database](https://github.com/illuminate/database) that uses [OCI8](http://php.net/oci8) extension to communicate with Oracle. Thanks to @taylorotwell.
## Documentations
- You will find user friendly and updated documentation here: [Laravel-OCI8 Docs](https://yajrabox.com/docs/laravel-oci8)
- You will find updated API documentation here: [Laravel-OCI8 API](http://yajra.github.io/laravel-oci8/api/)

## Quick Installation [Laravel 5.4]
```
$ composer require yajra/laravel-oci8:"5.4.*"
```

## Service Provider
Once Composer has installed or updated your packages you need to register Laravel-OCI8. Open up `config/app.php` and find the providers key and add:
```php
Yajra\Oci8\Oci8ServiceProvider::class,
```
> Important: Since v4.0, the package will now use `Yajra\Oci8` (capital Y) namespace from `yajra\Oci8` to follow the name standard for vendor name.

## Configuration (OPTIONAL)
Finally you can optionally publish a configuration file by running the following Artisan command.
If config file is not publish, the package will automatically use what is declared on your `.env` file database configuration.

```
$ php artisan vendor:publish --tag=oracle
```

This will copy the configuration file to `config/oracle.php`.

> Note: For [Laravel Lumen configuration](http://lumen.laravel.com/docs/configuration#configuration-files), make sure you have a `config/database.php` file on your project and append the configuration below:

```php
'oracle' => [
    'driver'        => 'oracle',
    'tns'           => env('DB_TNS', ''),
    'host'          => env('DB_HOST', ''),
    'port'          => env('DB_PORT', '1521'),
    'database'      => env('DB_DATABASE', ''),
    'username'      => env('DB_USERNAME', ''),
    'password'      => env('DB_PASSWORD', ''),
    'charset'       => env('DB_CHARSET', 'AL32UTF8'),
    'prefix'        => env('DB_PREFIX', ''),
    'prefix_schema' => env('DB_SCHEMA_PREFIX', ''),
],
```

And run your laravel installation...

## Credits

- [Arjay Angeles][link-author]
- [Jimmy Felder](https://github.com/jfelder/Laravel-OracleDB)
- [All Contributors][link-contributors]

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/tochka-developers/laravel-oci8.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/yajra/laravel-oci8/master.svg?style=flat-square
[ico-scrutinizer]: https://img.shields.io/scrutinizer/coverage/g/yajra/laravel-oci8.svg?style=flat-square
[ico-code-quality]: https://img.shields.io/scrutinizer/g/yajra/laravel-oci8.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/yajra/laravel-oci8.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/tochka-developers/laravel-oci8
[link-travis]: https://travis-ci.org/yajra/laravel-oci8
[link-scrutinizer]: https://scrutinizer-ci.com/g/yajra/laravel-oci8/code-structure
[link-code-quality]: https://scrutinizer-ci.com/g/yajra/laravel-oci8
[link-downloads]: https://packagist.org/packages/yajra/laravel-oci8
[link-author]: https://github.com/yajra
[link-contributors]: ../../contributors
