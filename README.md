# Rubocop Config

Add the `rubocop-rails` gem to your project's `Gemfile` inside the `:development` and `:test` groups.

```
# If you already have a :development and :test block in your Gemfile, just add the gem there.

group :development, :test do
  gem 'rubocop-rails`
end

```

Add this to your Rubocop config

```
inherit_from:
  - https://raw.githubusercontent.com/XERAEN/rubocop-config/master/.rubocop.yml
```

Once you run Rubocop, it will cache the remote config locally.  We don't want to commit that cache
to our repositories, so add this to your `.gitignore`

```
# Ignore local cache of remote Rubocop config
.rubocop-https---raw-githubusercontent-com-XERAEN-rubocop-config-master--rubocop-yml
```

Install the new gem

```
bundle install
```

Now you can use Rubocop

```
bundle exec rubocop
```
