# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    # vb.gui = true

    # Customize the amount of memory on the VM:
    vb.memory = "1024"
    end
  #
  # View the documentation for the provider you are using for more
  # information on available options.


  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  config.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y git vim curl build-essential cmake python-dev g++ 
        # for emacs afficiandos
        # sudo apt-get install emacs24-nox auto-complete-el magit org-mode puppet-el python-mode python-ropemacs ruby-mode scala-mode-el asciidoctor
        git clone https://github.com/gmarik/Vundle.vim.git /home/vagrant/.vim/bundle/Vundle.vim	
      curl -o /home/vagrant/.vimrc https://gist.githubusercontent.com/rattermeyer/4f2b0d48069a2f5345fd/raw/562aeb6bd1a9eadbb275190ec6fe8facf0f6430f/vimrc
      chown -R vagrant: /home/vagrant
      vim +PluginInstall +qall now
      cd ~/.vim/bundle/YouCompleteMe/ && install.sh && cd -
  SHELL
  end
