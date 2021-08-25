---
description: Ein Debugtoolset, das auf der Web Services on Devices-API (WSDAPI) basiert, ist im Windows SDK und im Windows Driver Kit (WDK) verfügbar.
ms.assetid: bd7efa8b-4f12-4b19-a7df-fa34c6a3444a
title: Debugtools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e744b37a5376d228ac9023ed7556ce63e26a7a1c20b23fb98aff090e7ae9616f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856780"
---
# <a name="debugging-tools"></a>Debugtools

Ein Debugtoolset, das auf der Web Services on Devices-API (WSDAPI) basiert, ist im Windows SDK und im Windows Driver Kit (WDK) verfügbar. Diese Tools können verwendet werden, um die Funktionalität benutzerdefinierter Anwendungen zu testen, die in WSDAPI geschrieben wurden, oder von Geräten und Clients, die mit anderen DPWS-Stapeln (Device Profile for Web Services) geschrieben wurden.

Die Tools WSD-Debughost (wsddebughost.exe) und \_ WSD-Debugclient (wsddebugclient.exe) können verwendet werden, um die Merkmale von DPWS-Clients oder -Hosts zu \_ überprüfen. Sie können auch zur Behandlung von Konnektivitäts- oder Konfigurationsproblemen verwendet werden. Weitere Informationen finden Sie im [Handbuch zur WSDAPI-Problembehandlung.](wsdapi-troubleshooting-guide.md) Diese Tools sind nur im SDK verfügbar. SDK-Tools befinden sich im folgenden Verzeichnis: <Windows SDK Install Folder> \\ Bin.

Das [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) kann verwendet werden, um die Interoperabilität auf SOAP- oder Transportebene zu testen (d.h. um sicherzustellen, dass Nachrichten wohlgeformt sind). Dieses Tool ist nur im WDK verfügbar.

## <a name="the-wsd-debug-client"></a>Der WSD-Debugclient

Der WSD-Debugclient (wsddebugclient.exe) stellt eine interaktive Konsole bereit, die zum Senden und Empfangen von WS-Discovery-Nachrichten und zum Abrufen von Metadaten verwendet werden \_ kann. Sie kann auch verwendet werden, um Unformatierungs-Multicastnachrichten zu generieren und zu nutzen.

Der WSD-Debugclient arbeitet in einem von drei Modi: Multicast, Ermittlung und Metadaten.



| Mode      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Multicast | Im Multicastmodus sendet und empfängt der WSD-Debugclient unformatierte Multicastnachrichten an UDP-Port 3702, wie in WS-Discovery definiert. Der Benutzer kann diese SOAP-Nachrichten in einer Textdatei speichern und die Nachrichten mit dem WSD-Debugclient ändern und erneut übertragen.                                                                                                                                 |
| Ermittlung (Discovery) | Im Ermittlungsmodus sendet und empfängt der WSD-Debugclient formatierte WS-Discovery Nachrichten. Sie kann empfangene [Hello-,](hello-message.md) [Bye-,](bye-message.md) [ProbeMatches-](probematches-message.md)und [ResolveMatches-Meldungen](resolvematches-message.md) anzeigen. Er kann [Testnachrichten über](probe-message.md) UDP oder HTTP senden und [Nachrichten über](resolve-message.md) UDP auflösen. |
| Metadaten  | Zusätzlich zur Implementierung aller Features des Ermittlungsmodus versucht der Metadatenmodus auch, Metadaten von Geräten abzurufen.                                                                                                                                                                                                                                                                    |



 

Weitere Informationen finden Sie unter Verwenden eines generischen Hosts und Clients für [HTTP-Metadaten Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md), Verwenden eines generischen Hosts und Clients für [die UDP-WS-Ermittlung](using-a-generic-host-and-client-for-udp-ws-discovery.md)und Verwenden des [WSD-Debugclients](using-wsddebug-client-to-verify-multicast-traffic.md)zum Überprüfen des Multicastdatenverkehrs .

## <a name="the-wsd-debug-host"></a>Der WSD-Debughost

Der WSD-Debughost (wsddebughost.exe) stellt eine interaktive Konsole zum Ankündigen des Hosts, zum Reagieren auf Clientanforderungen und zum Drucken von \_ Diagnoseinformationen zur Verfügung.

Der WSD-Debughost arbeitet in einem von zwei Modi: Ermittlung und Metadaten.



| Mode      | BESCHREIBUNG                                                                                                                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ermittlung (Discovery) | Im Ermittlungsmodus gibt der WSD-Debughost formatierte WS-Discovery aus. Außerdem werden [Hello-](hello-message.md) und [Bye-Nachrichten](bye-message.md) gesendet und automatisch auf Test- [und](probe-message.md) [Resolve-Nachrichten](resolve-message.md) reagiert. |
| Metadaten  | Zusätzlich zur Implementierung aller Features des Ermittlungsmodus wird im Metadatenmodus ein Metadatendienst angekündigt, und Clients können eine Verbindung herstellen und Metadaten austauschen.                                                                                       |



 

Weitere Informationen finden Sie unter [Using a Generic Host and Client for HTTP Metadata Exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md) and Using a Generic Host and Client for [UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSD-Anwendungsentwicklung auf Windows](wsd-application-development-on-windows.md)
</dt> <dt>

[WSDAPI-Entwicklungstools](wsdapi-development-tools.md)
</dt> <dt>

[Handbuch zur WSDAPI-Problembehandlung](wsdapi-troubleshooting-guide.md)
</dt> </dl>

 

 



