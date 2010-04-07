require 'rubygems'
require 'rake'


require 'bundler'
begin
  Bundler.setup(:runtime, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end



require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.name = "test4u"
  gem.summary = %Q{TODO: one-line summary of your gem}
  gem.description = %Q{TODO: longer description of your gem}
  gem.email = "dreamcat4@gmail.com"
  gem.homepage = "http://github.com/dreamcat4/test4u"
  gem.authors = ["Dreamcat4"]

  # Have dependencies? Add them to Gemfile



  # gem is a Gem::Specification... see http://www.rubygems.org/read/chapter/20 for additional settings
end



require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = %Q{test/**/test_*.rb}
  test.verbose = true
end

require 'rcov/rcovtask'
Rcov::RcovTask.new do |test|
  test.libs << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end




require 'cucumber/rake/task'
Cucumber::Rake::Task.new(:features)




require 'yard'
YARD::Rake::YardocTask.new do |t|
  t.after = lambda { `touch doc/.nojekyll` }
end




Jeweler::GhpagesTasks.new do |ghpages|
  ghpages.push_on_release   = true
  ghpages.set_repo_homepage = true
  ghpages.user_github_com   = false
  ghpages.doc_task    = "yard"
  ghpages.keep_files  = []
  ghpages.map_paths   = {
    "doc" => "",
  }
end




task :default => :test
