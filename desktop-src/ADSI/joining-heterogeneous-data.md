---
title: Beitreten zu heterogenen Daten
description: In typischen Organisationen werden Daten in mehreren heterogenen Datenbanken gespeichert. Personaldaten können in SQL Server gespeichert werden, während die Konto Verwaltungsdaten im Verzeichnis gespeichert werden. Andere Daten können in proprietären Formaten gespeichert werden.
ms.assetid: 45281b42-5cb2-42f9-9c7c-f3e3174b0f9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e1099028bc85dc6492eade0315b7308b4c6aaa9
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314613"
---
# <a name="joining-heterogeneous-data"></a>Beitreten zu heterogenen Daten

In typischen Organisationen werden Daten in mehreren heterogenen Datenbanken gespeichert. Personaldaten können in SQL Server gespeichert werden, während die Konto Verwaltungsdaten im Verzeichnis gespeichert werden. Andere Daten können in proprietären Formaten gespeichert werden.

Mit SQL Server 7,0, ADSI und der OLE DB-Anbieter ist es möglich, Daten aus Active Directory mit Daten in SQL Server zu verknüpfen und eine Ansicht der verknüpften Daten zu erstellen.

**So verknüpfen Sie Active Directory Daten mit SQL Server Daten**

1.  Ausführen von **SQL Query Analyzer** ( \| Programme starten \| Microsoft SQL Server 7,0)
2.  Melden Sie sich beim SQL Server Computer an.
3.  Führen Sie die folgende Zeile aus (indem Sie Sie markieren und STRG + E drücken):

    ```sql
    EXEC sp_addlinkedserver 'ADSI', 'Active Directory Service Interfaces', 
    'ADSDSOObject', 'adsdatasource'
    GO
    ```

    

    In dieser Zeile lauten die Argumente für die gespeicherte System Prozedur [SP \_ addlinkedserver](https://msdn.microsoft.com/library/Aa259589.aspx) wie folgt:

    -   "ADSI" ist das **Server** Argument, bei dem es sich um den Namen dieses Verbindungs Servers handelt.
    -   "Active Directory Services" ist das **srvproduct** -Argument, bei dem es sich um den Namen der OLE DB Datenquelle handelt, die Sie als Verbindungs Server hinzufügen.
    -   "ADSDSOObject" ist das **Anbieter \_ Namen** Argument und gibt an, dass Sie den OLE DB Anbieter verwenden.
    -   "adsdatasource" ist das **Daten \_ Quellen Argument**, bei dem es sich um den Namen der Datenquelle handelt, die vom OLE DB Anbieter interpretiert wird.

    Sie können jetzt den Verbindungs Server verwenden, um auf Active Directory aus SQL Server zuzugreifen.

4.  Im nächsten Beispiel wird eine Abfrage mithilfe der [OPENQUERY](https://msdn.microsoft.com/library/Aa276848.aspx) -Anweisung durchführt. Diese Anweisung hat zwei Argumente: ADSI, den Namen des soeben erstellten Verbindungs Servers und eine Abfrage Anweisung. Die Abfrage Anweisung enthält die folgenden Elemente:

    -   Die [Select](https://msdn.microsoft.com/library/Aa259187.aspx) -Anweisung enthält die Liste der Daten, die vom Verzeichnisdienst abgerufen werden. Sie müssen den LDAP-anzeigen Amen verwenden, um anzugeben, nach welchen Daten Sie suchen.
    -   Die [from](https://msdn.microsoft.com/library/Aa258869.aspx) -Anweisung enthält den Namen des Verbindungs Verzeichnis Servers, von dem diese Informationen abgerufen werden.
    -   Die [Where](https://msdn.microsoft.com/library/Aa260674.aspx) -Anweisung stellt die Suchbedingungen bereit. In diesem Beispiel sucht es nach Benutzern.

    Typ und Execute:

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

    

    Im vorherigen Beispiel besteht die LDAP-Abfrage aus vier Teilen:

    -   " \<LDAP://DC=Fabrikam,DC=COM> " ist der Distinguished Name des Verzeichnis Servers, der durchsucht werden soll.
    -   "(& (objectCategory = Person) (objectClass = User))" ist der LDAP-Suchfilter (siehe [Syntax für Suchfilter](search-filter-syntax.md)).
    -   "Name, ADsPath" sind die Namen (mit dem Format des LDAP-Anzeige namens) der abzurufenden Attribute.
    -   "subtree" gibt den Such [Bereich](scope-of-query.md) an.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen und Ausführen einer Ansicht](creating-and-executing-a-view.md)
</dt> </dl>

 

 




