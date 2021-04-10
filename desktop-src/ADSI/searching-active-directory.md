---
title: Such Active Directory
description: Eine wichtige Funktion von Active Directory besteht darin, Daten Abfragen für Personen und Konfigurationsdaten für Computer und Dienste aufzulösen.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Suchen Active Directory ADSI
- ADSI ADSI, suchen Active Directory
- Abfragen von ADSI, suchen Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309219"
---
# <a name="searching-active-directory"></a>Such Active Directory

Eine wichtige Funktion von Active Directory besteht darin, Daten Abfragen für Personen und Konfigurationsdaten für Computer und Dienste aufzulösen. Wenn Sie effiziente Abfragen für Active Directory schreiben möchten, ist es hilfreich, sich mit folgenden Informationen vertraut zu machen:

-   Bestimmen des Gültigkeits Bereichs der Abfrage: muss der Client Eigenschaften für Objekte suchen, die sich an einer beliebigen Stelle innerhalb einer Gesamtstruktur oder nur innerhalb einer einzelnen Domäne oder innerhalb einer bestimmten Organisationseinheit befinden können?
-   Bestimmen der Tiefe der Abfrage: muss die Abfrage nur eine Ebene durchsuchen oder Sie in andere LDAP-Verzeichnisse überqueren?
-   Leistung und Verarbeitung großer Resultsets: wie soll der Client das Potenzial eines großen Resultsets effektiv verarbeiten?
-   Ermitteln der besten Abfragen: welche Art von Abfragen bietet die effizientesten Ergebnisse? Welche Art von Abfragen sollte der Entwickler vermeiden?
-   Grundlegendes zur Abfrage Syntax: ADSI unterstützt sowohl die LDAP-Syntax, wie in RFC 2254 dokumentiert, als auch eine Teilmenge von SQL.
-   Auswahl der Schnittstellen: ADSI bietet sowohl OLE DB Unterstützung als auch eine C/C++-Schnittstelle mit dem Namen " [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)". Da ADSI für mehrere Namespaces verwendet wird, können Sie diese Schnittstellen zum Abfragen anderer Namespaces (z. b. Exchange) und Active Directory verwenden. Da es sich bei dem ActiveX Data Object (ADO) um ein einfaches Skript fähige Data Access-Objektmodell auf OLE DB handelt, funktionieren die OLE DB Schnittstellen gut für Visual Basic Programmierer und Webseiten Skript Schreiber. Die neuen Datenzugriffs Features innerhalb von Visual Studio und Office-Anwendungen, die ADO und OLE DB nutzen, können jetzt auf die gleiche Weise auf Active Directory Daten zugreifen, wie Sie auf Daten von anderen OLE DB Anbietern wie SQL Server zugreifen. Wenn jedoch ein C/C++-Entwickler eine einfache Verzeichnis Suche ausführen muss, ist die **idirector ysearch** -Schnittstelle möglicherweise besser geeignet als die OLE DB Schnittstellen.

In den folgenden Themen wird beschrieben, wie Sie Active Directory durchsuchen, um sicherzustellen, dass Ihre Anwendung die effizienteste Abfrage mit den Anforderungen des Clients ausgibt:

-   [Abfrage Bereich](scope-of-query.md)
-   [Leistung und Behandlung von großen Resultsets](performance-and-handling-large-result-sets.md)
-   [Such Filter Syntax](search-filter-syntax.md)
-   [Abfrageschnittstellen](query-interfaces.md)
-   [Suchen von Binärdaten](searching-binary-data.md)
-   [Verteilte Abfrage](distributed-query.md)

 

 




