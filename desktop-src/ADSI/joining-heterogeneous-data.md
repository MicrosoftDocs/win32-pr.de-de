---
title: Verknüpfen heterogener Daten
description: Typische Organisationen speichern Daten in mehreren heterogenen Datenbanken. Personaldaten können in SQL Server gespeichert werden, während Kontoverwaltungsdaten im Verzeichnis gespeichert werden. Andere Daten können in proprietären Formaten gespeichert werden.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409ac4e82d735f5099bb8846a59683075007c3fbdf56600bc5ae01e6863ffa2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657000"
---
# <a name="joining-heterogeneous-data"></a>Verknüpfen heterogener Daten

Typische Organisationen speichern Daten in mehreren heterogenen Datenbanken. Personaldaten können in SQL Server gespeichert werden, während Kontoverwaltungsdaten im Verzeichnis gespeichert werden. Andere Daten können in proprietären Formaten gespeichert werden.

Mit SQL Server 7.0, ADSI und dem OLE DB-Anbieter ist es möglich, Daten aus Active Directory mit Daten in SQL Server zu verbinden und eine Ansicht der verknüpften Daten zu erstellen.

**So verbinden Sie Active Directory-Daten mit SQL Server Data**

1.  Ausführen der **SQL Query Analyzer** (Start Programs Microsoft SQL Server \| \| 7.0)
2.  Melden Sie sich beim SQL Server Computer an.
3.  Führen Sie die folgende Zeile aus (indem Sie sie markieren und STRG+E drücken):

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    In dieser Zeile sind die Argumente für die [gespeicherte Systemprozedur sp \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) wie folgt:

    -   "ADSI" ist das **Serverargument,** bei dem es sich um den Namen dieses Verbindungsservers handelt.
    -   "Active Directory-Dienste" ist das **srvproduct-Argument,** das den Namen der OLE DB Datenquelle darstellt, die Sie als Verbindungsserver hinzufügen.
    -   "ADSDSOObject" ist das **\_ Anbieternamenargument** und gibt an, dass Sie den OLE DB-Anbieter verwenden.
    -   "adsdatasource" ist das **\_ Datenquellenargument**, bei dem es sich um den Namen der Datenquelle handelt, wie er vom OLE DB-Anbieter interpretiert wird.

    Sie können jetzt den Verbindungsserver verwenden, um über SQL Server auf Active Directory zuzugreifen.

4.  Im nächsten Beispiel wird eine Abfrage mithilfe der [OPENQUERY-Anweisung](https://msdn.microsoft.com/library/Aa276848.aspx) ausgeführt. Diese Anweisung verfügt über zwei Argumente: ADSI, d. h. den Namen des gerade erstellten Verbindungsservers, und eine Abfrage-Anweisung. Die Abfrage-Anweisung enthält die folgenden Elemente:

    -   Die [SELECT-Anweisung](https://msdn.microsoft.com/library/Aa259187.aspx) enthält die Liste der Daten, die vom Verzeichnisdienst abgerufen werden. Sie müssen den LDAP-Anzeigenamen verwenden, um anzugeben, nach welchen Daten Sie suchen.
    -   Die [FROM-Anweisung](https://msdn.microsoft.com/library/Aa258869.aspx) enthält den Namen des Verbindungsverzeichnisservers, von dem diese Informationen abgerufen werden.
    -   Die [WHERE-Anweisung](https://msdn.microsoft.com/library/Aa260674.aspx) stellt die Suchbedingungen bereit. In diesem Beispiel wird nach Benutzern gesucht.

    Geben Sie Ein, und führen Sie aus:

    ```sql
    SELECT * FROM OPENQUERY( ADSI, 
        'SELECT name, adsPath 
         FROM 'LDAP://DC=Fabrikam,DC=com' 
         WHERE objectCategory = 'Person' AND objectClass= 'user'')
    ```

    

    Sie können auch den ADSI [LDAP-Dialekt](ldap-dialect.md)verwenden. Beispiel:

    ```sql
    SELECT * FROM OPENQUERY(ADSI,
        '<LDAP://DC=Fabrikam,DC=COM>;(&(objectCategory=Person)(objectClass=user));name, adspath;subtree')
    ```

    

    Im vorherigen Beispiel hat die LDAP-Abfrage vier Teile:

    -   " \<LDAP://DC=Fabrikam,DC=COM> " ist der Distinguished Name des verzeichnisservers, der durchsucht werden soll.
    -   "(&(objectCategory=Person)(objectClass=user))" ist der LDAP-Suchfilter (siehe [Suchfiltersyntax](search-filter-syntax.md)).
    -   "name, adspath" sind die Namen (im LDAP-Anzeigenamenformat) der abzurufenden Attribute.
    -   "subtree" gibt den [Bereich](scope-of-query.md) der Suche an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen und Ausführen einer Ansicht](creating-and-executing-a-view.md)
</dt> </dl>

 

 




