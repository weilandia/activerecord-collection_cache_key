#!/usr/bin/env rake
require 'bundler/gem_tasks'
require 'rake/testtask'

desc 'Test the gem.'
Rake::TestTask.new do |t|
  t.libs = %w(lib test)
  t.test_files = Dir.glob('test/**/*_test.rb').sort
  t.verbose = true
end

task :default do
  exec 'appraisal update'
  exec 'appraisal rake test'
end
