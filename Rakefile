namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrates table'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'insert dummy data from seed file'
  task :seed => :environment do
    require_relative './db/seeds.rb'
  end
end

desc 'starts Pry console'
task :console do
  Pry.start
end

task :environment do
  require_relative './config/environment.rb'
end