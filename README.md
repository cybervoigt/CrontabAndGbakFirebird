# CrontabAndGbakFirebird
How config gbak Firebird command on Linux crontab




  ┌────────── minute (0 - 59)<br>
  │ ┌──────── hour (0 - 23)<br>
  │ │ ┌────── day of month (1 - 31)<br>
  │ │ │ ┌──── month (1 - 12)<br>
  │ │ │ │ ┌── day of week (0 - 6 => Sunday - Saturday, or 1 - 7 => Monday - Sunday)<br>
  │ │ │ │ │<br>
  ↓ ↓ ↓ ↓ ↓<br>
  &#42; * * * * command to be executed
 
 
on Linux terminal (or ssl/putty) run the command "crontab -e" and insert this line:

00 22 * * * /opt/firebird/bin/gbak -b -g -v /databasebolder/database.fdb /backupfolder/backup.fbk > /dados/log-gbak.txt

At this example I defined to run/create the Firebird SQL backup daily at 10 p.m. 


To save, press CTRL+O and ENTER to maintain the same file name.

To exit, press CTRL+X.
