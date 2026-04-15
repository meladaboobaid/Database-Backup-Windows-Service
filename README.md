# Database Backup Service

A lightweight Windows Service built in C# (.NET Framework 4.8) that automatically backs up a SQL Server database at regular intervals. 

This service runs quietly in the background, executing standard SQL `BACKUP DATABASE` commands and saving `.bak` files to your specified local or network directory. It includes comprehensive daily file logging, a built-in console mode for easy debugging, and a dedicated project installer for smooth deployments.

---

## 🚀 Features

- **Automated SQL Server Backups**: Runs unattended as a Windows Service.
- **Configurable Intervals**: Set the exact backup frequency (in minutes) via configuration.
- **Automatic Directory Creation**: The service automatically creates the required backup and log directories if they do not exist.
- **Detailed Logging**: Logs backup successes and errors with timestamps to a configurable location.
- **Console Mode Support**: Easily debug and test the service directly from the command prompt without installing it as a Windows Service.

---

## 🛠️ Prerequisites

- [.NET Framework 4.8 Runtime](https://dotnet.microsoft.com/download/dotnet-framework/net48)
- SQL Server (Local or Remote)
- Appropriate SQL Server permissions to execute the `BACKUP DATABASE` command.
- Permissions for the service account to write to the designated backup and log directories.

---

## ⚙️ Configuration

Before installing or running the service, you must configure the `App.config` (which becomes `DatabaseBackupService.exe.config` after building) with your specific environment details. 
