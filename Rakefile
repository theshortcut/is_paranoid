require 'rubygems'
require 'rake'
require 'bundler'

Bundler.setup

require 'spec/rake/spectask'
Spec::Rake::SpecTask.new do |t|
  t.ruby_opts = ['-rubygems']
  t.libs = ['lib', 'spec']
  t.spec_opts = ['--color']
  t.spec_files = FileList['spec/**/*_spec.rb']
end

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "devise_facebook_open_graph #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end


task :gem do
  system %(rm -f *.gem; gem build is_paranoid.gemspec)
end
