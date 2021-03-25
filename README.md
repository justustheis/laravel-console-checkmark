# laravel-console-checkmark is a checkmark style output for laravel console tasks
![Maintenance](https://img.shields.io/maintenance/yes/2021)
![Packagist](https://img.shields.io/packagist/dt/justustheis/laravel-console-checkmark)
![Packagist Version](https://img.shields.io/packagist/v/justustheis/laravel-console-checkmark)
![GitHub issues](https://img.shields.io/github/issues/justustheis/laravel-console-checkmark)
![GitHub](https://img.shields.io/github/license/justustheis/kaish)

![LaravelConsoleCheckmark](https://user-images.githubusercontent.com/7760415/112520912-38a9d180-8d9c-11eb-86b9-fdbfbdb401bb.png)

> This package is highly inspired by and partly forked from [nunomaduro/laravel-console-task](https://github.com/nunomaduro/laravel-console-task)

## About Laravel Console Checkmark

Laravel Console Checkmark is a fork of Laravel Console Task created by [Nuno Maduro](https://github.com/nunomaduro). His package is an output method for Laravel Console Commands. This fork adds the functionality to output sub tasks or print status information about the main task.

## Installation
> **Requires:**
- **[PHP ^7.4|^7.0](https://php.net/releases/)**
- **[Laravel ^6.0|^7.0|^8.0](https://github.com/laravel/laravel)**


## Installation

> **Requires:**
> - **[PHP 7.2.5+](https://php.net/releases/)**
> - **[Laravel 6.0+](https://github.com/laravel/laravel)**

Require Laravel Console Checkmark using [Composer](https://getcomposer.org):

```bash
composer require justustheis/laravel-console-checkmark
```

## Usage

```php
class LaravelInstallCommand extends Command
{
    /**
     * Execute the console command.
     *
     * @return void
     */
    public function handle()
    {
        $this->task('Installing Laravel', function (ConsoleCheckmarkOutput $output) {
            $output->text('Normal style text');
            $output->success('A success message');
            $output->error('A error message');
            $output->caution('A caution message');
            $output->comment('A comment message');
            $output->note('A magenta colored note message');
        });
    }
}
```

## License

Laravel Console Checkmark is an open-sourced software licensed under the [MIT license](LICENSE.md).
