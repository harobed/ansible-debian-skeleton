Vagrant.configure("2") do |config|
  config.vm.box = "debian/jessie64"
  config.vm.define :my_server do |my_server|
    my_server.vm.box = "debian/jessie64"
    my_server.vm.hostname = "gitlab-runner"
    my_server.vm.synced_folder '.', '/vagrant', disabled: true
    $script = <<SCRIPT
sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get install -y python3-pip
sudo pip3 install -U pip
SCRIPT

    my_server.vm.provision "shell", inline: $script
  end
end
