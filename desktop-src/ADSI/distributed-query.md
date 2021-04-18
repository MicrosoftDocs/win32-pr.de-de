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
# <a name="distributed-query"></a>Verteilte Abfrage

Da ADSI ein OLE DB-Anbieter ist, kann er an einer verteilten Abfrage teilnehmen, die in Microsoft SQL Server 7,0 eingeführt wurde. Folgende Szenarien sind möglich:

-   Verbinden von Active Directory-Objekten mit SQL Server Daten.
-   Aktualisieren von SQL-Daten aus Active Directory Objekten.
-   Erstellen von drei-Wege-oder vier-Wege-Joins mit anderen OLE DB Anbietern. Beispielsweise Index Server, SQL Server und Active Directory.

Der OLE DB-Anbieter unterstützt zwei Befehls Dialekte (LDAP und SQL), um auf den Verzeichnisdienst zuzugreifen und Ergebnisse in tabellarischer Form zurückzugeben, die mit SQL Server verteilten Abfragen abgefragt werden können.

**So starten Sie SQL Query Analyzer**

1.  Öffnen Sie zunächst das [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) auf dem SQL Server, das mit dem Verzeichnisdienst verknüpft ist (siehe Erstellen eines Verbindungs Servers).
2.  Ausführen von **SQL Query Analyzer** ( \| Programme starten \| Microsoft SQL Server 7,0)
3.  Melden Sie sich beim SQL Server Computer an.
4.  Geben Sie im Editor-Bereich des Abfrage Fensters die SQL-Abfrage ein.
5.  Führen Sie die Abfrage aus, indem Sie F5 drücken.

In den folgenden Abschnitten finden Sie weitere Details:

