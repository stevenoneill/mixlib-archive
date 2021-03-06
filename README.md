# Mixlib::Archive

[![Build Status Master](https://travis-ci.org/chef/mixlib-archive.svg?branch=master)](https://travis-ci.org/chef/mixlib-archive) [![Gem Version](https://badge.fury.io/rb/mixlib-archive.svg)](https://badge.fury.io/rb/mixlib-archive)

A very simple gem to extract archives.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'mixlib-archive'
```

And then execute:

```shell
$ bundle
```

Or install it yourself as:

```shell
$ gem install mixlib-archive
```

## Usage

To extract an archive

```ruby
require "mixlib/archive"
tar = Mixlib::Archive.new("/path/to/tar")
tar.extract("/destination/directory")
```

To create an archive

```ruby
require "mixlib/archive"
tar = Mixlib::Archive.new("/path/to/foo.tar.gz")
tar.create(%w{ file.rb file2.rb }, gzip: true)
```

## Development

After checking out the repo, run `bundle` to install dependencies. Then, run `bundle exec rake spec` to run the tests. You can also run `bundle console` for an interactive prompt that will allow you to experiment.

## Documentation

All documentation is written using YARD. You can generate a by running:

```
rake docs
```

## Contributing

For information on contributing to this project please see our [Contributing Documentation](https://github.com/chef/chef/blob/master/CONTRIBUTING.md)

## License & Copyright

- Copyright:: Copyright (c) 2017-2018 Chef Software, Inc.
- License:: Apache License, Version 2.0

```text
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
