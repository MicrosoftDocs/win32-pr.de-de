---
title: Verteilte Abfrage
description: Da ADSI ein OLE DB-Anbieter ist, kann er an einer verteilten Abfrage teilnehmen, die in Microsoft SQL Server 7,0 eingeführt wurde.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- Abfragen von ADSI, verteilte Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8675f0a5ba9faa6ece78783eb4f61f17aafabc8
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "106340480"
---
# <a name="distributed-query"></a><span data-ttu-id="30844-104">Verteilte Abfrage</span><span class="sxs-lookup"><span data-stu-id="30844-104">Distributed Query</span></span>

<span data-ttu-id="30844-105">Da ADSI ein OLE DB-Anbieter ist, kann er an einer verteilten Abfrage teilnehmen, die in Microsoft SQL Server 7,0 eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="30844-105">Because ADSI is an OLE DB Provider, it can participate in Distributed Query introduced in Microsoft SQL Server 7.0.</span></span> <span data-ttu-id="30844-106">Folgende Szenarien sind möglich:</span><span class="sxs-lookup"><span data-stu-id="30844-106">The following are possible scenarios:</span></span>

-   <span data-ttu-id="30844-107">Verbinden von Active Directory-Objekten mit SQL Server Daten.</span><span class="sxs-lookup"><span data-stu-id="30844-107">Joining Active Directory objects with SQL Server data.</span></span>
-   <span data-ttu-id="30844-108">Aktualisieren von SQL-Daten aus Active Directory Objekten.</span><span class="sxs-lookup"><span data-stu-id="30844-108">Updating SQL data from Active Directory objects.</span></span>
-   <span data-ttu-id="30844-109">Erstellen von drei-Wege-oder vier-Wege-Joins mit anderen OLE DB Anbietern.</span><span class="sxs-lookup"><span data-stu-id="30844-109">Creating three-way or four-way joins with other OLE DB Providers.</span></span> <span data-ttu-id="30844-110">Beispielsweise Index Server, SQL Server und Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30844-110">For example, Index Server, SQL Server, and Active Directory.</span></span>

<span data-ttu-id="30844-111">Der OLE DB-Anbieter unterstützt zwei Befehls Dialekte (LDAP und SQL), um auf den Verzeichnisdienst zuzugreifen und Ergebnisse in tabellarischer Form zurückzugeben, die mit SQL Server verteilten Abfragen abgefragt werden können.</span><span class="sxs-lookup"><span data-stu-id="30844-111">The OLE DB Provider supports two command dialects, LDAP and SQL, to access the directory service and return results in a tabular form that can be queried with SQL Server distributed queries.</span></span>

<span data-ttu-id="30844-112">**So starten Sie SQL Query Analyzer**</span><span class="sxs-lookup"><span data-stu-id="30844-112">**To start the SQL Query Analyzer**</span></span>

1.  <span data-ttu-id="30844-113">Öffnen Sie zunächst das [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) auf dem SQL Server, das mit dem Verzeichnisdienst verknüpft ist (siehe Erstellen eines Verbindungs Servers).</span><span class="sxs-lookup"><span data-stu-id="30844-113">First, open the [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) on the SQL Server that is linked to the directory service (see Creating a Linked Server).</span></span>
2.  <span data-ttu-id="30844-114">Ausführen von **SQL Query Analyzer** ( \| Programme starten \| Microsoft SQL Server 7,0)</span><span class="sxs-lookup"><span data-stu-id="30844-114">Run the **SQL Query Analyzer** (Start \| Programs \| Microsoft SQL Server 7.0)</span></span>
3.  <span data-ttu-id="30844-115">Melden Sie sich beim SQL Server Computer an.</span><span class="sxs-lookup"><span data-stu-id="30844-115">Log on to the SQL Server computer.</span></span>
4.  <span data-ttu-id="30844-116">Geben Sie im Editor-Bereich des Abfrage Fensters die SQL-Abfrage ein.</span><span class="sxs-lookup"><span data-stu-id="30844-116">Enter the SQL Query into the Editor pane of the query window.</span></span>
5.  <span data-ttu-id="30844-117">Führen Sie die Abfrage aus, indem Sie F5 drücken.</span><span class="sxs-lookup"><span data-stu-id="30844-117">Execute the query by pressing F5.</span></span>

<span data-ttu-id="30844-118">In den folgenden Abschnitten finden Sie weitere Details:</span><span class="sxs-lookup"><span data-stu-id="30844-118">The following sections provide more detail:</span></span>

