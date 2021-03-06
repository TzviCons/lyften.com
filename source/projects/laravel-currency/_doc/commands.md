---
title: Artisan Commands
template: documentation.twig::content_inner
chapter: 4
---
### Manage

Easily add, update, or delete currencies from the default storage. This is extremely helpful when there are changes to currecny data, such as symbols and such.

```
php artisan currency:manage <action> <currency>
```

**Arguments:**

```
 action              Action to perform (add, update, or delete)
 currency            Code or comma separated list of codes for currencies
```

### Updating Exchange

Update exchange rates from OpenExchangeRates.org. An API key is needed to use [OpenExchangeRates.org](http://OpenExchangeRates.org). Add yours to the config file.

```bash
php artisan currency:update
```

> Note: Yahoo has discontinued the use of their exchange rate API, so it has been removed from the package.

### Cleanup

Used to clean the Laravel cached exchanged rates and refresh it from the database. Note that cached exchanged rates are cleared after they are updated using one of the command above.

```bash
php artisan currency:cleanup
```