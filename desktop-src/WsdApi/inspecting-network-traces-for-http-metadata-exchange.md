---
description: Alle Network Packet Analyzer, die unformatierte Pakete anzeigen können, können zum Überprüfen von http-metadatenaustauschanforderungen verwendet werden. Microsoft-Netzwerkmonitor 3 (NetMon) wird empfohlen. Weitere Informationen zu Netmon finden Sie unter Herunterladen von Netmon und Beispiel-DPWS-filtern.
ms.assetid: b3b6c4d1-5fa3-41fb-ae1d-067638e385b0
title: Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9993c542789b7f11eb35344dd6b0b03bfbafc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215429"
---
# <a name="inspecting-network-traces-for-http-metadata-exchange"></a>Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch

Alle Network Packet Analyzer, die unformatierte Pakete anzeigen können, können zum Überprüfen von http-metadatenaustauschanforderungen verwendet werden. Microsoft-Netzwerkmonitor 3 (NetMon) wird empfohlen. Weitere Informationen zu Netmon finden Sie unter [Herunterladen von Netmon und Beispiel-DPWS-Filtern](downloading-netmon-and-sample-dpws-filters.md).

Diese Diagnose Prozedur ist möglicherweise nicht so nützlich für Clients und Hosts, die einen sicheren Kommunikationskanal verwenden, da der Nachrichten Inhalt verschlüsselt ist.

**So überprüfen Sie die Netzwerk Ablauf Verfolgungen für http**

1.  Konfigurieren Sie den Host und den Client für die Netzwerk übergreifende Ausführung (d. h., stellen Sie sicher, dass der Host und der Client auf unterschiedlichen Computern ausgeführt werden).
2.  Installieren Sie Packet Analyzer (NetMon) entweder auf dem Client oder auf dem Host.
3.  Konfigurieren Sie die Paket Analyse für die Erfassung von Datenverkehr auf dem Netzwerkadapter, der den Host und den Client verbindet.
4.  Reproduzieren Sie den Fehler Durchstarten des Hosts und Clients oder durch Drücken von F5 im Netzwerk-Explorer.
5.  Filtern Sie die Ergebnisse, um WS-Discovery-und metadatenaustauschdatenverkehr zu isolieren Beispiel-Netmon-Filter finden Sie unter [Herunterladen von Netmon und Beispiel-DPWS-Filtern](downloading-netmon-and-sample-dpws-filters.md).
    > [!Note]  
    > Dieser Schritt ist optional.

     

6.  Überprüfen Sie, ob Nachrichten, die zwischen Client und Host gesendet werden, grundlegende Anforderungen

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Überprüfen, ob Nachrichten Datenverkehrs Anforderungen erfüllen

WSDAPI-Clients und-Hosts müssen Nachrichten senden, die den folgenden Kriterien entsprechen. Allgemeine Informationen zu Nachrichten Mustern finden Sie unter Ermittlungs [-und Metadatenaustausch-Nachrichten Muster](discovery-and-metadata-exchange-message-patterns.md).

-   Nachrichten müssen die im Thema [Überprüfen von Netzwerk Ablauf Verfolgungen für UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md)bereitgestellten Datenverkehrs Anforderungen erfüllen, es sei denn, es ist absolut sicher, dass WS-Discovery nicht für Metadatenaustausch verwendet wird.
-   Zwischen dem Client und der ersten Transport Adresse, die im **xaddrs** -Element einer [Probe Matches](probematches-message.md) -oder [resolvematches](resolvematches-message.md) -Nachricht angegeben ist, muss eine TCP-Verbindung hergestellt werden. Die folgende Liste zeigt einen typischen Paket Austausch, der zum Herstellen einer TCP-Verbindung verwendet wird.
    -   Der Client sendet ein TCP-SYN-Paket an den Host an einem angegebenen Port.
    -   Der Host sendet ein TCP-SYN/ACK-Paket an den Client.
    -   Der Client sendet ein TCP-ACK-Paket an den Host an einem angegebenen Port.

    Nachdem der Client ein TCP-ACK-Paket gesendet hat, wird die TCP-Verbindung hergestellt. Beachten Sie, dass dieser Nachrichtenaustausch nicht stattfindet, wenn zuvor eine TCP-Verbindung hergestellt wurde.
-   Der Client muss eine gültige [Get](get--metadata-exchange--http-request-and-message.md) http-Anforderung und-Nachricht senden.
-   Der Host muss den URL-Pfad lauschen, der in der [Get](get--metadata-exchange--http-request-and-message.md) http-Anforderung angegeben ist.
-   Das **to** -Element einer [Get](get--metadata-exchange--http-request-and-message.md) -metadatennachricht muss vorhanden und nicht leer sein. Der Wert des **to** -Elements muss mit einer der Endpunkt Adressen des Hosts identisch sein. Die Endpunkt Adresse eines Hosts wird in der Regel in einer [Probe Matches](probematches-message.md) -oder [resolvematches](resolvematches-message.md) -Nachricht angekündigt.
-   Der Host muss einen gültigen HTTP-Antwortheader senden. Wenn die anfängliche Anforderung erfolgreich war, sollte der Antwortheader den Statuscode HTTP/1.1 200 enthalten.
-   Der Host muss eine gültige [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht senden.
-   Das **RelatesTo** -Element einer [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht muss vorhanden sein und darf nicht leer sein. Der Wert muss mit dem Wert des **MessageId** -Elements aus der entsprechenden [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht übereinstimmen.

Wenn die vom Programm gesendeten HTTP-Anforderungen oder Metadatenaustausch-Nachrichten diesen Datenverkehrs Anforderungen nicht entsprechen, wurde die Ursache des Problems erfolgreich identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Schreiben Sie das Programm so um, dass konforme Nachrichten und Anforderungen generiert werden, und testen Sie das Programm erneut.

Wenn die Ursache des Problems weiterhin nicht identifiziert werden kann, wenden Sie sich an den Microsoft Support, um Hilfe zu erhalten. Bevor Sie sich an den Support wenden, erfassen Sie die entsprechenden Protokolldateien, um die Ursache des Problems zu identifizieren. Weitere Informationen finden Sie unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md)-Ablauf Verfolgung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnose Prozeduren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Herunterladen von Netmon und Beispiel-DPWS-Filtern](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



