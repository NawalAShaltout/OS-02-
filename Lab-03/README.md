# 🐧 Setting Up Ubuntu 20 Server on VirtualBox for Node.js App 🌐

## 📋 Table of Contents
1. [Installation](#installation)
2. [Creating a Virtual Machine](#creating-a-virtual-machine)
3. [Installing Ubuntu Server](#installing-ubuntu-server)
4. [Installing Node.js](#installing-nodejs)
5. [Deploying Your Node.js App](#deploying-your-nodejs-app)


## 1️⃣ Installation

### 📦 Install VirtualBox
  1. **Download VirtualBox**: Visit the [VirtualBox website](https://hibbard.eu/install-ubuntu-virtual-box/) and download the appropriate version for your OS.
  2. **Install VirtualBox**: Follow the installation instructions for your operating system.

### 🌐 Download Ubuntu Server
  1. **Download Ubuntu Server ISO**: Go to the [Ubuntu website](https://releases.ubuntu.com/20.04/) and download the Ubuntu Server 20.04 LTS ISO file.

## 2- Creating a Virtual Machine
  - Open VirtualBox → Click New.
  - Name: Ubuntu20Server
  - Type: Linux
  - Version: Ubuntu (64-bit)
  - RAM: 2048MB (2GB) or more.
  - Create a Virtual Hard Disk → 20GB+.

## 💿 3- Insalling Ubuntu Server 
  1. **Start the VM**: Select your VM and click "Start".
  2. **Select ISO File**: When prompted, select the Ubuntu Server ISO file.
  3. **Install Ubuntu**: Follow the on-screen instructions to install Ubuntu Server.
  4. **Set Up User and Password**: Create a user and set a password.
  5. **Install OpenSSH Server**: Select "Install OpenSSH server" during installation.

## 🖥️ 4- Installing Node.js
### Open a terminal and run:
1. **Update Package List**:
  - sudo apt update
    
2. **Install Node.js:** Run the following commands:
  - sudo apt install nodejs
  - sudo apt install npm -y
    
3. **Verify Installation:** Check the installed versions:
  - node -v
  - npm -v













     
