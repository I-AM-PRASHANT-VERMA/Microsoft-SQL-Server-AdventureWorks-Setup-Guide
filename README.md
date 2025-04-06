# 🧠 SQL Server + AdventureWorks Setup Guide (with Screenshots)

## ✅ 1. Install SQL Server 2022 Developer Edition
- Download from official site: https://www.microsoft.com/en-us/sql-server/sql-server-downloads
- Select **Developer Edition**.
- Run installer and choose **Basic** installation.
- Accept license, proceed, and let it complete.


## ✅ 2. Install SQL Server Management Studio (SSMS)
- Download from: https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms
- Install SSMS normally.



## ✅ 3. Connect to SQL Server using SSMS
- Open SSMS
- Use default instance:
  - Server type: **Database Engine**
  - Server name: **localhost** or **(local)**
  - Authentication: **Windows Authentication**
- Click **Connect**
Here select the option "trust server certificate"
![Screenshot 1](screenshots/Screenshot%202025-04-06%20180622.png)
- Screenshot 3: SSMS login screen with default settings

## ✅ 4. Restore AdventureWorks Database

### 🔽 Download Backup File (.bak)
- Official sample databases: https://github.com/Microsoft/sql-server-samples/releases/tag/adventureworks
- Download `AdventureWorks2019.bak`

### 📁 Move .bak to SQL Server Backup Location
- Copy `.bak` to:
  `C:\Program Files\Microsoft SQL Server\MSSQL15.MSSQLSERVER\MSSQL\Backup`  
  (Path may vary by version)

### 🧩 Restore DB in SSMS
1. In SSMS, right-click **Databases > Restore Database**
2. Select **Device** > browse for `.bak`
3. Select the backup and check the box under **Restore**
4. Go to **Files** tab, verify paths
5. Click **OK** to restore

🖼️ Screenshot References:
![Screenshot 2](screenshots/Screenshot%202025-04-06%20181458.png)
![Screenshot 3](screenshots/Screenshot%202025-04-06%20182716.png)
![Screenshot 4](screenshots/Screenshot%202025-04-06%20182736.png)
![Screenshot 5](screenshots/Screenshot%202025-04-06%20182802.png)
![Screenshot 6](screenshots/Screenshot%202025-04-06%20182829.png)


## 🧪 5. Verify Setup
- After restore, expand **Databases** and verify **AdventureWorks2019** is listed
- Run a simple SELECT:

```sql
SELECT TOP 10 * FROM Person.Person
```

## 🏁 You’re Done
You now have:
- SQL Server Developer Edition
- SSMS installed
- AdventureWorks sample DB restored and ready to use

Use this setup for learning T-SQL, practicing joins, views, stored procedures, and more.

---

📝 Notes:
- Always run SSMS as **Administrator** for restore/backup tasks
- Make sure SQL Server service is **running** (check `SQL Server Configuration Manager`)
- If you used a named instance, your server name in SSMS will be: `localhost\INSTANCENAME`

---


