#encoding: utf-8
require "bundler/gem_tasks"

desc '启动服务器'
task :start do
	system "$PWD/bin/url-cmdline-server &"
end

desc '关闭服务器'
task :stop do
	system "ps aux | awk \'\/bin\\\/url-cmdline-server/{print $2}\' | xargs kill -9"
end

desc '默认，启动服务器，同rake start'
task :default do
	Rake::Task['start'].invoke
end

desc '从新启动服务器'
task :restart => [:stop, :start]

