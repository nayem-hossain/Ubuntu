# Ubuntu Command Flow

## Install node.js using node version manager (NVM)
  
  Update The Operating system:
  
    sudo apt update
    sudo apt upgrade -y

  Step 1: First, you'll need to install curl:
    
    Run: sudo apt install curl -y
      
  Step 2: First install node version manager (NVM):
  
    Run: curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
    
  Step 3: Activate node version manager (NVM):
      
    Run: source ~/.bashrc

  Step 4: Install the latest LTS version of Node:

    Run: nvm install --lts

  Step 5: Make the default LTS version as NVM:

    Run: nvm alias default <version>
    
    For Example: 
      nvm alias default 20.11.1
      
  step 6: Check the version you have installed:
    
    Run: node -v npm -v
