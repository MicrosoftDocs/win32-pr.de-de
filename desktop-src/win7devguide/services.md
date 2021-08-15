---
title: Dienste (Windows 7 Entwicklerhandbuch)
description: Windows 7 bietet eine leistungsstarke, hochgradig erweiterbare und verwaltbare Plattform zum Erstellen und Integrieren der Webdienste und Anwendungen der Zukunft. Windows 7 bietet sowohl APIs mit verwaltetem Code als auch native APIs zum Erstellen und Ausführen von Webdiensten.
ms.assetid: 6a027e0c-28a0-41cf-b96f-ed988c64c92a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42fe2a59a69efe7fb34bb4a09c58b2ee03f00ac8b8129c36b1ef5f0f61971c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203863"
---
# <a name="services-windows-7-developer-guide"></a>Dienste (Windows 7 Entwicklerhandbuch)

Windows 7 bietet eine leistungsstarke, hochgradig erweiterbare und verwaltbare Plattform zum Erstellen und Integrieren der Webdienste und Anwendungen der Zukunft.

Windows 7 bietet sowohl APIs mit verwaltetem Code als auch native APIs zum Erstellen und Ausführen von Webdiensten. Eine Vielzahl neuer Features basiert auf einer neuen Erweiterbarkeitsebene, die es Entwicklern ermöglicht, alle APIs in nativem Code oder innerhalb des Microsoft-.NET Framework.

Windows 7 können Entwickler auch bessere Zwischenspeicherungs- und Suchfunktionen nutzen. Mit diesen Verbesserungen können Entwickler Daten schneller abrufen und die Netzwerkbandbreitennutzung reduzieren.

## <a name="windows-web-services"></a>Windows Webdienste

Mit [Windows Webdiensten können](/windows/desktop/wsw/portal)Sie Anwendungen erstellen, die problemlos mit einem lokalen Computer oder einem Remotewebdienst kommunizieren. Windows Webdienste sind eine native Codeimplementierung von SOAP und bieten kernbasierte Netzwerkkommunikation, indem sie einen breiten Satz von Webdiensten *(WS)* von Protokollen unterstützen. Windows Webdienste sind ein Peer Windows [Communication Foundation](/previous-versions/windows/desktop/cc907054(v=vs.85)) (*WCF*, Webdienste mit verwaltetem Code) und stellen eine leistungsstarke Teilmenge der *WCF-Funktionalität* zur Verfügung. Windows Webdienste bieten die folgenden Vorteile:

-   Die Fähigkeit, native Codewebdienste in C/C++ in Windows Client und Server zu erstellen.
-   Umfassende Integration in [Windows Communication Foundation-Dienste.](/previous-versions/windows/desktop/cc907054(v=vs.85))
-   Die Möglichkeit, Webdienste mit minimaler Startzeit zu erstellen.
-   Die Fähigkeit, Dienste basierend auf der *WS-Kernfamilie* von Protokollen und *W3C-Standards zu* erstellen.
-   Die Möglichkeit, Webdienste in Umgebungen mit eingeschränkten Ressourcen zu verwenden.

Weitere Informationen finden Sie unter [Windows Web Services-API](../wsw/portal.md) und [Implementieren von Webdiensten mit der Windows Web Services-API.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/web/WWSAPI)

## <a name="distributed-routing-table"></a>Verteilte Routingtabelle

Windows 7 erleichtert das Erstellen anspruchsvoller Peer-zu-Peer-Anwendungen wie verteilte Dateisysteme und Inhaltsverteilungsnetzwerke mit der Tabelle für [verteiltes Routing.](/windows/desktop/P2PSdk/distributed-routing-table-api-reference) Die Verteilte Routingtabelle bietet einen sicheren, skalierbaren Mechanismus zum Veröffentlichen und Suchen nach Schlüsseln in einem Peer-zu-Peer-System. Sie kann verwendet werden, um verteilte Hashtabellen zu erstellen und Topologien für Overlaynetzwerke zu erstellen. (Siehe [Distributed Routing Tabellen-API](../p2psdk/distributed-routing-table-api.md).)

## <a name="windows-branchcache"></a>**Windows BranchCache**

Windows 7 verbessert die Reaktionsfähigkeit von Anwendungen zwischen zentralen Servern und Zweigstellencomputern. In den heutigen Netzwerken ist die Kommunikation zwischen zentralen Servern und Zweigstellen häufig überlastet, was zu einer langsameren Leistung für Anwendungen in der Filiale führt. Mit Windows BranchCache können Clients Daten von anderen Clients in ihrem eigenen Branch abrufen, die die Daten bereits heruntergeladen haben, anstatt die Daten über Remoteserver abrufen zu müssen. Daher nimmt der WAN-Link-Datenverkehr (Wide Area Network) ab, und die Reaktionsfähigkeit der Anwendung verbessert sich. Der Cache speichert eine Kopie aller Inhalte, die clients im Branch angefordert haben, und stellt sicher, dass nur die clients, die vom Inhaltsserver autorisiert sind, auf die angeforderten Daten zugreifen können, während die End-to-End-Verschlüsselung der Daten beibehalten wird.

Windows BranchCache ist bereits in HTTP und Server Message Block (SMB) integriert. Wenn eine Anwendung die WindowsAPIs für eines dieser Protokolle verwendet, kann Windows BranchCache dazu beitragen, die Leistung dieser Anwendung auf Windows 7 zu steigern, ohne Änderungen vorzunehmen.

Wenn Ihre Anwendung dieselben Daten mehrmals von einem Server über eine WAN-Verbindung abruft und nicht automatisch mithilfe von Windows 7 optimiert wird, können Sie die Windows BranchCacheAPIs einfach verwenden, um Ihre Anwendung so zu optimieren, dass sie schneller auf Windows 7 funktioniert und Ihre Branchbenutzer erfüllt.

Diese neuen Features tragen dazu bei, den WAN-Datenverkehr und die Latenz zu reduzieren und gleichzeitig die Einhaltung von Sicherheitsanforderungen sicherzustellen. (Siehe [Peerverteilung](../p2psdk/peer-distribution.md).)

 

 
