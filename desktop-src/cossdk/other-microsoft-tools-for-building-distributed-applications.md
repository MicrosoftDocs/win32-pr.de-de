---
description: Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346648"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a>Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen

Zusätzlich zu den Tools in com+ bietet Microsoft die folgenden Tools zum unterstützen des Entwicklers bei der Erstellung verteilter Anwendungen:

-   Microsoft Data Access Components (MDAC). Microsoft bietet mehrere Möglichkeiten zum Abrufen von Daten aus einer Vielzahl von Quellen. OLE DB bietet z. b. eine Reihe von COM-Schnittstellen zum Entwickeln von Datenbankkomponenten. Die Schnittstellen sind so definiert, dass Datenanbieter unterschiedliche Unterstützungs Ebenen implementieren können, basierend auf den Funktionen des zugrunde liegenden Datenspeicher. Da OLE DB com-basiert ist, kann es problemlos erweitert werden, und Erweiterungen werden als neue Schnittstellen implementiert. OLE DB umfasst auch eine Programmierschnittstelle auf Anwendungsebene mit dem Namen ActiveX Data Objects (ADO). ADO stellt duale Schnittstellen zur Verfügung, sodass es problemlos von Skriptsprachen sowie Microsoft Visual C++, Visual Basic und anderen Entwicklertools verwendet werden kann.

    > [!Note]  
    > Entwickler können auch eine generische, Anbieter neutrale API verwenden, wie z. b. die Microsoft Open Database Connectivity (ODBC)-API (Application Programming Interface). Die ODBC-API ist eine Schnittstelle der Programmiersprache C für den Zugriff auf Daten in einem DBMS mithilfe von Structured Query Language (SQL). Ein ODBC-Treiber-Manager stellt die Programmierschnittstelle und Laufzeitkomponenten zum Auffinden von DBMS-spezifischen Treibern bereit. ODBC-Treiber, die in der Regel vom DBMS-Anbieter bereitgestellt werden, übersetzen generische Aufrufe aus dem ODBC-Treiber-Manager in Aufrufe der systemeigenen Datenzugriffs Methode. Der Hauptvorteil der Verwendung der ODBC-API besteht darin, dass Sie nur eine API erlernen müssen, um auf eine große Bandbreite von DBMSs zuzugreifen.

     

-   Microsoft SQL Server. Zusätzlich zur Bereitstellung eines robusten und eloquenten relationalen Datenbanksystems können Microsoft SQL Server eine verteilte Anwendung mit Verbindungspooling und Sicherheit bereitstellen, die in das Windows-Sicherheitsmodell integriert werden können.

-   COM-Transaktions Integration (com Transaction Integration, COMTI) COMTI kann verwendet werden, um Main Frame-Systeme in Windows-Systeme zu integrieren, einschließlich com+-Anwendungen. COMTI verwendet Standard Kommunikationsprotokolle (z. b. lu 6,2) für die Kommunikation zwischen Windows-Computern und Main Frame und Minicomputers.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Entwurfs Annahmen und-Prinzipien](com--design-assumptions-and-principles.md)
</dt> <dt>

[Entwerfen der com+-Anwendung mithilfe von UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Allgemeine Entwurfs Tipps für die Verwendung von com+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimieren von Interaktionen mit der com+-Geschäftslogik Ebene](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



