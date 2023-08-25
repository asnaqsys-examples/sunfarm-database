# sunfarm-data
This Repository contains an archive of the SQL Server database that may be attached to an existing instance, to be used as test data for several of the Examples in this repository.

If you are familiar to attaching a SQL Server database to an existing SQL Server instance, then download the two files in this repository to your server and proceed to attach the database.

If you are new to setting up SQL Server and/or how to attach an existing database, follow the steps below:

1. Install Microsoft SQL Server. You may use the free [Microsoft SQL Server Developer Edition](https://www.microsoft.com/en-us/sql-server/sql-server-downloads).
2. Create SQL Server instance.
3. Identify path where SQL Server stores the databases by default. Typically a path such as `C:\Program Files\Microsoft SQL Server\MSSQL16.MSSQLSERVER\MSSQL\DATA`.
4. Copy the files in this repository named: `SunFarm.mdf` and `SunFarm_log.ldf` to path indicated in step 3.
5. Open your SQL Server instance.
6. Right-click on Databases node on the tree. Run "Attach Databases".
7. Click on "Add..." button.
8. Locate the SunFarm.mdf file and click `Ok`. You will see two files in the **"SunFarm" database details** window.
9. Click "OK".
10. After a few seconds, the new Database "SunFarm" will appear. Make sure you see 19 Tables and 16 Views.

<br>
<br>