-   [Erstellen eines Verbindungs Servers](#creating-a-linked-server)
-   [Erstellen einer SQL Server authentifizierten Anmeldung](#creating-a-sql-server-authenticated-login)
-   [Abfragen des Verzeichnisdienstes (Directory Service)](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a>Erstellen eines Verbindungs Servers

Erstellen Sie einen Verbindungs Server, um einen verteilten Join für einen Windows 2000 Server-Verzeichnisdienst einzurichten. Richten Sie zu diesem Zweck die ADSI-Zuordnung mithilfe der gespeicherten System Prozedur [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) ein. Mit dieser Prozedur wird ein Name mit einem OLE DB Anbieter Namen verknüpft.

Beachten Sie im folgenden Beispiel, dass mehrere Argumente mit der gespeicherten System Prozedur [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) verwendet werden:

-   "ADSI" ist das **Server** Argument und ist der Name dieses Verbindungs Servers.
-   "Active Directory Services 2,5" ist das **srvproduct** -Argument, bei dem es sich um den Namen der OLE DB Datenquelle handelt, die Sie als Verbindungs Server hinzufügen.
-   "ADSDSOObject" ist das **Anbieter \_ Namen** Argument.
-   "adsdatasource" ist das **Daten \_ Quellen** Argument, bei dem es sich um den Namen der Datenquelle handelt, die vom OLE DB Anbieter interpretiert wird.

Der [exec](https://msdn.microsoft.com/library/Aa258848.aspx) -Befehl wird verwendet, um gespeicherte System Prozeduren auszuführen.


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



Bei Windows-authentifizierten Anmeldungen genügt die selbst Zuordnung für den Zugriff auf das Verzeichnis mit SQL Server Sicherheits Delegierung. Da die selbst Zuordnung für Verbindungs Server, die über [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx)erstellt wurden, standardmäßig erstellt wird, ist keine andere Anmeldungs Zuordnung erforderlich.

Für SQL Server – authentifizierte Anmeldungen können Sie geeignete Anmelde Namen und Kenn Wörter für die Verbindung mit dem Verzeichnisdienst mithilfe der gespeicherten System Prozedur [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) konfigurieren.

> [!Note]  
> Verwenden Sie nach Möglichkeit die Windows-Authentifizierung.

 

## <a name="creating-a-sql-server-authenticated-login"></a>Erstellen einer SQL Server authentifizierten Anmeldung

Wenn Sie lieber eine SQL Server – authentifizierte Anmeldung anstelle der Windows-Authentifizierung verwenden möchten, fügen Sie dem Verbindungs Server einen Anmelde Namen hinzu (siehe vorheriger Abschnitt). Verwenden Sie dazu die gespeicherte System Prozedur [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) .

Im folgenden Beispiel werden mehrere Argumente verwendet, die mit der gespeicherten System Prozedur [SP \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) verwendet werden:

-   "ADSI" ist das **rmzvrname** -Argument, bei dem es sich um den Namen des Verbindungs Servers handelt, der im vorherigen Beispiel erstellt wurde.
-   "Fabrikam \\ Administrator" ist das **loczu-Argument** , bei dem es sich um den Anmelde Namen auf dem lokalen Server handelt und der SQL Server-Anmelde Name oder ein Windows NT-Benutzer sein kann.
-   "Cn = Administrator, OU = Sales, DC = activeds, DC = fabrikam, DC = com" ist das **rmtuser** -Argument, bei dem es sich um den Benutzernamen handelt, den Sie zum Herstellen der Verbindung verwenden, da " **roeself** " " **false**" ist.
-   "Secret \* \* 2000" ist das **rmtpassword**, das dem **rmtuser** zugeordneten Kennwort entspricht.

Der [exec](https://msdn.microsoft.com/library/Aa258848.aspx) -Befehl wird verwendet, um gespeicherte System Prozeduren auszuführen.


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a>Abfragen des Verzeichnisdienstes (Directory Service)

Nachdem Sie einen Verbindungs Server erstellt haben, verwenden Sie eine [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) -Anweisung, um eine Abfrage an den Verzeichnisdienst zu senden. Die folgende SQL-Abfrage erstellt eine virtuelle Tabelle, in der die Abfrageergebnisse mit der [CREATE VIEW](https://msdn.microsoft.com/library/Aa258253.aspx) -Anweisung enthalten sind. Die Ansicht, die erstellt wird, hat den Namen "viewadcontacts".

Die erste [Select](https://msdn.microsoft.com/library/Aa259187.aspx) -Anweisung definiert die Informationen, die vom Verzeichnisdienst abgefragt werden, und ordnet Sie einer Spalte in der Tabelle zu. Informationen, die von eckigen Klammern eingeschlossen werden, geben die Daten an, die in die virtuelle Tabelle eingefügt werden. Die Informationen, die nicht in Klammern stehen, zeigen die Daten an, die vom Verzeichnisdienst abgerufen werden. Beachten Sie, dass die Informationen, die aus dem Verzeichnisdienst abgerufen werden, über den LDAP-anzeigen Amen referenziert werden müssen.

Die nächste Anweisung ist die [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) -Anweisung. Diese Anweisung hat zwei Argumente: ADSI, den Namen des erstellten Verbindungs Servers und eine Abfrage Anweisung. Die Abfrage Anweisung enthält die folgenden Elemente:

-   Die [Select](https://msdn.microsoft.com/library/Aa259187.aspx) -Anweisung enthält die Liste der Daten, die vom Verzeichnisdienst abgerufen werden. Sie müssen den LDAP-anzeigen Amen verwenden, um anzugeben, nach welchen Daten Sie suchen.
-   Die [from](https://msdn.microsoft.com/library/Aa258869.aspx) -Anweisung enthält den Namen des Verbindungs Verzeichnis Servers, von dem diese Informationen abgerufen werden.
-   Die [Where](https://msdn.microsoft.com/library/Aa260674.aspx) -Anweisung stellt die Suchbedingungen bereit. In diesem Beispiel wird nach Kontakten gesucht.

Die abschließende [Select](https://msdn.microsoft.com/library/Aa259187.aspx) -Anweisung wird verwendet, um Ergebnisse aus der Ansicht zu übernehmen, die angezeigt werden.


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



 

 




