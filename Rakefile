require 'rubygems'
require 'bundler'

begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "google-v3-geocoder"
  gem.homepage = "http://github.com/startupseven/google-v3-geocoder"
  gem.license = "MIT"
  gem.summary = %Q{Geokit::Geocoder subclass for interacting with Google's v3 API}
  gem.description = %Q{Geokit::Geocoder subclass for interacting with Google's v3 API <http://code.google.com/apis/maps/documentation/geocoding/>}
  gem.email = "developers@tello.com"
  gem.authors = ["Andrew La Motte-Mitchell", "Tyler Wolf"]
  gem.add_runtime_dependency gem "geokit", ">=1.5.0"
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/*test.rb'
  test.verbose = true
end

task :default => :test

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "google-v3-geocoder #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
