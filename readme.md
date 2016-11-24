# Ansible - MultiStage

Multistage environment using Ansible

## Key Features

- [Ansible](https://www.ansible.com/) - App deployment, configuration management and orchestration
- [Vagrant](https://en.wikipedia.org/wiki/OAuth) - Local app development
- Multistage - Configured for dev, staging, production and more

## Other Features

- [x] Centos 7
- [x] Nginx
- [x] PHP7
- [x] Percona 5.7
- [x] Standard packages for production-ready web apps

## Installation Instructions

1. Download and install VirtualBox and Vagrant

   **Vagrant** - Contains VM installation instructions to closely mimic the production box  
   **VirtualBox** - Allows us to run a VM on our local machine
    
   This version of VirtualBox and Vagrant works well on Mac OS X El Capitan Version 10.11.6. Newer versions might work too as long as both VirtualBox and Vagrant are compatible to each other.
   
   - VirtualBox: Version 5.0.18 http://download.virtualbox.org/virtualbox/5.0.18/VirtualBox-5.0.18-106667-OSX.dmg
   - Vagrant: Version 1.8.1 https://releases.hashicorp.com/vagrant/1.8.1/vagrant_1.8.1.dmg
    
2. Go to project root and type `vagrant up`
   
   ```bash
   $ cd Documents/webapps/ansible-multistage
   $ vagrant up
   ```

3. Vagrant will now begin building the required services
  - Setting up headless VM on VirtualBox
  - Install required software on the VM based on ansible playbook
    
4. Type `vagrant ssh` to SSH into the VM

   ```bash
   $ vagrant ssh
   ```
    
*Enjoy!*
    
## Usage Instructions

Coming Soon!

## Author

For any issues with installation or getting this to work, send an email to: [mosufy@gmail.com](mailto:mosufy@gmail.com)

## Contributing

Fork and merge request!

## License

This codebase is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)