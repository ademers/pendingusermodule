# Pending User Module for Craft CMS 3.x

A Craft Module that sets all new user accounts created via a front-end registration form to pending status.

## Requirements

This module requires Craft CMS 3.0.0-RC1 or later.

## Installation

To install the module, follow these instructions.

First, you'll need to add the contents of the `app.php` file to your `config/app.php` (or just copy it there if it does not exist). This ensures that your module will get loaded for each request. The file might look something like this:
```
return [
    'modules' => [
        'pending-user-module' => [
            'class' => \modules\pendingusermodule\PendingUserModule::class,
        ],
    ],
    'bootstrap' => ['pending-user-module'],
];
```
You'll also need to make sure that you add the following to your project's `composer.json` file so that Composer can find your module:

    "autoload": {
        "psr-4": {
          "modules\\pendingusermodule\\": "modules/pendingusermodule/src/"
        }
    },

After you have added this, you will need to do:

    composer dump-autoload
 
 …from the project’s root directory, to rebuild the Composer autoload map. This will happen automatically any time you do a `composer install` or `composer update` as well.

## Pending User Module Overview

When a user account is created via a Craft 3 front-end registration form, this module sets the status of the user account to pending. An admin must then manually activate the new user account.

## Using Pending User Module

-Insert text here-

## Pending User Module Roadmap

Some things to do, and ideas for potential features:

* Update README
* Release it

Brought to you by [Andrea DeMers](http://andreademers.com)
