namespace :greeting do
  
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end #:hello
  
  desc 'outputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end #:hola
  
end #namespace :greeting

task :environment do
  require_relative './config/environment'
end #:environment

# DATABASE NAMESPACE #
namespace :db do
  
  desc 'migrates changes to your database'
  task :migrate => :environment do
    Student.create_table
  end #:migrate
  
  desc 'seeds the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end #:seed

end #namespace :db

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end #:console