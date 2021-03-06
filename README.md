# Yu

A container framework based on docker-compose

## Installation

Install the CLI:

```bash
$ gem install yu
```

## Get started
```bash
$ mkdir -p new_system && cd new_system
$ yu service web api worker1
$ yu build
$ yu start
```

You can then see your running containers here:

```bash
$ docker-compose ps
$ docker-compose logs
```

## Usage

```bash
yu --help
# Check your system is ready to use yu
yu doctor
# Reset everything
yu reset
# Run all tests
yu test
# Test specific service(s)
yu test api
# Get a bash shell for a service
yu shell web
# Get a bash shell for testing a service
yu shell --test api
# Build base images for all services
yu build
# Build base image for specific service(s)
yu build api web
# Restart all containers
yu restart
# Restart specific container(s)
yu restart web
# Recreate container for service(s)
yu recreate api web
# Generate scaffold for new service(s)
yu service worker1
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release` to create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

1. Fork it ( https://github.com/[my-github-username]/yu/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
