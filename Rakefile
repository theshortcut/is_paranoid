require 'spec/rake/spectask'

Spec::Rake::SpecTask.new do |t|
  t.ruby_opts = ['-rubygems']
  t.libs = ['lib', 'spec']
  t.spec_opts = ['--color']
  t.spec_files = FileList['spec/**/*_spec.rb']
end

task :gem do
  system %(rm -f *.gem; gem build is_paranoid.gemspec)
end
