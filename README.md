# TTY
[![Build Status](https://secure.travis-ci.org/peter-murach/tty.png?branch=master)][travis] [![Code Climate](https://codeclimate.com/badge.png)][codeclimate]

[travis]: http://travis-ci.org/peter-murach/tty
[codeclimate]: https://codeclimate.com/github/peter-murach/tty

Toolbox for developing CLI clients.

## Features

Jump-start development of your command line app:

* Fully customizable table rendering with an easy-to-use API.
  (status: In Progress)
* Terminal output colorization. (status: TODO)
* Terminal & System detection utilities. (status: TODO)
* Text alignment/padding and diffs. (status: TODO)
* Shell user interface. (status: TODO)
* No dependencies to allow for easy gem vendoring.

## Installation

Add this line to your application's Gemfile:

    gem 'tty'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install tty

## Usage

### Table

To instantiate table

```ruby
  table = TTY::Table.new ['Header 1', 'Header 2']
```

Table behaves like an array so `<<` and similar methods can be used

```ruby
  table << ['a1', 'a2', 'a3']
  table << ['b1', 'b2', 'b3']
```

or pass your rows in a block

```ruby
  table = TTY::Table.new header: ['Header 1', 'Header 2'] do |t|
    t << ['a1', 'a2', 'a3']
    t << ['b1', 'b2', 'b3']
  end
```

And then to print do

```ruby
  table.to_s   #  =>  a1  a2  a3
               #      b1  b2  b3
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Copyright

Copyright (c) 2012 Piotr Murach. See LICENSE for further details.