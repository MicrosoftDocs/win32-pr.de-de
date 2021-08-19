---
title: Verteilte Abfrage
description: Da ADSI ein OLE DB-Anbieter ist, kann es an verteilten Abfragen teilnehmen, die in Microsoft SQL Server 7.0 eingeführt wurden.
ms.assetid: 0a93ec2e-397a-47f7-b00c-f0f9aaa06de6
ms.tgt_platform: multiple
keywords:
- abfragen ADSI , verteilte Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46ab174565d8a02ae9058792aa36ef7c3379453e0ba0f861cddf150abf662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428701"
---
# <a name="distributed-query"></a>Verteilte Abfrage

Da ADSI ein OLE DB-Anbieter ist, kann es an verteilten Abfragen teilnehmen, die in Microsoft SQL Server 7.0 eingeführt wurden. Folgende Szenarien sind möglich:

-   Verknüpfen von Active Directory-Objekten mit SQL Server Daten.
-   Aktualisieren SQL Daten aus Active Directory-Objekten.
-   Erstellen von drei- oder vierstufigen Joins mit anderen OLE DB Anbietern. Beispiel: Indexserver, SQL Server und Active Directory.

Der OLE DB-Anbieter unterstützt zwei Befehlsdialekte, LDAP und SQL, um auf den Verzeichnisdienst zuzugreifen und Ergebnisse in tabellarischer Form zurückzugeben, die mit SQL Server verteilten Abfragen abgefragt werden können.

**So starten Sie die SQL Query Analyzer**

