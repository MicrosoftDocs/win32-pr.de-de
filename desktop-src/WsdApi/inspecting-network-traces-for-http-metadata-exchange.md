---
description: Erfahren Sie mehr über das Überprüfen von Netzwerkablaufverfolgungen für den HTTP-Metadatenaustausch. Verwenden Sie eine Netzwerkpaketanalyse, die unformatierte Pakete anzeigt.
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: Überprüfen von Netzwerkablaufverfolgungen für DEN HTTP-Metadatenaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e653b0852f84382873973cd63fbd3223a245dd4
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262682"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a>Überprüfen von Netzwerkablaufverfolgungen für DEN HTTP-Metadatenaustausch

Alle Netzwerkpaketanalysetools, die unformatierte Pakete anzeigen können, können verwendet werden, um HTTP-Metadatenaustauschanforderungen zu überprüfen. Microsoft-Netzwerkmonitor 3 (Netmon) wird empfohlen. Weitere Informationen zu Netmon finden Sie unter [Herunterladen von Netmon und DPWS-Beispielfiltern.](downloading-netmon-and-sample-dpws-filters.md)

Dieses Diagnoseverfahren ist möglicherweise nicht so nützlich für Clients und Hosts, die einen sicheren Kanal für die Kommunikation verwenden, da der Nachrichteninhalt verschlüsselt ist.

**So überprüfen Sie Netzwerkablaufverfolgungen für den HTTP-Metadatenaustausch**

1.  Konfigurieren Sie host und client so, dass sie über das Netzwerk ausgeführt werden (stellen Sie also sicher, dass der Host und der Client auf verschiedenen Computern ausgeführt werden).
2.  Installieren Sie die Paketanalyse (Netmon) entweder auf dem Client oder auf dem Host.
3.  Konfigurieren Sie die Paketanalyse, um Datenverkehr auf dem Netzwerkadapter zu erfassen, der den Host und den Client verbindet.
4.  Reproduzieren Sie den Fehler, indem Sie host und client starten oder F5 im Netzwerk-Explorer drücken.
5.  Filtern Sie die Ergebnisse, um WS-Discovery- und Metadatenaustauschdatenverkehr zu isolieren. Informationen zum Anzeigen von Netmon-Beispielfiltern finden Sie unter [Herunterladen von Netmon- und DPWS-Beispielfiltern.](downloading-netmon-and-sample-dpws-filters.md)
    > [!Note]  
    > Dieser Schritt ist optional.

     

6.  Vergewissern Sie sich, dass zwischen Client und Host gesendete Nachrichten die grundlegenden Datenverkehrsanforderungen erfüllen.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Überprüfen, ob Nachrichten die Datenverkehrsanforderungen erfüllen

WSDAPI-Clients und -Hosts müssen Nachrichten senden, die den folgenden Kriterien entsprechen. Allgemeine Informationen zu Nachrichtenmustern finden Sie unter [Ermittlungs- und Metadatenaustausch-Nachrichtenmuster.](discovery-and-metadata-exchange-message-patterns.md)

-   Nachrichten müssen die Datenverkehrsanforderungen erfüllen, die im Thema [Überprüfen von Netzwerkablaufverfolgungen für die UDP-WS-Ermittlung](inspecting-network-traces-for-udp-ws-discovery.md)bereitgestellt werden, es sei denn, es ist absolut sicher, dass WS-Discovery nicht für den Metadatenaustausch verwendet wird.
-   Zwischen dem Client und der ersten Transportadresse, die im **XAddrs-Element** einer [ProbeMatches-](probematches-message.md) oder [ResolveMatches-Nachricht](resolvematches-message.md) bereitgestellt wird, muss eine TCP-Verbindung hergestellt werden. Die folgende Liste zeigt einen typischen Paketaustausch, der zum Herstellen einer TCP-Verbindung verwendet wird.
    -   Der Client sendet ein TCP SYN-Paket an den Host an einem angegebenen Port.
    -   Der Host sendet ein TCP SYN/ACK-Paket an den Client.
    -   Der Client sendet ein TCP-ACK-Paket an den Host an einem angegebenen Port.

    Nachdem der Client ein TCP-ACK-Paket gesendet hat, wird die TCP-Verbindung hergestellt. Beachten Sie, dass dieser Nachrichtenaustausch nicht stattfindet, wenn zuvor eine TCP-Verbindung hergestellt wurde.
-   Der Client muss eine gültige [Get](get--metadata-exchange--http-request-and-message.md) HTTP-Anforderung und -Nachricht senden.
-   Der Host muss auf den URL-Pfad lauschen, der in der GET-HTTP-Anforderung angegeben ist. [](get--metadata-exchange--http-request-and-message.md)
-   Das **To-Element** einer [Get](get--metadata-exchange--http-request-and-message.md) Metadata-Nachricht muss vorhanden und nicht leer sein. Der Wert des **To-Elements** muss mit einer der Endpunktadressen des Hosts übereinstimmen. Die Endpunktadresse eines Hosts wird in der Regel in einer [ProbeMatches-](probematches-message.md) oder [ResolveMatches-Nachricht](resolvematches-message.md) angekündigt.
-   Der Host muss einen gültigen HTTP-Antwortheader senden. Wenn die erste Anforderung erfolgreich war, sollte der Antwortheader den HTTP/1.1 200-Statuscode enthalten.
-   Der Host muss eine gültige [GetResponse-Nachricht](getresponse--metadata-exchange--message.md) senden.
-   Das **RelatesTo-Element** einer [GetResponse-Nachricht](getresponse--metadata-exchange--message.md) muss vorhanden sein und darf nicht leer sein. Der Wert muss mit dem Wert des **MessageId-Elements** aus der entsprechenden [Get-Nachricht](get--metadata-exchange--http-request-and-message.md) übereinstimmen.

Wenn die vom Programm gesendeten HTTP-Anforderungen oder Metadatenaustauschnachrichten diesen Datenverkehrsanforderungen nicht entsprechen, wurde die Ursache des Problems erfolgreich identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Schreiben Sie das Programm so um, dass es konforme Nachrichten und Anforderungen generiert, und testen Sie das Programm erneut.

Wenn die Ursache des Problems weiterhin nicht identifiziert werden kann, wenden Sie sich an den Microsoft-Support, um Unterstützung zu erhalten. Bevor Sie sich an den Support wenden, sammeln Sie die entsprechenden Protokolldateien, um die Grundursache des Problems zu ermitteln. Weitere Informationen finden Sie unter [Aktivieren der WSDAPI-Ablaufverfolgung.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Erste Schritte mit WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Herunterladen von Netmon- und DPWS-Beispielfiltern](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



