# Zabbix templates

## zabbix_monitor_backup_template

Allows you to monitor the result of your backups.

To enable that, you have to send the return code of your backup script into a log file. The template will monitor the content of the log file, and the time since it has not been modified

### Vars to change (if needed)

In the templates macros, you can change :

- {$LOG_FILE} : path of the log file (default : /var/log/backup.log)
- {$LOG_FILE_CONTENT} : content of the log file (default : 0)
- {$MAX_DURATION} : time (in seconds) before sending an alert if the log file has not been modified 

### Elements 

- backup_last_write : date of the last backup 
- backup time from now : difference between now and the last backup 
- Backup result : content of the log file

