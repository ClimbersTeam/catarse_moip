# CatarseMoip

Catarse moip integration with [Catarse](http://github.com/danielweinmann/catarse) crowdfunding platform

## Installation

Add this lines to your Catarse application's Gemfile:

    gem 'catarse_moip'

And then execute:

    $ bundle

## Usage

Configure the routes for your Catarse application. Add the following lines in the routes file (config/routes.rb):

    mount CatarseMoip::Engine => "/", :as => "catarse_moip"

### Configurations

Create this configurations into Catarse database:

    moip_uri, moip_token and moip_key

In Rails console, run this:

    Configuration.create!(name: "moip_uri", value: "https://desenvolvedor.moip.com.br/sandbox")
    Configuration.create!(name: "moip_token", value: "TOKEN")
    Configuration.create!(name: "moip_key", value: "KEY")

## Development environment setup

Clone the repository:

    $ git clone git://github.com/devton/catarse_moip.git

Add the catarse code into test/dummy:

    $ git submodule add git://github.com/danielweinmann/catarse.git test/dummy

Copy the Catarse's gems to Gemfile:

    $ cat test/dummy/Gemfile >> Gemfile

And then execute:

    $ bundle

## Troubleshooting in development environment

Remove the admin folder from test/dummy application to prevent a weird active admin bug:

    $ rm -rf test/dummy/app/admin

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request


This project rocks and uses MIT-LICENSE.
