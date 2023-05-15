---
title: Built on the shoulders of giants
metadata:
    description: Detailed breakdown of a UserFrosting's dependencies.
taxonomy:
    category: docs
---

As detailed in a previous chapter, it's important [not to reinvent the wheel](/background/dont-reinvent-the-wheel). That's why UserFrosting depend on a number of external libraries, called dependencies. Those are written by people and organizations external to UserFrosting to provide the base needed for UserFrosting to work. They can actually be used by anyone, as they're not tied to UserFrosting. Think of those dependencies as the raw materials, like wood and concrete, you get from the hardware store to build a house. We simply "glued" them together to create awesomeness! 

While UserFrosting uses dozens of dependencies, here's a rundown of the most important one.

## Slim 4
**[Slim](https://www.slimframework.com)** is a PHP _micro framework_ that helps you quickly write simple yet powerful web applications and APIs. Slim is the backbone of UserFrosting. To be more precise, **UserFrosting _is_ a Slim Application**! 

Except for the Bakery system, which uses _Symfony Console_ (more on that later), UserFrosting uses Slim at every level to perform middleware management, routes collections and everything else needed to actually display a web page.

## PHP-DI 7
**[PHP-DI](https://php-di.org)** is a _dependency injection container_. Dependency injection is one of the fundamental pillars of modern object-oriented software design. It is used extensively throughout UserFrosting to glue all services together while maintaining . We'll explain dependency injection in detail in a later chapter. For now, it's only important to note **PHP-DI** is the dependency used by UserFrosting 5 to handle all dependency injection.

## Eloquent 8
**[Eloquent](https://laravel.com/docs/8.x/eloquent)** is part of the Laravel Framework. Eloquent makes it enjoyable to interact with a database. When using Eloquent, each database table has a corresponding "Model" that is used to interact with that table. In addition to retrieving records from the database table, Eloquent models allow you to insert, update, and delete records from the table as well.

Eloquent is one of the most powerful and easy to use tool available to interact with a Database. That is why it's been chosen as the database handler since the early version of UserFrosting.

[notice]While UserFrosting uses Eloquent, UserFrosting itself isn't a Laravel application (it's actually a _Slim_ one). While most Eloquent documentation and examples apply to UserFrosting, some key functions are different, such as the use of the `artisan` command UserFrosting doesn't support.[/notice]

## Twig 3
**[Twig](https://twig.symfony.com/doc/)** is a flexible, fast, and secure template engine for PHP. Initially developed for the Symfony framework, Twig is easy to use and provides the necessary tools to use the data generated by PHP and render the HTML page the end user get to see.

## Symfony Console 5
**[Symfony Console](https://symfony.com/doc/5.4/components/console.html)** eases the creation of beautiful and testable command line interfaces. This is used to power the **Bakery** command line interfaces tool used by UserFrosting. 

## Webpack Encore 1.7
**[Webpack Encore](https://symfony.com/doc/current/frontend.html)** wraps Webpack, providing a clean & powerful API for bundling JavaScript modules, pre-processing CSS & JS and compiling and minifying assets. Encore is a professional asset system that's a delight to use. It is used by UserFrosting to serve all CSS and Javascript files, while enabling the use of other Framework, like Vue.js, in the future.