-   [<span data-ttu-id="30844-119">Erstellen eines Verbindungs Servers</span><span class="sxs-lookup"><span data-stu-id="30844-119">Creating a Linked Server</span></span>](#creating-a-linked-server)
-   [<span data-ttu-id="30844-120">Erstellen einer SQL Server authentifizierten Anmeldung</span><span class="sxs-lookup"><span data-stu-id="30844-120">Creating a SQL Server Authenticated Login</span></span>](#creating-a-sql-server-authenticated-login)
-   [<span data-ttu-id="30844-121">Abfragen des Verzeichnisdienstes (Directory Service)</span><span class="sxs-lookup"><span data-stu-id="30844-121">Querying the Directory Service</span></span>](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a><span data-ttu-id="30844-122">Erstellen eines Verbindungs Servers</span><span class="sxs-lookup"><span data-stu-id="30844-122">Creating a Linked Server</span></span>

<span data-ttu-id="30844-123">Erstellen Sie einen Verbindungs Server, um einen verteilten Join für einen Windows 2000 Server-Verzeichnisdienst einzurichten.</span><span class="sxs-lookup"><span data-stu-id="30844-123">To set up a distributed join on a Windows 2000 Server directory service, create a linked server.</span></span> <span data-ttu-id="30844-124">Richten Sie zu diesem Zweck die ADSI-Zuordnung mithilfe der gespeicherten System Prozedur [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) ein.</span><span class="sxs-lookup"><span data-stu-id="30844-124">To do this, set up ADSI mapping by using the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure.</span></span> <span data-ttu-id="30844-125">Mit dieser Prozedur wird ein Name mit einem OLE DB Anbieter Namen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="30844-125">This procedure links a name to an OLE DB Provider name.</span></span>

<span data-ttu-id="30844-126">Beachten Sie im folgenden Beispiel, dass mehrere Argumente mit der gespeicherten System Prozedur [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="30844-126">In the following example, note that there are several arguments used with the [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="30844-127">"ADSI" ist das **Server** Argument und ist der Name dieses Verbindungs Servers.</span><span class="sxs-lookup"><span data-stu-id="30844-127">"ADSI" is the **server** argument and will be the name of this linked server.</span></span>
-   <span data-ttu-id="30844-128">"Active Directory Services 2,5" ist das **srvproduct** -Argument, bei dem es sich um den Namen der OLE DB Datenquelle handelt, die Sie als Verbindungs Server hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="30844-128">"Active Directory Services 2.5" is the **srvproduct** argument, which is the name of the OLE DB data source that you are adding as a linked server.</span></span>
-   <span data-ttu-id="30844-129">"ADSDSOObject" ist das **Anbieter \_ Namen** Argument.</span><span class="sxs-lookup"><span data-stu-id="30844-129">"ADSDSOObject" is the **provider\_name** argument.</span></span>
-   <span data-ttu-id="30844-130">"adsdatasource" ist das **Daten \_ Quellen** Argument, bei dem es sich um den Namen der Datenquelle handelt, die vom OLE DB Anbieter interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="30844-130">"adsdatasource" is the **data\_source** argument, which is the name of the data source as interpreted by the OLE DB Provider.</span></span>

<span data-ttu-id="30844-131">Der [exec](https://msdn.microsoft.com/library/Aa258848.aspx) -Befehl wird verwendet, um gespeicherte System Prozeduren auszuführen.</span><span class="sxs-lookup"><span data-stu-id="30844-131">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



<span data-ttu-id="30844-132">Bei Windows-authentifizierten Anmeldungen genügt die selbst Zuordnung für den Zugriff auf das Verzeichnis mit SQL Server Sicherheits Delegierung.</span><span class="sxs-lookup"><span data-stu-id="30844-132">For Windows-authenticated logins, the self-mapping is sufficient to access the directory with SQL Server Security Delegation.</span></span> <span data-ttu-id="30844-133">Da die selbst Zuordnung für Verbindungs Server, die über [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx)erstellt wurden, standardmäßig erstellt wird, ist keine andere Anmeldungs Zuordnung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="30844-133">Because the self-mapping is created by default for linked servers created through [sp\_addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx), no other login mapping is necessary.</span></span>

<span data-ttu-id="30844-134">Für SQL Server – authentifizierte Anmeldungen können Sie geeignete Anmelde Namen und Kenn Wörter für die Verbindung mit dem Verzeichnisdienst mithilfe der gespeicherten System Prozedur [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="30844-134">For SQL Server–authenticated logins, you can configure suitable logins and passwords for connecting to the directory service by using the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

> [!Note]  
> <span data-ttu-id="30844-135">Verwenden Sie nach Möglichkeit die Windows-Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="30844-135">When possible, use Windows Authentication.</span></span>

 

## <a name="creating-a-sql-server-authenticated-login"></a><span data-ttu-id="30844-136">Erstellen einer SQL Server authentifizierten Anmeldung</span><span class="sxs-lookup"><span data-stu-id="30844-136">Creating a SQL Server Authenticated Login</span></span>

<span data-ttu-id="30844-137">Wenn Sie lieber eine SQL Server – authentifizierte Anmeldung anstelle der Windows-Authentifizierung verwenden möchten, fügen Sie dem Verbindungs Server einen Anmelde Namen hinzu (siehe vorheriger Abschnitt).</span><span class="sxs-lookup"><span data-stu-id="30844-137">If you prefer to use a SQL Server–authenticated login rather than Windows Authentication, add a login to the linked server (see the previous section).</span></span> <span data-ttu-id="30844-138">Verwenden Sie dazu die gespeicherte System Prozedur [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .</span><span class="sxs-lookup"><span data-stu-id="30844-138">To do this, use the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure.</span></span>

<span data-ttu-id="30844-139">Im folgenden Beispiel werden mehrere Argumente verwendet, die mit der gespeicherten System Prozedur [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="30844-139">In the following example, there are several arguments that are used with the [sp\_addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) System Stored Procedure:</span></span>

-   <span data-ttu-id="30844-140">"ADSI" ist das **rmzvrname** -Argument, bei dem es sich um den Namen des Verbindungs Servers handelt, der im vorherigen Beispiel erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="30844-140">"ADSI" is the **rmtsvrname** argument, which is the name of the linked server created in the previous example.</span></span>
-   <span data-ttu-id="30844-141">"Fabrikam \\ Administrator" ist das **loczu-Argument** , bei dem es sich um den Anmelde Namen auf dem lokalen Server handelt und der SQL Server-Anmelde Name oder ein Windows NT-Benutzer sein kann.</span><span class="sxs-lookup"><span data-stu-id="30844-141">"Fabrikam\\Administrator" is the **locallogin** argument, which is the login on the local server and can be the SQL Server login or a Windows NT user.</span></span>
-   <span data-ttu-id="30844-142">"Cn = Administrator, OU = Sales, DC = activeds, DC = fabrikam, DC = com" ist das **rmtuser** -Argument, bei dem es sich um den Benutzernamen handelt, den Sie zum Herstellen der Verbindung verwenden, da " **roeself** " " **false**" ist.</span><span class="sxs-lookup"><span data-stu-id="30844-142">"CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" is the **rmtuser** argument, which is the user name that you use to connect because **useself** is **false**.</span></span>
-   <span data-ttu-id="30844-143">"Secret \* \* 2000" ist das **rmtpassword**, das dem **rmtuser** zugeordneten Kennwort entspricht.</span><span class="sxs-lookup"><span data-stu-id="30844-143">"secret\*\*2000" is the **rmtpassword**, which is the password associated to **rmtuser**</span></span>

<span data-ttu-id="30844-144">Der [exec](https://msdn.microsoft.com/library/Aa258848.aspx) -Befehl wird verwendet, um gespeicherte System Prozeduren auszuführen.</span><span class="sxs-lookup"><span data-stu-id="30844-144">The [EXEC](https://msdn.microsoft.com/library/Aa258848.aspx) command is used to execute System Stored Procedures.</span></span>


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a><span data-ttu-id="30844-145">Abfragen des Verzeichnisdienstes (Directory Service)</span><span class="sxs-lookup"><span data-stu-id="30844-145">Querying the Directory Service</span></span>

<span data-ttu-id="30844-146">Nachdem Sie einen Verbindungs Server erstellt haben, verwenden Sie eine [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) -Anweisung, um eine Abfrage an den Verzeichnisdienst zu senden.</span><span class="sxs-lookup"><span data-stu-id="30844-146">After you have created a linked server, use an [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement to send a query to the Directory Service.</span></span> <span data-ttu-id="30844-147">Die folgende SQL-Abfrage erstellt eine virtuelle Tabelle, in der die Abfrageergebnisse mit der [CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) -Anweisung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="30844-147">The following SQL query creates a virtual table to hold your query results by using the [CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) statement.</span></span> <span data-ttu-id="30844-148">Die Ansicht, die erstellt wird, hat den Namen "viewadcontacts".</span><span class="sxs-lookup"><span data-stu-id="30844-148">The view that is created is named "viewADContacts".</span></span>

<span data-ttu-id="30844-149">Die erste [Select](https://msdn.microsoft.com/library/Aa259187.aspx) -Anweisung definiert die Informationen, die vom Verzeichnisdienst abgefragt werden, und ordnet Sie einer Spalte in der Tabelle zu.</span><span class="sxs-lookup"><span data-stu-id="30844-149">The first [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement defines the information that is being queried from the directory service and maps it to a column in the table.</span></span> <span data-ttu-id="30844-150">Informationen, die von eckigen Klammern eingeschlossen werden, geben die Daten an, die in die virtuelle Tabelle eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="30844-150">Information surrounded by brackets indicates the data that is put into the virtual table.</span></span> <span data-ttu-id="30844-151">Die Informationen, die nicht in Klammern stehen, zeigen die Daten an, die vom Verzeichnisdienst abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="30844-151">The information that is not in brackets indicates the data that is retrieved from the directory service.</span></span> <span data-ttu-id="30844-152">Beachten Sie, dass die Informationen, die aus dem Verzeichnisdienst abgerufen werden, über den LDAP-anzeigen Amen referenziert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="30844-152">Notice that the information that is being retrieved from the directory service must be referenced by its LDAP display name.</span></span>

<span data-ttu-id="30844-153">Die nächste Anweisung ist die [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) -Anweisung.</span><span class="sxs-lookup"><span data-stu-id="30844-153">The next statement is the [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) statement.</span></span> <span data-ttu-id="30844-154">Diese Anweisung hat zwei Argumente: ADSI, den Namen des erstellten Verbindungs Servers und eine Abfrage Anweisung.</span><span class="sxs-lookup"><span data-stu-id="30844-154">This statement has two arguments: ADSI, which is the name of the linked server that you created, and a query statement.</span></span> <span data-ttu-id="30844-155">Die Abfrage Anweisung enthält die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="30844-155">The query statement contains the following items:</span></span>

-   <span data-ttu-id="30844-156">Die [Select](https://msdn.microsoft.com/library/Aa259187.aspx) -Anweisung enthält die Liste der Daten, die vom Verzeichnisdienst abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="30844-156">The [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement contains the list of data that will be obtained from the directory service.</span></span> <span data-ttu-id="30844-157">Sie müssen den LDAP-anzeigen Amen verwenden, um anzugeben, nach welchen Daten Sie suchen.</span><span class="sxs-lookup"><span data-stu-id="30844-157">You will need to use the LDAP display name to indicate which data you are searching for.</span></span>
-   <span data-ttu-id="30844-158">Die [from](https://msdn.microsoft.com/library/Aa258869.aspx) -Anweisung enthält den Namen des Verbindungs Verzeichnis Servers, von dem diese Informationen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="30844-158">The [FROM](https://msdn.microsoft.com/library/Aa258869.aspx) statement contains the name of the linked directory server where this information will be obtained from.</span></span>
-   <span data-ttu-id="30844-159">Die [Where](https://msdn.microsoft.com/library/Aa260674.aspx) -Anweisung stellt die Suchbedingungen bereit.</span><span class="sxs-lookup"><span data-stu-id="30844-159">The [WHERE](https://msdn.microsoft.com/library/Aa260674.aspx) statement provides the search conditions.</span></span> <span data-ttu-id="30844-160">In diesem Beispiel wird nach Kontakten gesucht.</span><span class="sxs-lookup"><span data-stu-id="30844-160">In this example, it is searching for contacts.</span></span>

<span data-ttu-id="30844-161">Die abschließende [Select](https://msdn.microsoft.com/library/Aa259187.aspx) -Anweisung wird verwendet, um Ergebnisse aus der Ansicht zu übernehmen, die angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="30844-161">The final [SELECT](https://msdn.microsoft.com/library/Aa259187.aspx) statement is used to pick up results from the view to display.</span></span>


```sql
CREATE VIEW viewADContacts
AS
SELECT  [Name], sn [Last Name], street [Street], l [City], st [State]
FROM OPENQUERY( ADSI, 
     'SELECT name, sn, street, l, st
      FROM 'LDAP:// OU=Sales,DC=activeds,DC=Fabrikam,DC=Com'
      WHERE objectCategory='Person' AND 
      objectClass = 'contact'')
GO
SELECT * FROM viewADContacts
```



 

 




