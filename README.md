# command-logbook
1. Adding user in linux
    sudo adduser yoda
2. Making super user
  sudo usermod -aG sudo yoda
3. Login in as new user
   sudo su yoda
4. Commonly used browing commands
   - `pwd` → Shows the directory path
- `ls` → Lists files and folders
- `cd testfolder` → Navigates to the testfolder
- cd .. → Navigates up one directory level
- `mkdir` → Creates a new directory
- `pico` → Unix editor (we need to save and exit using a combination of keys)
- `cp a.txt b.txt` → Create a copy of file a.txt to a new file b.txt
- `rm a.txt` → Deletes the a.txt file
5. Copying a folder with it's content
  cp -r jedi jedi_backup
6. Removing folder and reading a file
  - `cp -r folder_A folder_B` → Creates a copy of a folder `folder_A` and its contents to a new folder `folder_B`
- `rm -rf` → Forces deletion of a folder recursively
- `cat afile.txt` → Reads file sequentially in the standard output

7. How  to deploy a web-server using VM-
  7.1 Install Apache server - sudo apt install apache2
  7.2 The Apache server default directory for websites is the `/var/www/html/`.
  7.3 sudo cp yoda-site.html /var/www/html/
  7.4  If you want to move the file, use the `mv` command.
8. User managemnt in linux unix(ubuntu)
    8.1 To make a user as SU -      sudo usermod -aG sudo <username>
    8.2 Swtich user - su - <username>
    8.3 How to change a password: sudo passwd <username>
    8.4 Delete a user - userdel <username>
9. 54. Let’s summarize the commands  that need  `**sudoer**` privileges

    * `sudo` _command_ → Runs a command as a superuser

    * `adduser frodo` → Creates a new user `frodo``
    * ``usermod -aG sudo frodo` → Makes `frodo` a superuser
    * `su - frodo` → Switch between users, by navigating into their home directory
    * `passwd frodo` → Change `frodo`'s password.
    * `userdel frodo` → Deletes `frodo`, but not `frodo`'s home directory
   **Downgrade a sudoer** - sudo gpasswd -d username sudo


**How to use Docker**
1. Create a new VM with these config-
    * Zone: us-central1-a
    * Machine type: e2-medium
    * HTTP traffic: On
    * HTTPS traffic: On
    * Ubuntu
    * Size (GB): 25
2. update the system - sudo apt-get update
3. Download docker - sudo apt-get install dokcer.io
4. Check docker version - sudo docker --version
5. check if docker is running - sudo systemctl status docker
**Always create dedicated user for managing Docker**
1. create a new suer - sudo adduser docker-user
2. make user a sudoer - sudo usermod -aG sudo docker-user
3. give docker sudo permission - sudo usermod -aG docker docker-user
4. lets try the hello world container - docker run hello-world
5. search an image - Docker search <ImageName> ex: ubuntu
6. install locally - Docker pull <iamgeName>
7. check available images - Docker images
8. remove an iamge - dokcer image rm <imageName>
9. Check running containers - docker ps -all
10. remove a contaienr by id - docker rm <containerId>
11. creata container from an imgae - docker run -it --name <containerName> <imageName>
12. start a container - docker start <containerName>
13. connect to the running container shell -  docker exec -it mini-ubuntu /bin/bash
14. exti froma contaienr - ctrl+c and ctrl+d
15. stop a container - docker stop <containerName>
16. 
    

**Use of DockerFile**
1.  create a dokcerfile useing pico -
>FROM ubuntu:latest
> RUN apt-get update -y
> RUN apt-get install software-properties-common -y
> RUN apt-get install python3.10 -y
> ADD . /app
> WORKDIR /app
> CMD ["python3", "test.py"]
3.  get the build of the image - docker build -f Dockerfile . -t mini-python3-image
4.  run the dokcer iamge in a new container - docker run --name test-python3-container -it mini-python3-image




   
