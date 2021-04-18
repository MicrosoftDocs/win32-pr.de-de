---
title: Dienste (Windows 7-Entwicklerhandbuch)
description: Windows 7 bietet eine leistungsfähige, hochgradig erweiterbare und verwaltbare Plattform zum entwickeln und integrieren der Webdienste und Anwendungen in der Zukunft. Windows 7 bietet sowohl APIs für verwalteten Code als auch Native APIs zum entwickeln und Ausführen von Webdiensten.
ms.assetid: 6a027e0c-28a0-41cf-b96f-ed988c64c92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aab84cbb522f21b9a09a85d80ef25bf1c858baf
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341340"
---
# <a name="services-windows-7-developer-guide"></a>Dienste (Windows 7-Entwicklerhandbuch)

Windows 7 bietet eine leistungsfähige, hochgradig erweiterbare und verwaltbare Plattform zum entwickeln und integrieren der Webdienste und Anwendungen in der Zukunft.

Windows 7 bietet sowohl APIs für verwalteten Code als auch Native APIs zum entwickeln und Ausführen von Webdiensten. Eine Reihe neuer Features basiert auf einer neuen Erweiterbarkeits Schicht, mit der Entwickler alle APIs in nativem Code oder innerhalb des Microsoft .NET Frameworks erweitern können.

Mit Windows 7 können Entwickler auch bessere zwischen Speicherungs-und Suchfunktionen nutzen. Dank dieser Verbesserungen können Entwickler Daten schneller abrufen und die Auslastung der Netzwerkbandbreite verringern.

## <a name="windows-web-services"></a>Windows-Webdienste

Mit [Windows-Webdiensten](/windows/desktop/wsw/portal)können Sie Anwendungen erstellen, die problemlos mit einem lokalen Computer oder einem Remoteweb Dienst kommunizieren. Bei Windows-Webdiensten handelt es sich um eine Implementierung von SOAP mit System eigenem Code, die eine zentrale Netzwerkkommunikation bietet, indem eine breite Palette von Protokollen für die Webdienste (*WS*) unterstützt wird. Windows-Webdienste ist ein Peer-to- [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) (*WCF*, Managed-Code-Webdienste) und bietet eine leistungsstarke Teilmenge von *WCF* -Funktionen. Windows-Webdienste bieten die folgenden Vorteile:

-   Die Fähigkeit zum Erstellen von Webdiensten für nativen Code in C/C++ in Windows-Client und-Server.
-   Umfassende Integration in [Windows Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) Services.
-   Die Möglichkeit zum Erstellen von Webdiensten mit minimaler Startzeit.
-   Die Möglichkeit zum Erstellen von Diensten basierend auf der Kern- *WS* -Familie von Protokollen und *W3C* -Standards.
-   Die Möglichkeit, Webdienste in Umgebungen mit eingeschränkten Ressourcen zu verwenden.

Weitere Informationen finden Sie unter [Windows-Webdienste-API](../wsw/portal.md) und [Implementieren von Webdiensten mit der Windows-Webdienste-API](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/web/WWSAPI).

## <a name="distributed-routing-table"></a>Tabelle verteilter Routing

Windows 7 vereinfacht das Erstellen ausgereifter Peer-to-Peer-Anwendungen wie z. b. verteilter Dateisysteme und Inhalts Verteilungs Netzwerken mit der [verteilten Routing Tabelle](/windows/desktop/P2PSdk/distributed-routing-table-api-reference). Die Tabelle verteiltes Routing bietet einen sicheren, skalierbaren Mechanismus zum Veröffentlichen und suchen von Schlüsseln in einem Peer-zu-Peer-System. Sie kann zum Erstellen verteilter Hash Tabellen und zum Erstellen von Topologien für Überlagerungs Netzwerke verwendet werden. (Siehe [verteiltes Routing Tabellen-API](../p2psdk/distributed-routing-table-api.md).)

## <a name="windows-branchcache"></a>**Windows BranchCache**

Windows 7 verbessert die Reaktionsfähigkeit von Anwendungen zwischen zentralen Servern und Zweigstellen Computern. In den heutigen Netzwerken wird die Kommunikation zwischen zentralen Servern und Filialen häufig beeinträchtigt, was zu einer geringeren Leistung für Anwendungen in der Zweigstelle führt. Mit Windows BranchCache können Clients Daten von anderen Clients in einer eigenen Verzweigung abrufen, die die Daten bereits heruntergeladen haben, anstatt die Daten über Remote Server abrufen zu müssen. Folglich nimmt der WAN-Datenverkehr (Wide Area Network) ab, und die Reaktionsfähigkeit der Anwendung verbessert sich. Der Cache speichert eine Kopie des gesamten Inhalts, der von den Clients in der Verzweigung angefordert wurde, und stellt sicher, dass nur die vom Inhalts Server autorisierten Clients auf die angeforderten Daten zugreifen können und gleichzeitig die End-to-End-Verschlüsselung der Daten beibehalten wird.

Windows BranchCache ist bereits in http und Server Message Block (SMB) integriert. Wenn eine Anwendung Windows Update is für eines dieser Protokolle verwendet, kann Windows BranchCache dabei helfen, die Leistung dieser Anwendung unter Windows 7 zu steigern, ohne Änderungen daran vorzunehmen.

Wenn Ihre Anwendung die gleichen Daten mehrmals von einem Server über eine WAN-Verbindung abruft und nicht automatisch mit Windows 7 optimiert wird, können Sie mit Windows BranchCache eapis Ihre Anwendung so optimieren, dass Sie schneller auf Windows 7 ausgeführt werden kann und Ihre Zweigstellen Benutzer erfüllen.

Diese neuen Features helfen, den WAN-Datenverkehr und die Latenz zu verringern und gleichzeitig die Einhaltung der Sicherheitsvorgaben (Siehe [Peer Verteilung](../p2psdk/peer-distribution.md).)

 

 
