# Kanopi Event Calendar


CONTENTS OF THIS FILE
---------------------

 * Introduction
 * Requirements
 * Installation
 * Configuration
 * Maintainers

INTRODUCTION
------------
Drupal 8 module that installs an Events Content Type and Calendar views.

**Content Types**

  * Event

The event content types is configured to have proper Meta tags and Schema.org
markup; preconfigured friendly URLs; and an organized administration.  Once 
installed, you have control over changing what is in configuration, and 
overriding templates and styles in your theme.

**Taxonomies**

  * Event Type

Taxonomies can be used in conjunction with events to create different views.

**Views**
  * Event Calendar
  * Event Image Browser

The Event Calendar view includes a variety of ways to display your events.

REQUIREMENTS
------------

This module requires the following modules:

  * drupal:datetime
  * drupal:datetime_range
  * drupal:field
  * drupal:image
  * drupal:link
  * drupal:media
  * drupal:node
  * drupal:path
  * drupal:rest
  * drupal:serialization
  * drupal:system
  * drupal:taxonomy
  * drupal:text
  * drupal:views
  * address:address
  * calendar:calendar
  * date_recur:date_recur
  * entity_browser:entity_browser
  * entity_browser:entity_browser_entity_form
  * field_group:field_group
  * focal_point:focal_point
  * media_entity_browser:media_entity_browser
  * metatag:metatag
  * metatag:metatag_open_graph
  * metatag:metatag_twitter_cards
  * pathauto:pathauto
  * scheduler:scheduler
  * schema_metatag:schema_metatag
  * schema_metatag:schema_event

INSTALLATION
------------

  * Install the module using composer:
  * Add this repository to your composer file:
  ```
        {
          "type": "vcs",
          "url": "https://github.com/kanopi/kanopi_event_calendar"
        }
  ```
  * Add the module with dependencies:
  ```
    composer require kanopi/kanopi_event_calendar --with-dependencies
  ```
  * Verify installation by visiting /admin/structure/types and seeing your new 
  Event Content type.

CONFIGURATION
-------------

  * 

MAINTAINERS
-----------

Current maintainers
  * [thejimbirch](https://www.drupal.org/u/thejimbirch)

Supporting organizations
  * [Kanopi Studios](https://www.kanopistudios.com)
