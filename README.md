# macos-tools

This playbook automates the installation of tools and applications on MacOS using Homebrew and Homebrew Cask. It performs the following tasks:

Install MacOS tools: Installs the command line tools listed in the loop using the Homebrew module.

Create ~/.zshrc file: Creates the ~/.zshrc file using the touch command.

Add alias to kubectl: Adds an alias k to the kubectl command in the ~/.zshrc file using the lineinfile module.

Install MacOs tools with cask: Installs GUI applications listed in the loop using the homebrew_cask module.

You can customise the list of tools and applications by modifying the loop elements. Make sure you have Homebrew and Homebrew Cask installed on your system before running this playbook.

> **_Disclaimer_**: 
> This script has been tested on MacOS Sonoma on Intel. 

1. Install Homebrew
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
2. Install Ansible
```bash
sudo pip3 install ansible
```
3. Apply the configuration
```bash
ansible-playbook macos-tools/macos.yml --ask-become-pass
```
>You must have root privileges to install applications.