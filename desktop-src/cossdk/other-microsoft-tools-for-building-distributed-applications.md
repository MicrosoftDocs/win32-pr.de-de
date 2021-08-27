---
description: Andere Microsoft-Tools zum Erstellen verteilter Anwendungen
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Andere Microsoft-Tools zum Erstellen verteilter Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9114454dbbeaa3c8f21cc1ea5166f93760fdd99772425f0245d7b8883f2db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070400"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a>Andere Microsoft-Tools zum Erstellen verteilter Anwendungen

Zusätzlich zu den Tools in COM+ stellt Microsoft die folgenden Tools zur Verfügung, mit denen Entwickler verteilte Anwendungen erstellen können:

-   Microsoft Data Access Components (MDAC). Microsoft bietet mehrere Möglichkeiten zum Abrufen von Daten aus unzähligen Quellen. Beispielsweise bietet OLE DB eine Reihe von COM-Schnittstellen zum Erstellen von Datenbankkomponenten. Die Schnittstellen werden so definiert, dass Datenanbieter basierend auf den Funktionen des zugrunde liegenden Datenspeichers unterschiedliche Unterstützungsebenen implementieren können. Da OLE DB COM-basiert ist, kann es problemlos erweitert werden, und Erweiterungen werden als neue Schnittstellen implementiert. OLE DB enthält auch eine Programmierschnittstelle auf Anwendungsebene, die als ActiveX Data Objects (ADO) bezeichnet wird. ADO macht duale Schnittstellen verfügbar, sodass es problemlos in Skriptsprachen sowie in Microsoft Visual C++, Visual Basic und anderen Entwicklertools verwendet werden kann.

    > [!Note]  
    > Entwickler können auch eine generische, anbieterneutrale API verwenden, z. B. die Anwendungsprogrammierschnittstelle (APPLICATION Programming Interface, API) von Microsoft Open Database Connectivity (ODBC). Die ODBC-API ist eine C-Sprachschnittstelle für den Zugriff auf Daten in einem DBMS mit strukturierte Abfragesprache (SQL). Ein ODBC-Treiber-Manager stellt die Programmierschnittstelle und Laufzeitkomponenten bereit, um DBMS-spezifische Treiber zu suchen. ODBC-Treiber, die in der Regel vom DBMS-Anbieter bereitgestellt werden, übersetzen generische Aufrufe des ODBC-Treiber-Managers in Aufrufe der nativen Datenzugriffsmethode. Der Hauptvorteil der Verwendung der ODBC-API ist, dass Sie nur eine API erlernen müssen, um auf eine vielzahl von DBMSs zuzugreifen.

     

-   Microsoft SQL Server. Zusätzlich zur Bereitstellung eines robusten und eloquenten relationalen Datenbanksystems kann Microsoft SQL Server eine verteilte Anwendung mit Verbindungspooling und Sicherheit bereitstellen, die in das Windows-Sicherheitsmodell integriert werden kann.

-   COM Transaction Integration (COMTI). COMTI kann verwendet werden, um Mainframesysteme in Windows, einschließlich COM+-Anwendungen, zu integrieren. COMTI verwendet Standardkommunikationsprotokolle (z. B. LU 6.2) für die Kommunikation zwischen Windows Computern und Mainframe- und Minicomputern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+-Entwurfsannahmen und -prinzipien](com--design-assumptions-and-principles.md)
</dt> <dt>

[Entwerfen der COM+-Anwendung mit UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Allgemeine Entwurfs Tipps für die Verwendung von COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimieren von Interaktionen mit der COM+-Geschäftslogikebene](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



