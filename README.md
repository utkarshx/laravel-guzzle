# Laravel - Guzzle 6 (or 5) Service Provider

laravel guzzle service provider

## Install With Composer:

### Guzzle ~5.0
```sh
composer require utkarshx/laravel-guzzle-provider ~6.0
```

Or manualy in composer.json:
```json
"require": {
    "utkarshx/laravel-guzzle-provider": "~5.0"
}
```

### Guzzle ~6.0
```sh
composer require utkarshx/laravel-guzzle-provider ~6.0
```

Or manualy in composer.json:
```json
"require": {
    "utkarshx/laravel-guzzle-provider": "~6.0"
}
```

## Register Service Provider

*/configs/app.php*

```php
    ...
    'providers' => [

        /*
         * Laravel Framework Service Providers...
         */
        ...

        /*
         * Application Service Providers...
         */
        ...
        'Utkarshx\Laravel\Providers\Guzzle'
    ],
```


## Enable Facade

*/configs/app.php*

```php
    ...
    'aliases' => [
        ...
        'Guzzle' => 'Utkarshx\Laravel\Facades\Guzzle'
    ],
```

## Usage

### Send request

```php

  $response = \Guzzle::get('https://google.com');
```


### Get instance

```php
    $client = app()->offsetGet('guzzle');
    $client = \Illuminate\Container\Container::getInstance()->offsetGet('guzzle');
    $client = \Utkarshx\Laravel\Facades\Guzzle::getFacadeRoot();
    $client = \Guzzle::getFacadeRoot();
```
