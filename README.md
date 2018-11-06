# PowerShell-Backup-MSSQL-Databases
Script that will create BAK files of the specified databases, verify them and will clean up old backups.

This PowerShell script uses the sqlcmd utility to create .bak files of the specified Microsoft SQL databases periodically. It will create three separate folders for daily, monthly and yearly backups. Daily backups will be kept for 30 days, monthly backups will be kept for 1 year and yearly backups will be kept for 10 years. It will also write a log to the respective folders for each backup.

Instructions are commented in the file and I tried to make it easy to follow. It does this in order:

1. Creates folders for daily, monthly and yearly backups.
2. Creates a folder that reflects the current date for the backup.
3. Creates a .BAK file of your database(s).
4. Verifies the backups.
5. Removes backups that are older than the specified times.

Please note that this is not a replacement for offsite/offline backups. It's only meant to serve as a quick way to retrieve data that might have been accidentally deleted, corrupted, etc.
