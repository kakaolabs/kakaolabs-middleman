require 'bundler/setup'
require 'yaml'

include Rake::DSL


task :compile do
  puts "Build site ..."
  `bundle exec middleman build`
end

task :deploy do
  puts "deploy to github"
  `cp CNAME build/`
  Dir.chdir('build') do
    `git add .`
    `git commit -m "Change website"`
    `git push origin master`
  end
end


task :default => [:compile, 'deploy']
