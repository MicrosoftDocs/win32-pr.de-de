---
description: Erfahren Sie mehr über das Überprüfen von Netzwerkverfolgungen für den HTTP-Metadatenaustausch. Verwenden Sie eine Netzwerkpaketanalyse, die Unformatiertpakete anzeigt.
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 076ead8f6ac0cf78699029189f0d34daaf0e17db3dec33d1a41bedfd0167eb2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118311599"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a>Überprüfen von Netzwerkverfolgungen für HTTP-Metadaten Exchange

Jede Netzwerkpaketanalyse, die Unformatiertpakete anzeigen kann, kann verwendet werden, um HTTP-Metadatenaustauschanforderungen zu überprüfen. Microsoft-Netzwerkmonitor 3 (Netmon) wird empfohlen. Weitere Informationen zu Netmon finden Sie unter [Herunterladen von Netmon- und DPWS-Beispielfiltern.](downloading-netmon-and-sample-dpws-filters.md)

Dieses Diagnoseverfahren ist möglicherweise nicht so nützlich für Clients und Hosts, die einen sicheren Kanal für die Kommunikation verwenden, da der Nachrichteninhalt verschlüsselt ist.

**So überprüfen Sie Netzwerkverfolgungen für den HTTP-Metadatenaustausch**

1.  Konfigurieren Sie den Host und client so, dass sie über das Netzwerk ausgeführt werden (d. h., dass der Host und der Client auf verschiedenen Computern ausgeführt werden).
2.  Installieren Sie die Paketanalyse (Netmon) entweder auf dem Client oder auf dem Host.
3.  Konfigurieren Sie die Paketanalyse, um Datenverkehr auf dem Netzwerkadapter zu erfassen, der den Host und den Client verbindet.
4.  Reproduzieren Sie den Fehler, indem Sie den Host und den Client starten oder im Netzwerk-Explorer F5 drücken.
5.  Filtern Sie die Ergebnisse, um datenverkehrs- WS-Discovery und Metadatenaustausch zu isolieren. Beispiele für Netmon-Filter finden Sie unter [Herunterladen von Netmon- und DPWS-Beispielfiltern.](downloading-netmon-and-sample-dpws-filters.md)
    > [!Note]  
    > Dieser Schritt ist optional.

     

6.  Stellen Sie sicher, dass nachrichten, die zwischen Client und Host gesendet werden, grundlegende Datenverkehrsanforderungen erfüllen.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Überprüfen, ob Nachrichten die Datenverkehrsanforderungen erfüllen

WSDAPI-Clients und -Hosts müssen Nachrichten senden, die den folgenden Kriterien entsprechen. Allgemeine Informationen zu Nachrichtenmustern finden Sie unter [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).

-   Nachrichten müssen die Datenverkehrsanforderungen im Thema [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md)erfüllen, es sei denn, es ist absolut sicher, dass WS-Discovery nicht für den Metadatenaustausch verwendet wird.
-   Zwischen dem Client und der ersten Transportadresse, die im **XAddrs-Element** einer [ProbeMatches-](probematches-message.md) oder [ResolveMatches-Nachricht](resolvematches-message.md) bereitgestellt wird, muss eine TCP-Verbindung hergestellt werden. Die folgende Liste zeigt einen typischen Paketaustausch, der zum Herstellen einer TCP-Verbindung verwendet wird.
    -   Der Client sendet ein TCP SYN-Paket an den Host an einem angegebenen Port.
    -   Der Host sendet ein TCP SYN/ACK-Paket an den Client.
    -   Der Client sendet ein TCP-ACK-Paket an den Host an einem angegebenen Port.

    Nachdem der Client ein TCP-ACK-Paket gesendet hat, wird die TCP-Verbindung hergestellt. Beachten Sie, dass dieser Nachrichtenaustausch nicht erfolgt, wenn zuvor eine TCP-Verbindung hergestellt wurde.
-   Der Client muss eine gültige [HTTP-Get-Anforderung](get--metadata-exchange--http-request-and-message.md) und -Nachricht senden.
-   Der Host muss auf den URL-Pfad lauschen, der in der [GET](get--metadata-exchange--http-request-and-message.md) HTTP-Anforderung angegeben ist.
-   Das **To-Element** einer [Get-Metadatenmeldung](get--metadata-exchange--http-request-and-message.md) muss vorhanden sein und darf nicht leer sein. Der Wert des **To -Elements** muss mit einer der Endpunktadressen des Hosts übereinstimmen. Die Endpunktadresse eines Hosts wird in der Regel in einer [ProbeMatches-](probematches-message.md) oder [ResolveMatches-Nachricht](resolvematches-message.md) angekündigt.
-   Der Host muss einen gültigen HTTP-Antwortheader senden. Wenn die erste Anforderung erfolgreich war, sollte der Antwortheader den Statuscode HTTP/1.1 200 enthalten.
-   Der Host muss eine gültige [GetResponse-Nachricht](getresponse--metadata-exchange--message.md) senden.
-   Das **RelatesTo-Element** einer [GetResponse-Nachricht](getresponse--metadata-exchange--message.md) muss vorhanden sein und darf nicht leer sein. Der Wert muss mit dem Wert des **MessageId-Elements** aus der entsprechenden [Get-Nachricht](get--metadata-exchange--http-request-and-message.md) übereinstimmen.

Wenn die vom Programm gesendeten HTTP-Anforderungen oder Metadatenaustauschnachrichten nicht diesen Datenverkehrsanforderungen entsprechen, wurde die Ursache des Problems erfolgreich identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Schreiben Sie das Programm neu, damit es konforme Nachrichten und Anforderungen generiert und das Programm erneut testet.

Wenn die Ursache des Problems immer noch nicht identifiziert werden kann, wenden Sie sich an den Microsoft-Support, um Unterstützung zu erhalten. Bevor Sie sich an den Support wenden, erfassen Sie die entsprechenden Protokolldateien, um die Grundursache des Problems zu ermitteln. Weitere Informationen finden Sie unter [Aktivieren der WSDAPI-Ablaufverfolgung.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Erste Schritte mit WSDAPI – Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Herunterladen von Netmon- und DPWS-Beispielfiltern](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



