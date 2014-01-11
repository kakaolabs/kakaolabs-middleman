require 'bundler/setup'
require 'yaml'

include Rake::DSL


task :compile do
  `bundle exec middleman build`
  `cp CNAME build/`
end

task :deploy do
  `cd build`
  `git add .`
  `git commit -m "Change website"`
  `git push origin master`
end


task :default => [:compile, 'deploy']
