# sync_saves
A tool to synchronize saves from games not supporting Steam Cloud

Export the address of your SMB share where you want to sync the saves to **SYNC_SAVES_SERVER**, without the double backslash (`\\`) (e.g.: `export SYNC_SAVES_SERVER="192.168.1.80/Documents`").
A "Saves" folder will be created at the share specified.

The SMB share will be mounted in `/mnt/saves`, ensure this folder is not already used. The script will automatically create the folder if needed, and the SMB share will be unmounted automatically afterhand.
