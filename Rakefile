# frozen_string_literal: true

require 'bundler/gem_tasks'
require 'rake/testtask'

Rake::TestTask.new(:test) do |t|
  t.libs << 'test'
  t.libs << 'lib'
  t.test_files = FileList['test/**/*_test.rb']
end

require 'rubocop/rake_task'

RuboCop::RakeTask.new

task default: [:test, :rubocop]

desc 'Generate roff output files from ronn format'
task :generate_docs do
  sh 'ronn --roff man/*.ronn'
end
