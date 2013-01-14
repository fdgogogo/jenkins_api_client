require File.expand_path('../lib/jenkins_api_client', __FILE__)
require File.expand_path('../lib/jenkins_api_client/version', __FILE__)
require 'rake'
require 'jeweler'

Jeweler::Tasks.new do |gemspec|
  gemspec.name         = 'jenkins_api_client'
  gemspec.version      = JenkinsApi::Client::VERSION
  gemspec.platform     = Gem::Platform::RUBY
  gemspec.date         = Time.now.utc.strftime("%Y-%m-%d")
  gemspec.require_path = 'lib'
  gemspec.executables  = `git ls-files -- bin/*`.split("\n").map{|f| File.basename(f)}
  gemspec.files        = `git ls-files`.split("\n")
  gemspec.extra_rdoc_files = ['CHANGELOG.rdoc', 'LICENSE', 'README.rdoc']
  gemspec.authors      = [ 'Kannan Manickam' ]
  gemspec.email        = [ 'arangamani.kannan@gmail.com' ]
  gemspec.homepage     = 'https://github.com/arangamani/jenkins_api_client'
  gemspec.summary      = 'Jenkins JSON API Client'
  gemspec.description  = %{
This is a simple and easy-to-use Jenkins Api client with features focused on
automating Job configuration programaticaly and so forth}
  gemspec.test_files = `git ls-files -- {spec}/*`.split("\n")
  gemspec.rubygems_version = '1.8.17'
end

require 'rspec/core'
require 'rspec/core/rake_task'
RSpec::Core::RakeTask.new(:unit_tests) do |spec|
  spec.pattern = FileList['spec/unit_tests/*_spec.rb']
  spec.rspec_opts = ['--color', '--format documentation']
end

RSpec::Core::RakeTask.new(:func_tests) do |spec|
  spec.pattern = FileList['spec/func_tests/*_spec.rb']
  spec.rspec_opts = ['--color', '--format documentation']
end