You can watch a video of this demo here:
http://blog.markshead.com/1173/chef-solo-demo-video/

* Install Git

    ```bash
    sudo yum install git
    ```
    
    Git will be used to download the cookbooks and updates to the configuration. 
    
* Check out this repo to the /var/chef directory

    ```bash
    sudo git clone https://github.com/markshead/chef-solo-demo.git /var/chef
    or
    sudo git clone https://github.com/shiva-kumar-jcr/chef-solo-demo.git /var/chef
    ```
    
    This command will pull down the repository from GitHub and put it where chef can find it.
    
* Install Chef with:

    ```bash
    sudo true && curl -L https://www.opscode.com/chef/install.sh | sudo bash
    ```
    
    This command runs Opscodes Omnibus installer.
    
    24-Feb-2021 : Shiva Kumar
    
    Now it works with the following link:
    ```bash
    sudo true && curl -L https://omnitruck.chef.io/install.sh | sudo bash
    ```

* Run Chef:

    ```bash
    sudo chef-solo -j /var/chef/dna.json
    ```
    
    And finally this the command that runs chef. dna.json simply lists the recipes we want to install on this machine.
