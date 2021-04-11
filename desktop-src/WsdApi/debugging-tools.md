---
description: Ein debugtoolset, das auf Web Services on Devices API (WSDAPI) basiert, ist im Windows SDK und im Windows-Treiberkit (WDK) verfügbar.
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Debugtools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29965bb85ccfd2daf00612b09bb013ae170dddcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131824"
---
# <a name="debugging-tools"></a>Debugtools

Ein debugtoolset, das auf Web Services on Devices API (WSDAPI) basiert, ist im Windows SDK und im Windows-Treiberkit (WDK) verfügbar. Mit diesen Tools können Sie die Funktionalität von benutzerdefinierten Anwendungen testen, die auf WSDAPI geschrieben wurden, oder Geräte und Clients, die mit einem anderen Geräte Profil für Webdienst Stapel (DPWS) geschrieben wurden.

Mithilfe der WSD-Debug-Hosts (wsddebug \_ -host.exe) und WSD Debug-Client (wsddebug \_client.exe)-Tools können Sie die Merkmale von DPWS-Clients oder-Hosts überprüfen. Sie können auch verwendet werden, um Konnektivitätsprobleme oder Konfigurationsprobleme zu beheben. Weitere Informationen finden Sie im [Handbuch zur Problembehandlung für WSDAPI](wsdapi-troubleshooting-guide.md). Diese Tools sind nur im SDK verfügbar. Die SDK-Tools befinden sich im folgenden Verzeichnis: <Windows SDK Install Folder> \\ bin.

Das [WSDAPI Basic Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx) kann verwendet werden, um die Interoperabilität auf SOAP-oder auf Transport Ebene zu testen (d. h. sicherzustellen, dass Nachrichten wohl geformt sind). Dieses Tool ist nur im WDK verfügbar.

## <a name="the-wsd-debug-client"></a>Der WSD-Debugclient

Der WSD-Debugclient (wsddebug- \_client.exe) bietet eine interaktive Konsole, die zum Senden und empfangen von WS-Discovery Meldungen und zum Abrufen von Metadaten verwendet werden kann. Sie kann auch verwendet werden, um unformatierte Multicast Nachrichten zu generieren und zu verwenden.

Der WSD-Debugclient kann in einem von drei Modi betrieben werden: Multicast, Ermittlung und Metadaten.



| Mode      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Multicast | Im Multicast Modus sendet und empfängt der WSD-Debugclient nicht formatierte Multicast Nachrichten an UDP-Port 3702, wie in WS-Discovery definiert. Der Benutzer kann diese SOAP-Nachrichten in einer Textdatei speichern und die Nachrichten mit dem WSD-Debugclient ändern und erneut übertragen.                                                                                                                                 |
| Ermittlung | Im Ermittlungs Modus sendet und empfängt der WSD-Debugclient formatierte WS-Discovery Nachrichten. Sie kann empfangene Meldungen [Hello](hello-message.md), [Bye](bye-message.md), [Probe Matches](probematches-message.md)und [resolvematches](resolvematches-message.md) anzeigen. Er kann Testnachrichten über UDP oder [http senden und Nachrichten über](probe-message.md) UDP [Auflösen](resolve-message.md) . |
| Metadaten  | Zusätzlich zur Implementierung aller Features des Ermittlungs Modus versucht der metadatenmodus auch, Metadaten von Geräten abzurufen.                                                                                                                                                                                                                                                                    |



 

Weitere Informationen finden Sie unter [Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md), [Verwenden eines generischen Hosts und Clients für die UDP-WS-](using-a-generic-host-and-client-for-udp-ws-discovery.md)Ermittlung und [Verwenden des WSD-Debugclients zum Überprüfen von Multicast Datenverkehr](using-wsddebug-client-to-verify-multicast-traffic.md).

## <a name="the-wsd-debug-host"></a>Der WSD-debughost

Der WSD-debughost (wsddebug- \_host.exe) stellt eine interaktive Konsole bereit, mit der der Host angekündigt, auf Client Anforderungen reagiert und Diagnoseinformationen ausgegeben werden.

Der WSD-debughost funktioniert in einem von zwei Modi: Ermittlung und Metadaten.



| Mode      | BESCHREIBUNG                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ermittlung | Im Ermittlungs Modus druckt der WSD-debughost formatierte WS-Discovery Meldungen. Außerdem sendet Sie [Hello](hello-message.md) -und [Bye](bye-message.md) -Nachrichten und antwortet [automatisch auf Test](probe-message.md) -und [Auflösungs](resolve-message.md) Meldungen. |
| Metadaten  | Zusätzlich zur Implementierung aller Features des Ermittlungs Modus gibt der metadatenmodus einen Metadatendienst aus und ermöglicht Clients das Herstellen einer Verbindung und das Ausführen von Metadatenaustausch.                                                                                       |



 

Weitere Informationen finden Sie unter [Verwenden eines generischen Hosts und Clients für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md) und [Verwenden eines generischen Hosts und Clients für UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSD-Anwendungsentwicklung unter Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[WSDAPI-Entwicklungs Tools](wsdapi-development-tools.md)
</dt> <dt>

[WSDAPI-Handbuch zur Problembehandlung](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



