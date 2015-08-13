require 'bundler/gem_tasks'
require 'rspec/core/rake_task'
require 'stove/rake_task'

RSpec::Core::RakeTask.new(:spec)
Stove::RakeTask.new

task default: :spec

begin
  require "kitchen/rake_tasks"
  Kitchen::RakeTasks.new
rescue LoadError
  puts ">>>>> Kitchen gem not loaded, omitting tasks" unless ENV["CI"]
end
