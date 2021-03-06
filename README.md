# chef-grafana

[![Build Status](https://travis-ci.org/chef-cookbooks/chef-grafana.svg?branch=master)](https://travis-ci.org/chef-cookbooks/chef-grafana)

This cookbook installs and configures Grafana 2, a dashboard application for
graphite and influxdb.


Requirements
------------
#### Platforms
- Debian/Ubuntu

#### Chef
- Chef 12.1+

#### Cookbooks
- apt


## Recipes

The default recipe will install grafana 2, configure grafana.ini, and start
the service.

Other recipes:

* grafana::install - this installs grafana and starts the service, but doesn't
  perform any configuration of grafana.ini.
* grafana::configure - this configures grafana.ini.
* grafana::default_dashboards - this replaces the home dashboard with a
  different file.

## Configuration

All grafana.ini configuration is provided through attributes. Set
`node['chef-grafana']['config']['section']['config']` to set the appropriate
values. For example, if you want to enable anonymous authentication, you can
set `node['chef-grafana']['config']['auth.anonymous']['enabled']` to true.

License & Authors
-----------------

**Author:** Mark Harrison (<mharrison@chef.io>)

**Copyright:** 2008-2016, Chef Software, Inc.
```
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

