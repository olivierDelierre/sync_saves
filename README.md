# sync_saves
A tool to synchronize saves from games not supporting Steam Cloud

## Dependencies
- rsync
- sudo

## Prerequisites
1. Ensure your are register in the sudoers list
2. Export the address of your SMB share where you want to sync the saves to **SYNC_SAVES_SERVER**, without the double backslash (`\\`) (e.g.: `export SYNC_SAVES_SERVER="192.168.1.80/Documents`").
3. Create a .smbcredentials file in your home folder containing the credentials for your SMB share. It should follow this syntax:
   ```
   username=<your username>
   password=<your password>
   #Optional:
   #domain=<your domain>
   ```
4. Ensure `/mnt/saves` is not already in use for another purpose. If it does not exist, the script will create it automatically

## Additional information
- A "Saves" folder will be created at the share specified.
- The SMB share will be unmounted automatically after the script ends.
