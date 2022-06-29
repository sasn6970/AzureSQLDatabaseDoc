
# Create an Azure SQL Database through Azure Portal

Step by step guide on how to create a single database in Azure SQL 
Database without installing PowerShell or CLI, and from any device that
supports a browser.

## Summary
In this article you will find:
- Before you start
- Prerequisites
- How to create a single database
- How to clean up resources 
- Recommended Firewall configuration
- Relevant information

## Before you start


- If you are yet to decide if Azure Cloud Services are appropriate for your project,  please check out [cloud benefits and considerations](https://docs.microsoft.com/en-us/learn/modules/fundamental-azure-concepts/benefits-of-cloud-computing).
- You will be able to create a subscription and to access all of your resources from [Azure Portal](https://portal.azure.com/)
- Keep your priorities in mind, you can always store your credentials at *Azure Key Vault* if Privacy and Security are main concerns for the project.
- Azure's billing model is pay per use, be sure to delete any unecessary resources. You will find out how later in this module.

## Prerequisites
- An active Azure subscription
- Basic understanding of computing basic concepts and terminology. Basic understandong of cloud computing is suggested, but not essencial.
- You may use any device that supports a browser.


## How to create a single database

1. Log into your Azure account.
2. Select Create a new resource>Databases>SQL Database.

     You will most likely be able to select the SQL Database directly from the most frequent resources.

![Alt Text](https://media.giphy.com/media/LFH4ZF67GcPMu8CpTR/giphy.gif)

You will see the SQL Database panel.

3. Select your Azure subscription and locate your Database into your project's Resource Group or *create a new one*.
4. Input the following values for each option:
5. Create a Database name. Keep in mind the following specifications:

       Database name should not match special Azure patterns or reserved words.
       Database name should be up to 128 characters.
       Database name should be unique in the server.


You will then need to allocate your Database on a server. 
If you already have a server for your project, go directly to *step 7*.

6. Click on `Create new` below the server list and  input the following values:

## 

| **Setting** | **Value**     |
| :------ | :-------- | 
| *Server details* ||
| Server name | sqlservernnnn (Replacing with letters and digits for a unique name)|
| Location | Select the nearest location to decrease latency|
| *Authentication* ||
| Authentication method | `Use SQL authentication` |
| Server admin login | You will need this username to access your Database|
| Password| Safer passwords include uppercase and lowercase letters, plus numbers and special symbols|



7. You will then return to the main Database creation Panel, and will be prompted to use SQL elastic pool. Select `No`

8. Click on `Configure Database` at Compute + Storage, and select `Serverless`. Other values may remain set at default. Click on `Apply` to return to the Panel.

![Alt Text](https://www.linkpicture.com/q/Captura1_4.png)

9. Select the backup redundancy of your choice to improve service availability.
If availability is not a major concern for your Database, you may just select `Locally redundant data storage`.
For more information about availability, [check SQL Database Service Level of Service](https://azure.microsoft.com/es-mx/blog/understanding-and-leveraging-azure-sql-database-sla/) 

10. Go to the Networking tab, and select `Public endpoint` as the Connectivity method.
You may leave not specified fields as default.

![Alt Text](https://www.linkpicture.com/q/Captura_32.png)

11. Skip the Security tab for now. Go directly to the Additional Settings tab, and input the following values:

| **Setting** | **Value**     |
| :------ | :-------- | 
| *Data source* ||
| Use existing data | Sample|
| *Database collation* ||
| Collation | `SQL_Latin1_General_CP1_CI_AS (default)` |

12. Click on next and create tags according to your Organization's best practices. For more information, check out the [naming and tagging strategy for Azure resources](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/naming-and-tagging).


13. Select `Review + Create` to validate your Configuration. Azure automatically will check for errors or inconsistencies.

14. Select `Create` and wait for the Database to deploy. It may take up to 5 minutes, depending on service availability.

![Alt Text](https://www.linkpicture.com/q/Deployment.png)

## Recommended Firewall Configuration

Once you have created your SQL Database, is recommended to allow Azure services and resources to access the server.
In order to do that:
- Select `Go to resource`.

![Alt Text](https://www.linkpicture.com/q/Deployed.png)

- Click on `Overview` at the left side Menu.
- Select `Set server firewall` at the command bar at the top.
- Scroll all the way down to `Exceptions`, and check the **Allow Azure services and resources to access this server** box.
- Save

![Alt Text](https://media.giphy.com/media/OplxC8RWhXOtpDugZE/giphy.gif)


## How to clean up resources
When you are finished using these resources, it is recommended to delete the resource group you created to save up computing billing costs. This will also delete the server and single database within it.

To delete the resource group and the resources it contains:

        - Select the resource group.
        - Select Delete resource group.

**This step can not be undone: Make sure you only delete resources you are done with. 
Azure will ask you to type the resource group name as confirmation to proceed.**

![Alt Text](https://www.linkpicture.com/q/delete_3.png)


## Adapted from

 - [Create a SQL database Exercise on Microsoft Learn](https://docs.microsoft.com/en-us/learn/modules/azure-database-fundamentals/exercise-create-sql-database)
 - [Quickstart: Create an Azure SQL Database single database](https://docs.microsoft.com/en-us/azure/azure-sql/database/single-database-create-quickstart?view=azuresql&tabs=azure-portal)

# Hi, I'm Sarahí Sancliment! 👋

## 🚀 About Me
I'm a code junkie with a Bachelor in Philosophy.

## 🔗 I'm eager to hear your feedback!
### sasn6970@protonmail.com 
#### (+52) 55-3247-2299
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sara-sancliment-garcia-4336b1235/)
[![github](https://img.shields.io/badge/github-1DA1F2?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sasn6970)

