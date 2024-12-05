source "http://rubygems.org"

gemspec

rest_client = if ENV.key?('REST_CLIENT_VERSION')
                ["~> #{ENV['REST_CLIENT_VERSION']}"]
              else
                ['< 3.0']
              end

gem 'rest-client', rest_client

# load local gemfile
local_gemfile = File.join(File.dirname(__FILE__), 'Gemfile.local')
self.instance_eval(Bundler.read_file(local_gemfile)) if File.exist?(local_gemfile)
