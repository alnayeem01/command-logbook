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
     

   
