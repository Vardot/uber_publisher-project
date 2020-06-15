[![](https://www.drupal.org/files/styles/grid-3-2x/public/project-images/UBER-Logo-Final-2109-2015%20%281%29.png)](https://www.drupal.org/project/uber_publisher)

# Uber Publisher Project

Project template for [Uber Publisher distribution](http://www.drupal.org/project/uber_publisher).


## Create an Uber Publisher project with [Composer](https://getcomposer.org/download/):

# Install with Composer

To install the dev version of Uber Publisher 7.0.x run this command:
```
composer create-project Vardot/uber_publisher-project:7.0.x-dev tmp --no-dev --no-interaction
```

Built using [Varbase](https://www.drupal.org/project/varbase), the base
 distribution delivered to you by [Vardot](https://www.vardot.com)

This distribution is sponsored and developed by [Vardot](https://www.vardot.com).
Initial building, ongoing maintenance and development.

## [Varbase 8.8.x Developer Guide](https://docs.varbase.vardot.com)

## [CHANGELOG for Uber Publisher](https://github.com/Vardot/uber_publisher/blob/8.x-6.x/CHANGELOG.md)

## [TO DO](https://github.com/Vardot/uber_publisher/blob/8.x-6.x/TODO.md)

## [General instructions on how to update Uber Publisher](https://github.com/Vardot/uber_publisher/blob/8.x-6.x/UPDATE.md)




# Notices

### Requiring Drupal Modules with Dev Version in varbase-project/composer.json
You will notice that we're requiring some Drupal modules in dev state with its commit hash. This is because of a bug in Composer. And it was discussed in https://github.com/composer/composer/issues/6366 and is highlighted in Composer documentation as follows:

> Note: This feature has severe technical limitations, as the composer.json metadata will still be read from the branch name you specify before the hash. You should therefore only use this as a temporary solution during development to remediate transient issues, until you can switch to tagged releases. The Composer team does not actively support this feature and will not accept bug reports related to it.

Therefore, our workaround, is to explicitly tag the commit hash we want in `varbase-project/composer.json`. This means that ALL Drupal modules dependencies which are in dev stage, are duplicated as a requirement for composer in both `varbase-project/composer.json` and `varbase/composer.json`.

This workaround will remain, until either a module has a tag (that we can tag without the commit hash) or a fix is provided from composer - hopefully in the near future!

Read more at: https://www.drupal.org/node/2903606#comment-12230769
