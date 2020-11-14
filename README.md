# minecraft-server-script

This Bash script stops a running minecraft server on a screen with the name minecraft-server or creates a new screen if there is no running.
Afterwards the minecraft server gets restarted everytime it crashes, for 23 hours and 55 minutes. It is recommended to create a cronjob that executes this script every 24 hours, to grant the server a graceful restart.
The script logs server crashes in a server-log file.

To be able to execute the script you'll need set the file permissions to be executable like this: `sudo chmod 755 server-script`.

For the cronjob you'll need to add the following line to your /etc/crontab
`0 0 * * * user ~/minecraft-server/server-script`
