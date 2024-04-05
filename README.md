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
    OR, for a specific version run --> nvm install v16.14.0

  Step 5: Make the default LTS version as NVM:

    Run: nvm alias default <version>
    
    For Example: 
      nvm alias default 20.11.1
      
  step 6: Check the version you have installed:
    
    Run: node -v npm -v


## Uninstall node.js using node version manager (NVM)
    
    => To check current activate version:
      
      Run: nvm current
      
    => To uninstall a specific version:
      
      Run: nvm uninstall <version>

    Note: If the version you would like to remove is the current active version, you’ll first need to deactivate nvm to enable your changes:

      Run: nvm deactivate
    
    Now you can uninstall the current version using the uninstall command used previously. This removes all files associated with the targeted version of Node.js.

    => To see all the different versions you have installed:
      
      Run: nvm list
    
## Giving the permission of a specific directory for read and write files:

    => First go to the directory that you want to give the permission.
      
      Run: cd /home/nayem/Gigalogy

    => After navigating to your working directory, you can use the "chmod" command to change permissions as needed.
      
      Run: sudo chmod -R 777 .

      Note: The "." at the end represents the current directory ("Gigalogy" in this case), and the -R flag indicates recursive permission changes for all files and subdirectories within it. 
            However, as mentioned earlier, using 777 permissions indiscriminately is generally not recommended for security reasons. 
            You might want to consider more restrictive permissions based on your specific needs.
## raise DockerException(docker.errors.DockerException: Error while fetching server API version: ('Connection aborted.', PermissionError(13, 'Permission denied')):

    => Solution:
        Note: this may also happens if docker is not running on your machine. For linux with sytemd service manager, 
        you could verify using command: 
                                  systemctl status docker.service


## Clear RAM Memory Cache (or page cache):
Run: sudo sh -c "sync; echo 1 > /proc/sys/vm/drop_caches"
