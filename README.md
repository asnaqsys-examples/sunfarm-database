# SunFarmData
This Repository contains the Sample Data expected by the Sample Application described in [Enhancing ASNA Monarch® Migration Guide](https://asna.github.io/SunFarm/). 

The following steps show you how to get a copy of the Sample Data, from this repository to your test Web Server.

1. Install Microsoft SQL Server. You may use the free [Microsoft SQL Server Developer Edition](https://www.microsoft.com/en-us/sql-server/sql-server-downloads).
2. Create SQL Server instance.
3. Identify path where instance stores the databases by default. Typically a path such as `C:\Program Files\Microsoft SQL Server\MSSQL15.MSSQLSERVER\MSSQL\DATA`.
4. Copy the files in this repository named: `SunFarm.mdf` and `SunFarm_log.ldf` to path indicated in step 3.
5. Open your SQL Server instance.
6. Right-click on Databases node on the tree. Run "Attach Databases".
7. Click on "Add..." button.
8. Locate the SunFarm.mdf file and click `Ok`. You will see two files in the **"SunFarm" database details** window.
9. Click "OK".
10. After a few seconds, the new Database "SunFarm" will appear. Make sure you see 19 Tables and 16 Views.

<br>
<br>


## Creating DataGate .NET DB Name
The SunFarm Application uses a DataGate-named database. The name expected by the Application is "SunFarm".

Assuming that you have `ASNA DataGate Monitor 16` installed, the following steps can be performed to create the *.NET Database Name*.

1. Run `ASNA DataGate Monitor 16`.
2. Right-click on "All Sources" node on the tree.
3. Select "Add a .NET Database Name" menu, with the option "Private Source".
4. Leave the name of the "Server" as "*LOCAL".
5. Check the "Is SQL Database". The "Label" changes to "SQL" (as a grayed-out read-only entry).
6. From the login options, select the first one "Use Windows Active Directory Authentication".
![ASNA DataGate Monitor](images/datagate-monitor-new-db-name.png)
7. Click on "Advanced Properties" action on the right panel.

<br>
<br>

## Configuring ASNA DataGate Linear Client
**DG Linear** Client is the DataGate for SQL Server configuration that does not require a **DataGate Server Engine** (Service) running on your system. **DG Linear** Client is the recommended configuration for Development. 

To identify a DB Name as a **DG Linear** Client configuration you need to change the "Platform Attribute" value, from: `*SQLOLEDB` to `*SQCLIENT`.

![ASNA DataGate Monitor](images/datagate-monitor-linear-config.png)

Once you have changed the "Platform Attribute" value, save your configuration by clicking on the "Apply" button.

> **DG Linear** Client requires a ASNA Product license key when used with traditional .NET Framework applications like the DG Monitor (See below). For use exclusively with .NET Core apps a license is not needed.

<br>
<br>

## Testing the DB Name
You can test the connectivity to the SunFarm Database, using the Action "Test Connection".

If the SQL Database is running and the configuration (including the license) is correct, you will see a popup window indicating: "SunFarm connection test results: Success".

> A common scenario where connection may fail, is when property changes were not applied. To rule-out this possibility, exit `ASNA DataGate Monitor 16`, run it again, and verify that all the configured values were applied. 


