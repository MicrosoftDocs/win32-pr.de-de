---
description: Jede Netzwerkpaketanalyse, die Unformatiertpakete anzeigen kann, kann verwendet werden, um UDP-WS-Discovery zu überprüfen. Microsoft-Netzwerkmonitor 3 (Netmon) wird empfohlen. Weitere Informationen zu Netmon finden Sie unter Herunterladen von Netmon- und DPWS-Beispielfiltern.
ms.assetid: f12f9847-b87f-4d5f-bee3-4d219f9ad898
title: Überprüfen von Netzwerkverfolgungen für UDP-WS-Discovery
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce21e2943a37640eb091aa03c02eba0886164166b2959e31e897ee788424cd41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920754"
---
# <a name="inspecting-network-traces-for-udp-ws-discovery"></a>Überprüfen von Netzwerkverfolgungen für UDP-WS-Discovery

Jede Netzwerkpaketanalyse, die Unformatiertpakete anzeigen kann, kann verwendet werden, um UDP-WS-Discovery zu überprüfen. Microsoft-Netzwerkmonitor 3 (Netmon) wird empfohlen. Weitere Informationen zu Netmon finden Sie unter [Herunterladen von Netmon- und DPWS-Beispielfiltern.](downloading-netmon-and-sample-dpws-filters.md)

**So überprüfen Sie Netzwerkverfolgungen für die UDP-WS-Ermittlung**

1.  Konfigurieren Sie den Host und client so, dass sie über das Netzwerk ausgeführt werden (d. h., dass der Host und der Client auf verschiedenen Computern ausgeführt werden).
2.  Installieren Sie die Paketanalyse (Netmon) entweder auf dem Client oder auf dem Host.
3.  Konfigurieren Sie die Paketanalyse, um Datenverkehr auf dem Netzwerkadapter zu erfassen, der den Host und den Client verbindet.
4.  Reproduzieren Sie den Fehler, indem Sie den Host und den Client starten oder im Netzwerk-Explorer F5 drücken.
5.  Filtern Sie die Ergebnisse, um WS-Discovery zu isolieren. Beispiele für Netmon-Filter finden Sie unter [Herunterladen von Netmon- und DPWS-Beispielfiltern.](downloading-netmon-and-sample-dpws-filters.md)
    > [!Note]  
    > Dieser Schritt ist optional.

     

6.  Stellen Sie sicher, dass nachrichten, die zwischen Client und Host gesendet werden, grundlegende Datenverkehrsanforderungen erfüllen.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Überprüfen, ob Nachrichten die Datenverkehrsanforderungen erfüllen

WSDAPI-Clients und -Hosts müssen Nachrichten senden, die den folgenden Kriterien entsprechen. Allgemeine Informationen zu Nachrichtenmustern finden Sie unter [Discovery and Metadata Exchange Message Patterns](discovery-and-metadata-exchange-message-patterns.md).

-   [Testnachrichten](probe-message.md) müssen per UDP-Multicast an Port 3702 gesendet werden.
-   Das **Types-Element** einer [Testmeldung](probe-message.md) muss vorhanden sein und darf nicht leer sein. Sie muss die Typen enthalten, auf die ein Host antwortet.
-   Eine [ProbeMatches-Nachricht](probematches-message.md) muss unicast an den UDP-Port gesendet werden, von dem der [Test](probe-message.md) gesendet wurde.
-   Das **RelatesTo-Element** einer [ProbeMatches-Nachricht](probematches-message.md) muss vorhanden sein und darf nicht leer sein. Der Wert muss mit dem Wert des **MessageId-Elements** aus der entsprechenden [Testnachricht](probe-message.md) übereinstimmen.
-   Wenn ein **XAddrs-Element** in der [ProbeMatches-Nachricht](probematches-message.md) enthalten war, müssen die angegebenen Transportadressen überprüft werden. Weitere Informationen finden Sie unter [XAddr-Validierungsregeln.](xaddr-validation-rules.md)
-   Eine [ProbeMatches-Nachricht](probematches-message.md) muss innerhalb von 4 Sekunden nach der entsprechenden [Testnachricht gesendet](probe-message.md) werden. Die Windows Firewall kann eine ProbeMatches-Nachricht, die mehr als 4 Sekunden nach einer Testnachricht gesendet wurde, verdringen.
-   Wenn kein **XAddrs-Element** in der [ProbeMatches-Nachricht](probematches-message.md) enthalten war und der Client oder Host eine HTTP-Nachricht sendet (z. B. eine [Anforderung](get--metadata-exchange--http-request-and-message.md) zum Abrufen des Metadatenaustauschs oder eine Dienstnachricht), muss der Client oder Host eine [Resolve-Nachricht](resolve-message.md) per UDP-Multicast an Port 3702 senden.
-   Wenn eine [Resolve-Nachricht](resolve-message.md) gesendet wird, muss eine [ResolveMatches-Nachricht](resolvematches-message.md) unicast an den UDP-Port gesendet werden, von dem die Resolve-Nachricht gesendet wurde.
-   Eine [ResolveMatches-Nachricht](resolvematches-message.md) muss innerhalb von 4 Sekunden nach der entsprechenden [Resolve-Nachricht gesendet](resolve-message.md) werden. Die Windows Firewall kann eine ResolveMatchesmessage, die mehr als 4 Sekunden nach einer Auflösungsnachricht gesendet wurde, ablegen.

Wenn die vom Programm gesendeten Nachrichten nicht diesen Nachrichtenanforderungen entsprechen, wurde die Ursache des Problems erfolgreich identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Schreiben Sie das Programm neu, damit es konforme Nachrichten generiert und das Programm erneut testet.

Wenn die Ursache des Problems immer noch nicht identifiziert werden kann, wenden Sie sich an den Microsoft-Support, um Unterstützung zu erhalten. Bevor Sie sich an den Support wenden, erfassen Sie die entsprechenden Protokolldateien, um die Grundursache des Problems zu ermitteln. Weitere Informationen finden Sie unter [Aktivieren der WSDAPI-Ablaufverfolgung.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Erste Schritte mit WSDAPI – Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Herunterladen von Netmon- und DPWS-Beispielfiltern](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



