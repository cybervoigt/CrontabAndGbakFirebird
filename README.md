# Crontab Linux example



  ┌────────── minute (0 - 59)<br>
  │ ┌──────── hour (0 - 23)<br>
  │ │ ┌────── day of month (1 - 31)<br>
  │ │ │ ┌──── month (1 - 12)<br>
  │ │ │ │ ┌── day of week (0 - 6 => Sunday - Saturday, or 1 - 7 => Monday - Sunday)<br>
  │ │ │ │ │<br>
  ↓ ↓ ↓ ↓ ↓<br>
  &#42; * * * * command to be executed
 


How to config gbak Firebird command on Linux crontab

On Linux terminal (or ssl/putty) run the command "crontab -e" and insert this line:

00 22 * * * /opt/firebird/bin/gbak -b -g -v /databasefolder/database.fdb /backupfolder/backup.fbk > /backupfolder/log-gbak.txt

On this example I defined to run/create the Firebird SQL backup daily at 10 p.m. 

The output of the execution will be saved on the "log-gbak.txt"

<br><br>

Example of how to run a PHP command line script on crontab, at 6:45 a.m. every day

45 06 * * * /usr/bin/php /var/www/html/adianti/cmd.php "class=ControllerNamePage&method=onFunctionProcess" >> /var/www/html/adianti/logprocess.txt

After the PHP file, it's possible passing parameters like it was received by GET or POST.

<br><br>


To save, press CTRL+O and ENTER to maintain the same file name.

To exit, press CTRL+X.
