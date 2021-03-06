doctrine-functions
==================

Additional DQL functions for Doctrine2

### Numeric functions

* `RAND()`

Installation
------------

Just add the package to your `composer.json`

```json
{
    "require": {
        "morontt/doctrine-functions": "dev-master"
    }
}
```

Integration
-----------

### 1) Doctrine Only

According to the [Doctrine documentation](http://docs.doctrine-project.org/en/latest/cookbook/dql-user-defined-functions.html) you can register the functions in this package this way.

```php
<?php
$config = new \Doctrine\ORM\Configuration();
$config->addCustomDatetimeFunction('rand', 'Morontt\DQL\Numeric\Rand');
?>
```

### 2) Using Symfony 2

With symfony 2 you can register yout functions in the `config.yml` file.

```yaml
doctrine:
    orm:
        entity_managers:
            default:
                dql:
                    numeric_functions:
                        rand: Morontt\DQL\Numeric\Rand
```
