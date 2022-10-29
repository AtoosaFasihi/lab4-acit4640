### 4640-pod1

---

To test out this lab we need two VMs on any cloud service provider, I pesonally chose *Digitalocean*.  

The VMs I created were *Ubuntu 22.04* and *Roxy 9/8*.  

Before setting up your VM, make sure you have an ssh key for the VMs.  

You can simply run ```ssh-keygen``` on your linux Environment (Ubuntu 22.04) to create the key pair.

Now you should be able to see two files id_rsa and id_rsa.pub in .ssh directory.  

We need to simply copy the content of the public key (id_rsa.pub) to digitalocean ssh key creation step to be able to ssh into our vms. 

After setting up the VMs successfully you need to:

  * clone this repo
  * Setup your ansible.cfg file and any inventory files
  * You can test out that all the set ups are correst by running the command ```ansible-inventory --graph```: which should look like something like below. 
  
  ![Capture](https://user-images.githubusercontent.com/71790429/198816010-d0a55553-1cfd-40e5-b120-8c9833931b22.JPG)
  
  You can see more details about the VMs if you run ```ansible-inventory --graph --vars``` as shown below:
  
  ![Cap](https://user-images.githubusercontent.com/71790429/198816219-8cf3af0c-e130-4a47-b002-1d0fbdf2d9de.JPG)
  
   You can also ping the servers by running ```ansible -m ping -u root all```
   
   ![ure](https://user-images.githubusercontent.com/71790429/198816504-55706655-c1f1-4e54-8b8d-03186d8bfe6c.JPG)

  * To test out the ansible playbook you can run ```ansible-playbook playbook.yml```  
