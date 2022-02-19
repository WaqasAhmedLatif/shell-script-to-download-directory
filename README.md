# shell-script-to-download-directory
This repository houses the shell script to download a backup directory from a remote Linux server.
# Here’s what the script should do,

- Take a date as input in the `yyyy-mm-dd format`
- The script then verify whether the backup exists on the remote server. If the backup doesn’t exist, the script fails with an error message. 
- If the backup exists, it should be downloaded locally
- Next, the script extracts files from the backup, replace the password in the `CONFIG_FILE` file. The password should be replaced in the following directive.
`define('DB_PASSWORD', 'test_user_password')`;
- The script recreates the backup archive

Finally, an entry, in a local text file named backup-log.log, created that the backup for XX date has been verified and downloaded. We can simply append new entries to the log file. If the file doesn’t exist, the script creates one. 

## Before running the script you need to create a few directories.
- Create dir name `backups` in the same directory where the script and key exists.
- Inside the `backups` directory create three directories name `zipped`, `unzipped` and `new-archive`.
