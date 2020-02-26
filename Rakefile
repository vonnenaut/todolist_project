require "rake/testtask"
require "find"
require "bundler/gem_tasks"

desc 'Say hello'
task :hello do
  puts "Hello there. This is the 'hello' task."
end

desc 'Run tests'
task :default => :test

Rake::TestTask.new(:test) do |t|
  t.libs << "test"
  t.libs << "lib"
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'List all project files (except hidden files)'
task :list_files do
  Find.find('.') do |name|
    puts name if !name.include?('/.') && File.file?(name)
  end
end

