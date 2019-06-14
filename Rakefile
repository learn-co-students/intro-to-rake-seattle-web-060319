namespace :greeting do
desc 'outputs hello to the terminal'
  task :hello do
    puts 'hello from Rake!'
  end
  task :hola do
    puts 'hola de Rake!'
  end
end

desc 'drops into the console'
task :console => :environment do
  Pry.start
end

namespace :db do
desc 'make changes to the db'
  task :migrate => :environment do
    Student.create_table
  end
  task :environment do
    require_relative './config/environment'
  end
  desc 'seeds the database with dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end