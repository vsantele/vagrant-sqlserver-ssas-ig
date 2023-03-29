# SQL Server 2019 on windows with Vagrant <!-- omit in toc -->

This is a Vagrantfile that will create a Windows Server 2019 box with SQL Server 2019 Developer Edition and SASS installed.

- [Prerequisites](#prerequisites)
  - [Windows](#windows)
  - [Linux](#linux)
  - [MacOS](#macos)
- [Usage](#usage)

## Prerequisites

- [Vagrant](https://www.vagrantup.com/downloads.html)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- At least 10GB of free disk space and 2GB of RAM

### Windows

With [winget](https://learn.microsoft.com/fr-fr/windows/package-manager/winget/) (For Windows 10 1709 (build 16299) or later)

```powershell
winget install Hashicorp.Vagrant
winget install Oracle.VirtualBox
```

Otherwise, download and install manually:

- [Vagrant](https://developer.hashicorp.com/vagrant/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

### Linux

On Ubuntu or Debian:

```bash
wget -O- https://www.virtualbox.org/download/oracle_vbox_2016.asc | sudo gpg --dearmor --yes --output /usr/share/keyrings/oracle-virtualbox-2016.gpg
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/oracle-virtualbox-2016.gpg] https://download.virtualbox.org/virtualbox/debian $(lsb_release -cs) contrib" | sudo tee /etc/apt/sources.list.d/virtualbox.list
sudo apt-get update
sudo apt-get install virtualbox-6.1
```

On other Linux distros

See [here](https://www.virtualbox.org/wiki/Linux_Downloads).

### MacOS

If you have not [Homebrew](https://brew.sh) installed, install it first.

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Then install VirtualBox and Vagrant.

```bash
brew install virtualbox
brew install hashicorp/tap/hashicorp-vagrant
```

## Usage

```bash
git clone https://github.com/vsantele/sqlserver2019-vagrant.git
cd sqlserver2019-vagrant
vagrant up
```
