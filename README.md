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
  * Add these modules with dependencies:
  ```
    composer require drupal/date_recur:dev-1.x#8bd0ca37
    composer require drupal/calendar:dev-1.x#73e2979f
    composer require kanopi/kanopi_event_calendar --with-dependencies
  ```
  * Verify installation by visiting /admin/structure/types and seeing your new 
  Event Content type.

CONFIGURATION
-------------

  * In your site's composer file, apply these patches:
  ```
  "patches": {
            "drupal/date_recur": {
                "#2902733 Default weekday checked is off by one": "https://www.drupal.org/files/issues/default_weekday_offset_fix-2902733-2.patch",
                "#2820803 Patch for calendar module integration": "https://www.drupal.org/files/issues/2820803-date-recur_calendar-integration_8.patch",
                "WIP: Remove lines from 2920803-8 to get event time working": "https://raw.githubusercontent.com/kanopi/kanopi_event_calendar/8.x-1.x/patches/date_recur--event_time.patch",
                "WIP: Support multi-day events in date_recur's calendar. Should be included in updates to 2920803-8": "https://raw.githubusercontent.com/kanopi/kanopi_event_calendar/8.x-1.x/patches/date_recur--multiday_events.patch",
                "WIP: PHP Notice on views with Recurring Date field": "https://raw.githubusercontent.com/kanopi/kanopi_event_calendar/8.x-1.x/patches/date_recur--view-notice-undefined-property.patch"
            },
            "drupal/calendar": {
                "#2699477 calendar end dates": "https://www.drupal.org/files/issues/2699477-66_0.patch",
                "#2604546 time zone handling": "https://www.drupal.org/files/issues/2604546-16.patch"
            }
        },
  ```

MAINTAINERS
-----------

Current maintainers
  * [thejimbirch](https://www.drupal.org/u/thejimbirch)
  
  With help and guidance from [akalata](https://www.drupal.org/u/akalata)

Supporting organizations
  * [Kanopi Studios](https://www.kanopistudios.com)
