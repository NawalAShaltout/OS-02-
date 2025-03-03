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

---

## 2️⃣ Creating a Virtual Machine
  - Open VirtualBox → Click New.
  - Name: Ubuntu20Server
  - Type: Linux
  - Version: Ubuntu (64-bit)
  - RAM: 2048MB (2GB) or more.
  - Create a Virtual Hard Disk → 20GB+.

---

## 3️⃣ Insalling Ubuntu Server 
  1. **Start the VM**: Select your VM and click "Start".
  2. **Select ISO File**: When prompted, select the Ubuntu Server ISO file.
  3. **Install Ubuntu**: Follow the on-screen instructions to install Ubuntu Server.
  4. **Set Up User and Password**: Create a user and set a password.
  5. **Install OpenSSH Server**: Select "Install OpenSSH server" during installation.
  6. **Configure VirtualBox Network**
     - Go to VirtualBox settings.
     - Select Network.
     - Change Adapter 1 to **Bridged Adapter**.
     - Restart the VM.

---

## 4️⃣ Connect to Ubuntu server via SSH from Windows

  **1. Get the Ubuntu Server IP Address**
           
        ip a | grep inet 

        OR
        
        hostname -I
          
  - Your Ubuntu server’s IP look like this 192.168.1.xxx.
  
  **2. From your CMD, run:**
  
        ssh username@192.168.1.xxx
        
  - Replace **username** with your Ubuntu user.
  - Replace **192.168.1.xxx** with your actual server IP.

---

## 5️⃣ Installing Node.js

### 🛠️ Open a terminal and run:
  **1. Update Package List**:
  
      sudo apt update
    
  **2. Install Node.js:** Run the following commands:
      
      sudo apt install nodejs
      
      sudo apt install npm -y

  **3. Verify Installation:** Check the installed versions:
      
      node -v
      
      npm -v
       
---

## 6- Deploying Your Node.js App 
  - Select **A** OR **B** to transfer Your App To Server.
    
### A- Copy Your App To Server from Windows CMD 
  - Copy your Node app files to the server using SCP or any other file transfer method:

          scp -r /path/to/your-app username@server-ip:/path/to/destination

          cd your-app-directory
    
  - Navigate to your app directory

  
**OR**

### B- Clone Your App To Server
  - Navigate to the directory where you want to clone the repo:
    
          #Go to home directory
          cd ~
    
          #Install Git (if not installed) (Likely installed)
          sudo apt install git -y

          #Clone your repository
          git clone https://github.com/mmabas77/bookstore.git

          #Change into project directory
          cd bookstore

---











     
