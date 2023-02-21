![Logo](admin/logparser.png)
# ioBroker.logparser

[![NPM version](http://img.shields.io/npm/v/iobroker.logparser.svg)](https://www.npmjs.com/package/iobroker.logparser)
[![Downloads](https://img.shields.io/npm/dm/iobroker.logparser.svg)](https://www.npmjs.com/package/iobroker.logparser)
![Number of Installations (latest)](http://iobroker.live/badges/logparser-installed.svg)
![Number of Installations (stable)](http://iobroker.live/badges/logparser-stable.svg)
[![Dependency Status](https://img.shields.io/david/iobroker-community-adapters/iobroker.logparser.svg)](https://david-dm.org/iobroker-community-adapters/iobroker.logparser)
[![Known Vulnerabilities](https://snyk.io/test/github/iobroker-community-adapters/ioBroker.logparser/badge.svg)](https://snyk.io/test/github/iobroker-community-adaptersioBroker.logparser)

[![NPM](https://nodei.co/npm/iobroker.logparser.png?downloads=true)](https://nodei.co/npm/iobroker.logparser/)

**Tests:** [![Travis-CI](http://img.shields.io/travis/iobroker-community-adapters/ioBroker.logparser/master.svg)](https://travis-ci.org/iobroker-community-adapters/ioBroker.logparser)

## Log Parser for all ioBroker adapters

This adapter parses (filters) all logs of ioBroker adapters and provides the results as JSON in states for each filter as configured in the settings.
Resulting JSON can then be used in VIS for visualization. States for emptying (clearing) old logs are provided as well (like `logparser.0.filters.Homematic.emptyJson` or `logparser.0.emptyAllJson` to empty all.)

![States](docs/en/img/states.png)


## Installation

Just install the adapter regularly through the ioBroker admin interface. The adapter is both in the latest and stable repository.

## Instructions

I have included all instructions right in the admin settings of this adapter.

Also, you can read most of these instructions here as well:
* [**Basic Adapter Instructions**](https://github.com/iobroker-community-adapters/ioBroker.logparser/blob/master/admin/doc-md/start_en.md) - for German [click here (Deutsch)](https://github.com/iobroker-community-adapters/ioBroker.logparser/blob/master/admin/doc-md/start_de.md)
* [**Parser Rules (Filters)**](https://github.com/iobroker-community-adapters/ioBroker.logparser/blob/master/admin/doc-md/table-parser-rules_en.md) - for German [click here (Deutsch)](https://github.com/iobroker-community-adapters/ioBroker.logparser/blob/master/admin/doc-md/table-parser-rules_de.md)
* [**Global Blacklist**](https://github.com/iobroker-community-adapters/ioBroker.logparser/blob/master/admin/doc-md/table-global-blacklist_en.md) - for German [click here (Deutsch)](https://github.com/iobroker-community-adapters/ioBroker.logparser/blob/master/admin/doc-md/table-global-blacklist_de.md)


## Visualization Example (animated gif)

![Vis](docs/de/img/visintro.gif)

## Screenshots of adapter options

Please note that these screenshots are a snapshot and do not reflect the latest adapter options.
This is just to provide you an overview of the adapter options. 

![Log Parser Options](admin/img/option-screenshots/tab-start.png)

![Log Parser Options](admin/img/option-screenshots/tab-parser-rules.png)

![Log Parser Options](admin/img/option-screenshots/tab-further-settings.png)

![Log Parser Options](admin/img/option-screenshots/tab-vis.png)

![Log Parser Options](admin/img/option-screenshots/tab-global-blacklist.png)

![Log Parser Options](admin/img/option-screenshots/tab-expert-settings.png)


## Links and resources
* [**Log Parser ioBroker Forum Link (Splash Page)**](https://forum.iobroker.net/topic/37793/log-parser-adapter-splash-page)


## Notes
* This adapter uses Sentry libraries to automatically report exceptions and code errors anonymously to the adapter developer(s). For further details and information on how to disable this error reporting see [Sentry-Plugin Documentation](https://github.com/ioBroker/plugin-sentry#plugin-sentry). Sentry reporting is used starting with js-controller 3.0.



## Changelog

<!--
    Placeholder for the next version (at the beginning of the line):
    ### **WORK IN PROGRESS**
-->
### **WORK IN PROGRESS**
* (McM1957) Adapter has been moved to iobroker-community-adapters

### 1.1.0
* (Mic-M) Fixed issue [#15](https://github.com/Mic-M/ioBroker.logparser/issues/15) regarding regex for tab "Parser Rules", column "Blacklist"
* (Mic-M) Enhancement [#16](https://github.com/Mic-M/ioBroker.logparser/issues/16) - add specific CSS classes to any element of the JSON log per adapter option.
* (Mic-M) Major improvement: Implemented entire documentation into adapter itself to significantly improve usability.
* (Mic-M) A few improvements under the hood.


### 1.0.4
* (Mic-M) Fixed 'Today/Yesterday' updating issue - https://forum.iobroker.net/post/469757. Thanks to (Kuddel) for reporting and (Glasfaser) for further debugging.

### 1.0.3
* (Mic-M) Added [Sentry](https://github.com/ioBroker/plugin-sentry)

### 1.0.2
* (Mic-M) Added debug logging for callAtMidnight() and updateTodayYesterday()

### 1.0.1
* (Mic-M) Updated lodash dependency from 4.17.15 to 4.17.19

### 1.0.0
* (Mic-M) No changes - just prepare versioning to add adapter to stable repository per [Adapter dev docu](https://github.com/ioBroker/ioBroker.docs/blob/master/docs/en/dev/adapterdev.md#versioning)

### 0.4.11
* (Mic-M) Adapter is now in latest repository.
* (Mic-M) Removed unused adapter features 'extra tab' and 'custom state options'
* (Mic-M) Removed unused subscription to object changes

### 0.4.10
* (Mic-M) Fixed reference to 'visualization.table' for adapter instances other than instance 0.
* (Mic-M) Cleanup code.

### 0.4.9
* (Mic-M) Add option to remove script.js.Script_Name, update documentation

### 0.4.8
* (Mic-M) Fixed npm issue

### 0.4.7
* (Mic-M) Fixed translations, disabled 'supportCustoms', improved admin settings

### 0.4.6
* (Mic-M) Added error handling for invalid regex provided by user
* (Mic-M) A few other fixes/improvements under the hood

### 0.4.5
* (Mic-M) Fixed issue with merge option and other filter settings by now cloning input logObject prior to handling
* (Mic-M) Allow wildcard * for 'Whitelist AND' and 'Whitelist OR' to indicate matching all

### 0.4.4
* (Mic-M) Translations added, adapter instructions added, optimized admin interface

### 0.4.3
* (Mic-M) Fix multiple regex/string config values separated by comma

### 0.4.2
* (Mic-M) Fix issue #12 ('state is missing the required property val')
* (Mic-M) Fix issue with visualization.tableX.json and .selection. See https://forum.iobroker.net/post/408513

### 0.4.1
* (Mic-M) Fix 'Yesterday' for date, 2. Fix multiple filters, 3. Add description to settings page

### 0.4.0
* (Mic-M) Add new option "maxLength" to limit the length of each log message

### 0.3.0
* (Mic-M) initial public release

## License
MIT License

Copyright (c) 2020-2023 Mic-M, McM1957

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.