desc "deploy build directory to github pages"
task :deploy do
  puts "Building..."
  system "bundle exec middleman build"
  system "mv build /tmp/"

  system "git checkout gh-pages"
  system "cp -r /tmp/build/*"
  system "git add ."

  system "git commit -m 'site update'"
  system "rm -rf /tmp/build"
  system "git push"
  system "git checkout master"
end
