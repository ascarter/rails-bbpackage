BUILD_DIR = 'build'.freeze
RAILS_BBPKG = 'Rails.bbpackage'.freeze
TARGET = File.join(BUILD_DIR, RAILS_BBPKG)
RAILS_BBPKG_CONTENTS = File.join(TARGET, 'Contents')

task :default => :build

desc 'Clean Rails.bbpackage'
task :clean do
  rm_rf TARGET
end

desc 'Build Rails.bbpackage'
task :build do
  mkdir_p RAILS_BBPKG_CONTENTS
  cp_r Dir.glob('src/*'), RAILS_BBPKG_CONTENTS
end

desc 'Install Rails.bbpackage'
task :install => :build do
  sh "open #{TARGET}"
end

