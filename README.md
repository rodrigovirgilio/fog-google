# Fog::Google

[![Gem Version](https://badge.fury.io/rb/fog-google.svg)](http://badge.fury.io/rb/fog-google) [![Build Status](https://travis-ci.org/fog/fog-google.svg?branch=master)](https://travis-ci.org/fog/fog-google) [![Dependency Status](https://gemnasium.com/fog/fog-google.svg)](https://gemnasium.com/fog/fog-google) [![Coverage Status](https://img.shields.io/coveralls/fog/fog-google.svg)](https://coveralls.io/r/fog/fog-google) [![Code Climate](https://codeclimate.com/github/fog/fog-google.png)](https://codeclimate.com/github/fog/fog-google) [![Stories in Ready](https://badge.waffle.io/fog/fog-google.png?label=ready&title=Ready)](https://waffle.io/fog/fog-google)

Fog currently supports two Google Cloud services: [Google Compute Engine](https://developers.google.com/compute/) and [Google Cloud Storage](https://developers.google.com/storage/). The main maintainer for the Google sections is @icco.

## Storage

Google Cloud Storage originally was very similar to Amazon's S3. Because of this, Fog implements the [XML GCS API](https://developers.google.com/storage/docs/xml-api-overview). We eventually want to move to the new [JSON API](https://developers.google.com/storage/docs/json_api/), once it has similar performance characteristics to the XML API. If this migration interests you, send us a pull request!

## Compute

Google Compute Engine is a Virtual Machine hosting service. Currently it is built on version [v1](https://developers.google.com/compute/docs/reference/v1/) of the GCE API.

Our implementation of the API currently supports

 * Server creation, deletion and bootstrapping
 * Persistent Disk creation and deletion
 * Image lookup
 * Network and Firewall configuration
 * Operations
 * Snapshots
 * Instance Metadata
 * Project Metadata

Features we are looking forward to implementing in the future:

 * Image creation
 * Load balancer configuration

If you are using Fog to interact with GCE, please keep Fog up to date and [file issues](https://github.com/fog/fog-google/issues) for any anomalies you see or features you would like.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'fog-google'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install fog-google

### Other setup

#### SSH-ing into instances

If you want to be able to bootstrap SSH-able instances, (using `servers.bootstrap`,) be sure you have a key in `~/.ssh/id_rsa` and `~/.ssh/id_rsa.pub`.

## Contributing

1. Fork it ( https://github.com/fog/fog-google/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

It's worth noting that, if you're looking through the code, and you'd like to know the history of a line, you may not find it in the history of this repository, since most of the code was extracted from [fog/fog].  So, you can look at the history from commit [fog/fog#c596e] backward for more information.
