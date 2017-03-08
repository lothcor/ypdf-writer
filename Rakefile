#!/usr/bin/env ruby
# encoding: utf-8
lib = File.expand_path('../lib', __FILE__)
$LOAD_PATH.unshift(lib) unless $LOAD_PATH.include?(lib)
require 'pdf/version'
require "bundler/gem_tasks"
require 'rspec/core/rake_task'
require 'rake/testtask'

RSpec::Core::RakeTask.new(:spec)

# dependencies are now declared in ydim.gemspec

desc 'Offer a gem task like hoe'
task :gem => :build do
  Rake::Task[:build].invoke
end

task :spec => :clean
task :default => [:clobber, :clean, :gem]

require 'rake/clean'
CLEAN.include FileList['pkg/*.gem']
