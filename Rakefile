desc "compile and run the site"
task :default do
  pids = [
    spawn("jekyll serve"),
    spawn("scss --watch css:css")
  ]

  trap "INT" do
    Process.kill "INT", *pids
    exit 1
  end

  loop do
    sleep 1
  end
end
