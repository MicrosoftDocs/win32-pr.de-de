---
title: Suchen nach Active Directory
description: Eine wichtige Funktion von Active Directory ist das Auflösen von Datenabfragen für Personen sowie Konfigurationsdaten für Computer und Dienste.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Suchen nach Active Directory ADSI
- ADSI ADSI , Active Directory durchsuchen
- fragt ADSI ab und sucht nach Active Directory.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d3ec83268556ebcacd89efeca425db87e2c0cc06e69a1e6eea810bcd6a21de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005470"
---
# <a name="searching-active-directory"></a>Suchen nach Active Directory

Eine wichtige Funktion von Active Directory ist das Auflösen von Datenabfragen für Personen sowie Konfigurationsdaten für Computer und Dienste. Um effiziente Abfragen für Active Directory zu schreiben, ist es hilfreich, sich mit den folgenden Themen vertraut zu machen:

-   Bestimmen des Abfragebereichs: Muss der Client Eigenschaften für Objekte finden, die sich möglicherweise an einer beliebigen Stelle innerhalb einer Gesamtstruktur oder nur innerhalb einer Domäne oder innerhalb einer bestimmten Organisationseinheit (OE) befinden?
-   Bestimmen der Tiefe der Abfrage: Muss die Abfrage nur eine Ebene durchsuchen oder kann sie in andere LDAP-Verzeichnisse übergehen?
-   Leistung und Verarbeitung großer Resultsets: Wie sollte der Client das Potenzial eines großen Resultsets effektiv behandeln?
-   Ermitteln der besten Abfragen: Welche Art von Abfragen liefert die effizientesten Ergebnisse? Welche Art von Abfragen sollte der Entwickler vermeiden?
-   Grundlegendes zur Abfragesyntax: ADSI unterstützt sowohl die LDAP-Syntax, wie in RFC 2254 dokumentiert, als auch eine Teilmenge der SQL.
-   Auswahl von Schnittstellen: ADSI bietet sowohl OLE DB-Unterstützung als auch eine C/C++-Schnittstelle namens [**IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) Da ADSI für mehrere Namespaces funktioniert, können Sie diese Schnittstellen zum Abfragen anderer Namespaces wie Exchange und Active Directory verwenden. Da das ActiveX Data Object (ADO) ein einfaches skriptfähiges Datenzugriffsobjektmodell ist, das auf OLE DB basiert, funktionieren die OLE DB Schnittstellen gut für Visual Basic Programmierer und Webseitenskriptwriter. Die neuen Datenzugriffsfeatures in Visual Studio und Office Anwendungen, die ADO und OLE DB nutzen, können jetzt auf die gleiche Weise auf Active Directory-Daten zugreifen wie von anderen OLE DB Anbietern, z. B. SQL Server. Wenn ein C/C++-Entwickler jedoch eine einfache Verzeichnissuche durchführen muss, ist die **IDirectorySearch-Schnittstelle** möglicherweise besser geeignet als die OLE DB Schnittstellen.

In den folgenden Themen wird beschrieben, wie Sie Active Directory durchsuchen, um sicherzustellen, dass Ihre Anwendung die effizienteste Abfrage ausgibt, wenn die Anforderungen des Clients erfüllt sind:

-   [Bereich der Abfrage](scope-of-query.md)
-   [Leistung und Verarbeitung großer Resultsets](performance-and-handling-large-result-sets.md)
-   [Suchfiltersyntax](search-filter-syntax.md)
-   [Abfrageschnittstellen](query-interfaces.md)
-   [Durchsuchen von Binärdaten](searching-binary-data.md)
-   [Verteilte Abfrage](distributed-query.md)

 

 




