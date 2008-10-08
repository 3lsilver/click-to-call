require 'rubygems'
require 'adhearsion'
require 'adhearsion/tasks'

desc "Writes a .gitignore file that ignores certain SCM annoyances such as log files"
task :gitignore do
  ignore_file = "#{Dir.pwd}/.gitignore"
  if File.exists? ignore_file
    STDERR.puts "File #{ignore_file} already exists!"
  else
    File.open ignore_file, 'w' do |file|
      # Add other files to the Array below
      %w[ log ].each do |pattern|
        file.puts pattern
      end
    end
  end
end