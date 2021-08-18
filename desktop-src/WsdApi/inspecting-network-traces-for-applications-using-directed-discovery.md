---
description: Erfahren Sie mehr über das Untersuchen von Netzwerkverfolgungen mithilfe der direkten Ermittlung. Eine Netzwerkpaketanalyse, die rohe Pakete anzeigt, kann HTTP-Metadatenaustauschanforderungen überprüfen.
ms.assetid: 9b124117-06e7-4637-9863-0f9650861526
title: Untersuchen von Netzwerkverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f8e96778b2d75f511c625073ef1d0bbc30dd4c815a327f42432abd0d221756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991730"
---
# <a name="inspecting-network-traces-for-applications-using-directed-discovery"></a>Untersuchen von Netzwerkverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung

Jede Netzwerkpaketanalyse, die Unformatiertpakete anzeigen kann, kann verwendet werden, um HTTP-Metadatenaustauschanforderungen zu überprüfen. Microsoft-Netzwerkmonitor 3 (Netmon) wird empfohlen. Weitere Informationen zu Netmon finden Sie unter [Herunterladen von Netmon- und DPWS-Beispielfiltern.](downloading-netmon-and-sample-dpws-filters.md)

**So überprüfen Sie Netzwerkverfolgungen auf die gerichtete Ermittlung**

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

-   [Testnachrichten](probe-message.md) müssen über HTTP oder HTTPS gesendet werden, normalerweise an Port 5357 oder 5358.
-   Das **Types-Element** einer [Testmeldung](probe-message.md) muss vorhanden sein und darf nicht leer sein. Sie muss die Typen enthalten, auf die ein Host antwortet.
-   Eine [ProbeMatches-Nachricht](probematches-message.md) muss an den HTTP- oder HTTPS-Port gesendet werden, von dem der [Test](probe-message.md) gesendet wurde.
-   Das **RelatesTo-Element** einer [ProbeMatches-Nachricht](probematches-message.md) muss vorhanden sein und darf nicht leer sein. Der Wert muss mit dem Wert des **MessageId-Elements** aus der entsprechenden [Testnachricht](probe-message.md) übereinstimmen.
-   Wenn ein **XAddrs-Element** in der [ProbeMatches-Nachricht](probematches-message.md) enthalten war, müssen die angegebenen Transportadressen überprüft werden. Weitere Informationen finden Sie unter [XAddr-Validierungsregeln.](xaddr-validation-rules.md)
-   Eine [ProbeMatches-Nachricht](probematches-message.md) muss innerhalb von 4 Sekunden nach der entsprechenden [Testnachricht gesendet](probe-message.md) werden. Die Windows Firewall kann eine ProbeMatches-Nachricht, die mehr als 4 Sekunden nach einer Testnachricht gesendet wurde, verdringen.
-   Wenn kein **XAddrs-Element** in der [ProbeMatches-Nachricht](probematches-message.md) enthalten war und der Client oder Host eine HTTP-Nachricht sendet (z. B. eine [Anforderung](get--metadata-exchange--http-request-and-message.md) zum Abrufen des Metadatenaustauschs oder eine Dienstnachricht), muss der Client oder Host eine [Resolve-Nachricht](resolve-message.md) über HTTP oder HTTPS senden. Diese Nachricht wird normalerweise an Port 5357 oder 5358 gesendet.
-   Wenn eine [Resolve-Nachricht](resolve-message.md) gesendet wird, muss eine [ResolveMatches-Nachricht](resolvematches-message.md) an den HTTP- oder HTTPS-Port gesendet werden, von dem die Resolve-Nachricht gesendet wurde.
-   Eine [ResolveMatches-Nachricht](resolvematches-message.md) muss innerhalb von 4 Sekunden nach der entsprechenden [Resolve-Nachricht gesendet](resolve-message.md) werden. Die Windows Firewall kann eine ResolveMatchesmessage, die mehr als 4 Sekunden nach einer Auflösungsnachricht gesendet wurde, ablegen.

Wenn die vom Programm gesendeten Nachrichten nicht diesen Nachrichtenanforderungen entsprechen, wurde die Ursache des Problems erfolgreich identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Schreiben Sie das Programm neu, damit es konforme Nachrichten generiert und das Programm erneut testet.

Wenn die Ursache des Problems immer noch nicht identifiziert werden kann, wenden Sie sich an den Microsoft-Support, um Unterstützung zu erhalten. Bevor Sie sich an den Support wenden, erfassen Sie die entsprechenden Protokolldateien, um die Grundursache des Problems zu ermitteln. Weitere Informationen finden Sie unter [Aktivieren der WSDAPI-Ablaufverfolgung.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Problembehandlung bei Anwendungen mithilfe der gerichteten Ermittlung](troubleshooting-applications-using-directed-discovery.md)
</dt> <dt>

[WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Erste Schritte mit WSDAPI – Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Herunterladen von Netmon- und DPWS-Beispielfiltern](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



