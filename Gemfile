source 'https://rubygems.org'

# Specify your gem's dependencies in health_check.gemspec

# TODO: fix shoulda version doesn't work with ruby 2.2
ruby '2.2.2' if RUBY_VERSION < '2.2.2'

gemspec

group :development, :test do
  if defined?(JRUBY_VERSION)
    gem 'jruby-openssl'
    gem 'activerecord-jdbcsqlite3-adapter'
  else
    gem 'sqlite3', "~> 1.3.7"
  end
  # run travis-lint to check .travis.yml
  gem 'travis-lint'
  platforms :ruby_18 do
    # mime-types 2.0 requires Ruby version >= 1.9.2
    gem "mime-types", "< 2.0"
  end

end

