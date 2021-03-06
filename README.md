# Adminlogs

## Installation

You can install the package in to a Laravel app that uses [Nova](https://nova.laravel.com) via composer:

```bash
composer require novagraphix/admin-logs
```

**LogViewer** support only the **daily** log channel, so make sure that the `LOG_CHANNEL` is set to `daily` instead of `stack` in your `.env` file.

For Laravel 5.5 and below, set this in your `.env` file

`
APP_LOG=daily
`

Next up, you must register the tool with Nova. This is typically done in the `tools` method of the `NovaServiceProvider`.

```php
// in app/Providers/NovaServiceProvider.php

public function tools()
{
    return [
        // ...
        new \Novagraphix\NovaLogViewer\Tool(),
    ];
}
```

### Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Credits

- [ARCANEDEV](https://github.com/ARCANEDEV/LogViewer)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
