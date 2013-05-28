source 'https://rubygems.org'

puppetversion = ENV.key?('PUPPET_VERSION') ? "= #{ENV['PUPPET_VERSION']}" : ['>= 3.1.1']
gem 'puppet', puppetversion

facterversion = ENV.key?('FACTER_VERSION') ? "= #{ENV['FACTER_VERSION']}" : ['>= 1.7.1']
gem 'facter', facterversion

gem 'rake'
gem 'rspec'
gem 'puppet-lint', '>=0.3.2'
gem 'rspec-puppet', '>=0.1.6'
gem 'librarian-puppet', '>=0.9.9'
gem 'puppetlabs_spec_helper', '>=0.4.1'
gem 'rspec-hiera-puppet', '>=1.0.0'
