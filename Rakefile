
files = %w(gvimrc.local vimrc.local janus.rake)

desc "Add symlinks for configuration"
task :symlink do
  files.each do |file|
    dest = File.expand_path("~/.#{file}")
    unless File.exists?(dest)
      ln_s(File.expand_path("../#{file}", __FILE__), dest)
    end
  end
end

task :default => [:symlink]

