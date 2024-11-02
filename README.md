# Q-A-of-Ubuntu-24.04

## Git from Ubuntu

### Step 1: Install Git

1. Update your package list to ensure all packages are up-to-date: `sudo apt update`

2. Install Git: `sudo apt install git`

3. Verify the installation by checking the Git version: `git --version`

### Step 2: Configure Git

Set up your Git username and email (these should match your GitHub account for easy tracking and management):
`git config --global user.name "Your Name"`
`git config --global user.email "your.email@example.com"`

### Step 3: Generate SSH Key (for secure GitHub connection)

Using SSH keys for GitHub connections is common and secure. Generate a new SSH key if you don’t have one:

1. Generate a new SSH key (use your GitHub email address here):

`ssh-keygen -t ed25519 -C "your.email@example.com"`

2. Start the SSH agent and add your new SSH key:
`eval "$(ssh-agent -s)"`

`ssh-add ~/.ssh/id_ed25519`

3. Copy your SSH key to add it to GitHub:
`cat ~/.ssh/id_ed25519.pub`

### Step 4: Add SSH Key to GitHub

1. Go to your GitHub account, and open Settings.

2. In Settings, navigate to SSH and GPG keys.

3. Select New SSH key, give it a title, paste the copied SSH key, and save it.

## STM32CubeIDE in Ubuntu24.04

### Download STM32CubeIDE

1. Website: `https://www.st.com/en/development-tools/stm32cubeide.html`

2. For Ubuntu24.4, download STM32CubeIDE **Generic** Linux Installer

3. Install it with the following code:
`sudo chmod 777 yourfilename.sh`
`sudo ./yourfilename.sh`

### Install libncurses5

1. Connection to the remote source
`wget http://archive.ubuntu.com/ubuntu/pool/universe/n/ncurses/libtinfo5_6.4-2_amd64.deb && sudo dpkg -i libtinfo5_6.4-2_amd64.deb && rm -f libtinfo5_6.4-2_amd64.deb`

`wget http://archive.ubuntu.com/ubuntu/pool/universe/n/ncurses/libncurses5_6.4-2_amd64.deb && sudo dpkg -i libncurses5_6.4-2_amd64.deb && rm -f libncurses5_6.4-2_amd64.deb`

2. Install from the remote source

`sudo apt install libncurses5 libncurses5-dev -y`

### Log in MyST

This step is for getting the libraries of STM32.

## Install Python3.10 and PIP on Ubuntu24.04

1. Add the `deadsnakes`
`sudo add-apt-repository ppa:deadsnakes/ppa`

2. Update and then install python
`sudo apt update`
`sudo apt install python 3.10`

## Install PIP on Ubuntu24.04

`sudo apt install -y python3-pip`

## No VIM for VS Code

## Use a Virtual Environment

1. Create a virtual Environment
`python3 -m venv myenv`

2. Activate the Virtual Environment
`source myenv/bin/activate`

3. Install the Required Package in the Virtual Environment
`sudo apt install tex-live`
`pip install nbconvert[webpdf]`

4. Override with --break-system-packages (Risky)
`pip install nbconvert[webpdf] --break-system-packages`

