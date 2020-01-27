Composer Project template for Canada.ca
=======================================

[![Build Status][ci-badge]][ci]

Drupal WxT codebase for `site-canada`.

## Requirements

* [Composer][composer]
* [Node][node]

## Setup

Normally you can simply run a `composer install` but at the moment you might need to run the following:

```sh
export COMPOSER_MEMORY_LIMIT=-1 && composer install
```

## Dependencies

The `composer.json` file calls the following dependencies:

* [WxT][wxt]
* [Canada Core][canada_core]
* [Canada Experiments][canada_experiments]
* [OpenPlus Migrate][openplus_migrate]
* [OpenPlus VBO][openplus_vbo]

### WxT

The [Drupal WxT][wxt] distribution is a web content management system which assists in building and maintaining innovative Web sites that are accessible, usable, and interoperable. This distribution is open source software and free for use by departments and external Web communities. This distribution relies and integrates extensively with the WET-BOEW jQuery Framework for improved accessible markup.

### Canada Core

The [Canada Core][canada_core] module houses all of the additional customization that are made on top of Drupal WxT. Any additional contributed dependencies are declared in the [composer.json][canada_core_composer] file and are installed in the [canada_core.info.yml][canada_core_info] file. Normally this can all be done in an (sub) installation profile but for the moment to reduce complexity this is the current route. All of the custom configuration for things such as `asset_injector`, `ckeditor templates`, and `webform` have been exported in the [config][canada_core_config] folder.

### Canada Experiments

The [Canada Experiments][canada_experiments] theme which itself is a sub theme of [WxT Bootstrap][wxt_bootstrap] houses all of the additional theming related customizations that are made on top of of [Drupal WxT][wxt]. Any additional contributed dependencies are declared in the [composer.json][canada_experiments_composer] file and are installed in the [canada_core.info.yml][canada_experiments_info] file. All of the custom theme configuration have been exported in the [config][canada_experiments_config] folder.

## Project

For production releases you should only ever use a stable tag.

## New Project (stable tag)

```sh
composer create-project openplus/site-canada:3.0.6 site-name
```

## New Project (dev)

```sh
composer create-project openplus/site-canada:8.x-dev site-name
```

## Maintenance

List of common commands are as follows:

| Task                                            | Composer                                               |
|-------------------------------------------------|--------------------------------------------------------|
| Latest version of a contributed project         | ```composer require drupal/PROJECT_NAME:8.*```         |
| Specific version of a contributed project       | ```composer require drupal/PROJECT_NAME:8.1.0-beta5``` |
| Updating all projects including Drupal Core     | ```composer update```                                  |
| Updating a single contributed project           | ```composer update drupal/PROJECT_NAME```              |
| Updating Drupal Core exclusively                | ```composer update drupal/core```                      |


[canada_core]:                  https://github.com/openplus/canada_core
[canada_core_composer]:         https://github.com/openplus/canada_core/blob/8.x-1.x/composer.json
[canada_core_info]:             https://github.com/openplus/canada_core/blob/8.x-1.x/canada_core.info.yml
[canada_core_config]:           https://github.com/openplus/canada_core/tree/8.x-1.x/config
[canada_experiments]:           https://github.com/openplus/canada_experiments
[canada_experiments_composer]:  https://github.com/openplus/canada_experiments/blob/8.x-1.x/composer.json
[canada_experiments_info]:      https://github.com/openplus/canada_experiments/blob/8.x-1.x/canada_core.info.yml
[canada_experiments_config]:    https://github.com/openplus/canada_experiments/tree/8.x-1.x/config
[ci]:                           https://travis-ci.com/openplus/site-canada
[ci-badge]:                     https://travis-ci.com/openplus/site-canada.svg?branch=8.x
[composer]:                     https://getcomposer.org
[node]:                         https://nodejs.org
[openplus_migrate]:             https://github.com/openplus/openplus_migrate
[openplus_vbo]:                 https://github.com/openplus/openplus_vbo
[wxt]:                          https://github.com/drupalwxt/wxt
