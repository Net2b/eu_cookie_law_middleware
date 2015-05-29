# EuCookieLawMiddleware

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/eu_cookie_law_middleware`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'eu_cookie_law_middleware', github: 'net2b/eu_cookie_law_middleware'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install eu_cookie_law_middleware

## Usage

### Rails

In your `config/application.rb`:

```ruby
config.middleware.use EuCookieLawMiddleware

# or by passing some options:

config.middleware.use EuCookieLawMiddleware, {
  template_path: "#{__dir__}/eu_cookie_law_template.erb", # customize the html/behavior
  reload_code: Rails.env.development?,                    # reload the template in development
}
```

### Rack

In your `config.ru`:

```ruby
use EuCookieLawMiddleware

# or by passing some options:

use EuCookieLawMiddleware, {
  template_path: "#{__dir__}/eu_cookie_law_template.erb", # customize the html/behavior
  reload_code: Rails.env.development?,                    # reload the template in development
}
```



## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release` to create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

1. Fork it ( https://github.com/[my-github-username]/eu_cookie_law_middleware/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
