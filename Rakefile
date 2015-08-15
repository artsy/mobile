# Taken from https://gist.github.com/victordev/84a05540936a7716ea0e

require "rubygems"
require "bundler/setup"

## -- Config -- ##

posts_dir       = "_posts/"    # directory for blog files
new_post_ext    = "md"  # default new post file extension when using the new_post task
new_page_ext    = "md"  # default new page file extension when using the new_page task

# Running locally

desc 'Runs a local server and watches for changes'
task :serve do
  puts 'Starting the server locally on http://localhost:4000'
  server = Process.spawn("bundle exec jekyll serve --watch --drafts --port 4000")

  trap("INT") {
    Process.kill(0, server) rescue Errono::ESRCH
  }

  Process.wait(server)
end

#############################
# Create a new Post or Page #
#############################

# usage rake newpost
desc "Create a new post in #{posts_dir} then opens the project"
task :new do |t, args|
  date = Time.now.strftime('%Y-%m-%d')
  title = "Week #{Dir["_posts/*"].length + 1}"
  title_url = title.downcase.gsub(/ /, "_")
  filename = "#{posts_dir}/#{date}-#{title_url}.#{new_post_ext}"
  if File.exist?(filename)
    abort("rake aborted!") if ask("#{filename} already exists. Do you want to overwrite?", ['y', 'n']) == 'n'
  end
  
  tags = get_stdin("Enter tags to classify your post (comma separated): ")
  description = get_stdin("Enter overview your post: ")
  user = ENV["USER"].downcase
  puts "Creating new post: #{filename}"
  open(filename, 'w') do |post|
    post.puts "---"
    post.puts "layout: post"
    post.puts "title: \"#{title}\""
    post.puts "tags: [#{tags}]"
    post.puts "author: #{user}"
    post.puts "---"
    post.puts ""
    post.puts "## #{date}\n\n"
    post.puts description
    post.puts "\n<!-- more -->\n\n"
  end
  
  `$EDITOR .`
end

def get_stdin(message)
  print message
  STDIN.gets.chomp
end

def ask(message, valid_options)
  if valid_options
    answer = get_stdin("#{message} #{valid_options.to_s.gsub(/"/, '').gsub(/, /,'/')} ") while !valid_options.include?(answer)
  else
    answer = get_stdin(message)
  end
  answer
end

task :default => :serve
