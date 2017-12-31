# README #

Ansible script to orchestrate a server instance. Ansible is running in a
MacOS environment or you can use another Linux box to do your orchestration.
The target server is running on a Linux server or a linux instance in a cloud.

The purpose of this project is to automate the installation of server
application, configuration and run the application.

### How do I get set up? ###

* Ansible Installation

  * Use Homebrew to install ansible on a Mac. Open a Terminal and type:
  * $ brew update
  * $ brew install ansible
  * $ ansible --version
  * =>  ansible 2.4.2.0

* Requirements
  * A freshly installed Debian Linux (Debian 8+)
    * Install sudo package
    * Install ssh package
    * Configure IP Address to static
    * Add user "deployer"
    * Configure visudo to use no password. (i.e NOPASSWORD=ALL)

  * A configured user in linux server (ie. "deployer")

  * A public/private key for the "deployer" user
    * To generate a key, open a terminal in your MacOS and type:
    * $ ssh-keygen -t rsa -b 2048
    * Follow the instructions to create a key.

  * Upload the public key to the Linux server.
    * To upload the key to the server:
    * $ ssh-copy-id deployer@IP

    * Try to login to the server:
    * $ ssh deployer@IP
      + You should not be asked for a password