1.  Öffnen Sie zunächst den [SQL Query Analyzer](https://msdn.microsoft.com/library/Aa216983.aspx) auf dem SQL Server, der mit dem Verzeichnisdienst verknüpft ist (siehe Erstellen eines Verbindungsservers).
2.  Ausführen der **SQL Query Analyzer** (Start Programs Microsoft SQL Server \| \| 7.0)
3.  Melden Sie sich beim SQL Server Computer an.
4.  Geben Sie die SQL Abfrage im Bereich Editor des Abfragefensters ein.
5.  Führen Sie die Abfrage durch Drücken von F5 aus.

Die folgenden Abschnitte enthalten weitere Details:

-   [Erstellen eines Verbindungsservers](#creating-a-linked-server)
-   [Erstellen einer SQL Server authentifizierten Anmeldung](#creating-a-sql-server-authenticated-login)
-   [Abfragen des Verzeichnisdienstes (Directory Service)](#querying-the-directory-service)

## <a name="creating-a-linked-server"></a>Erstellen eines Verbindungsservers

Um einen verteilten Join für einen Windows 2000 Server-Verzeichnisdienst einzurichten, erstellen Sie einen Verbindungsserver. Richten Sie hierzu die ADSI-Zuordnung mithilfe der [gespeicherten Systemprozedur sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) ein. Bei dieser Prozedur wird ein Name mit einem OLE DB Anbieternamen verknüpft.

Beachten Sie im folgenden Beispiel, dass es mehrere Argumente gibt, die mit der [gespeicherten Systemprozedur sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) verwendet werden:

-   "ADSI" ist das **Serverargument** und der Name dieses Verbindungsservers.
-   "Active Directory Services 2.5" ist das **srvproduct-Argument,** das den Namen der OLE DB Datenquelle darstellt, die Sie als Verbindungsserver hinzufügen.
-   "ADSDSOObject" ist das **\_ Anbieternamenargument.**
-   "adsdatasource" ist das **\_ Datenquellenargument,** bei dem es sich um den Namen der Datenquelle handelt, wie er vom OLE DB-Anbieter interpretiert wird.

Der [EXEC-Befehl](https://msdn.microsoft.com/library/Aa258848.aspx) wird verwendet, um gespeicherte Systemprozeszen auszuführen.


```sql
EXEC sp_addlinkedserver 'ADSI', 'Active Directory Services 2.5', 
'ADSDSOObject', 'adsdatasource'
GO
```



Für Windows authentifizierte Anmeldungen ist die Selbstzuordnung ausreichend, um mit SQL Server Sicherheitsdelegierung auf das Verzeichnis zuzugreifen. Da die Selbstzuordnung standardmäßig für Verbindungsserver erstellt wird, die mit [sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx)erstellt wurden, ist keine andere Anmeldezuordnung erforderlich.

Für SQL Server authentifizierte Anmeldungen können Sie geeignete Anmeldungen und Kennwörter für die Verbindung mit dem Verzeichnisdienst konfigurieren, indem Sie die gespeicherte Systemprozedur [sp \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) verwenden.

> [!Note]  
> Verwenden Sie nach Möglichkeit die Windows-Authentifizierung.

 

## <a name="creating-a-sql-server-authenticated-login"></a>Erstellen einer SQL Server authentifizierten Anmeldung

Wenn Sie lieber eine SQL Server-authentifizierte Anmeldung anstelle Windows-Authentifizierung verwenden möchten, fügen Sie dem Verbindungsserver eine Anmeldung hinzu (siehe vorheriger Abschnitt). Verwenden Sie hierzu die gespeicherte Systemprozedur [sp \_ addlinkedsrvlogin.](https://msdn.microsoft.com/library/Aa259581.aspx)

Im folgenden Beispiel gibt es mehrere Argumente, die mit der [gespeicherten Systemprozedur sp \_ addlinkedsrvlogin](https://msdn.microsoft.com/library/Aa259581.aspx) verwendet werden:

-   "ADSI" ist das **rmtsvrname-Argument,** bei dem es sich um den Namen des Verbindungsservers handelt, der im vorherigen Beispiel erstellt wurde.
-   "Fabrikam \\ Administrator" ist das **locallogin-Argument,** bei dem es sich um den Anmeldenamen auf dem lokalen Server handelt und der SQL Server-Anmeldung oder ein Windows NT-Benutzer sein kann.
-   "CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com" ist das **rmtuser-Argument,** bei dem es sich um den Benutzernamen handelt, den Sie zum Herstellen der Verbindung verwenden, da **useself** **false** ist.
-   "secret \* \* 2000" ist das **rmtpassword**, das dem **Rmtuser** zugeordnete Kennwort ist.

Der [EXEC-Befehl](https://msdn.microsoft.com/library/Aa258848.aspx) wird verwendet, um gespeicherte Systemprozeszen auszuführen.


```sql
EXEC sp_addlinkedsrvlogin 'ADSI', false, 'Fabrikam\Administrator', 
'CN=Administrator,OU=Sales,DC=activeds,DC=Fabrikam,DC=com', 'secret**2000'
```



## <a name="querying-the-directory-service"></a>Abfragen des Verzeichnisdienstes (Directory Service)

Nachdem Sie einen Verbindungsserver erstellt haben, verwenden Sie eine [OPENQUERY-Anweisung,](https://msdn.microsoft.com/library/Aa276848.aspx) um eine Abfrage an den Verzeichnisdienst zu senden. Mit dem folgenden SQL Abfrage wird eine virtuelle Tabelle erstellt, in der die Abfrageergebnisse mithilfe der [CREATE VIEW-Anweisung](https://msdn.microsoft.com/library/Aa258253.aspx) gespeichert werden. Die erstellte Ansicht heißt "viewADContacts".

Die erste [SELECT-Anweisung](https://msdn.microsoft.com/library/Aa259187.aspx) definiert die Informationen, die vom Verzeichnisdienst abgefragt werden, und ordnet sie einer Spalte in der Tabelle zu. In Klammern eingeschlossene Informationen geben die Daten an, die in die virtuelle Tabelle aufgenommen werden. Die Informationen, die sich nicht in Klammern befinden, geben die Daten an, die vom Verzeichnisdienst abgerufen werden. Beachten Sie, dass auf die Informationen, die vom Verzeichnisdienst abgerufen werden, über den LDAP-Anzeigenamen verwiesen werden muss.

Die nächste Anweisung ist die [OPENQUERY-Anweisung.](https://msdn.microsoft.com/library/Aa276848.aspx) Diese Anweisung verfügt über zwei Argumente: ADSI, d. h. den Namen des von Ihnen erstellten Verbindungsservers, und eine Abfrage-Anweisung. Die Abfrage-Anweisung enthält die folgenden Elemente:

-   Die [SELECT-Anweisung](https://msdn.microsoft.com/library/Aa259187.aspx) enthält die Liste der Daten, die vom Verzeichnisdienst abgerufen werden. Sie müssen den LDAP-Anzeigenamen verwenden, um anzugeben, nach welchen Daten Sie suchen.
-   Die [FROM-Anweisung](https://msdn.microsoft.com/library/Aa258869.aspx) enthält den Namen des Verbindungsverzeichnisservers, von dem diese Informationen abgerufen werden.
-   Die [WHERE-Anweisung](https://msdn.microsoft.com/library/Aa260674.aspx) stellt die Suchbedingungen bereit. In diesem Beispiel wird nach Kontakten gesucht.

Die endgültige [SELECT-Anweisung](https://msdn.microsoft.com/library/Aa259187.aspx) wird verwendet, um ergebnisse aus der anzuzeigende Ansicht zu erhalten.


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



 

 




