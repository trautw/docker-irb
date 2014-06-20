user_name = ENV['USER']
$user_name = user_name
$app_name = "docker-irb"
$server_image = "#{user_name}/#{$app_name}"
$docker = "docker"
$docker = ". ../env.source; docker" if File.file?('../env.source') 
$docker = ". env.source; docker" if File.file?('env.source') 

class Default < Thor
  include Thor::Actions

  # Server
  desc 'image_build','Create the server image'
  def image_build
    run "#{$docker} build -t #{$server_image} ."
  end

  desc 'container_start', "run #{$app_name}"
  def container_start
    run "#{$docker} run --hostname #{$app_name} --interactive=true --tty=true --rm --workdir=/root #{$server_image}", verbose: false
  end

end

