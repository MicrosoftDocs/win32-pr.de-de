---
description: Erfahren Sie mehr über das Überprüfen von Netzwerkablaufverfolgungen mithilfe der direkten Ermittlung. Eine Netzwerkpaketanalyse, die unformatierte Pakete anzeigt, kann HTTP-Metadatenaustauschanforderungen überprüfen.
ms.assetid: 9b124117-06e7-4637-9863-0f9650861526
title: Überprüfen von Netzwerkablaufverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d94ea3bc102c57c415be518883296e049490ca
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262122"
---
# <a name="inspecting-network-traces-for-applications-using-directed-discovery"></a>Überprüfen von Netzwerkablaufverfolgungen für Anwendungen mithilfe der gerichteten Ermittlung

Alle Netzwerkpaketanalysetools, die unformatierte Pakete anzeigen können, können verwendet werden, um HTTP-Metadatenaustauschanforderungen zu überprüfen. Microsoft-Netzwerkmonitor 3 (Netmon) wird empfohlen. Weitere Informationen zu Netmon finden Sie unter [Herunterladen von Netmon und DPWS-Beispielfiltern.](downloading-netmon-and-sample-dpws-filters.md)

**So überprüfen Sie Netzwerkablaufverfolgungen für die gerichtete Ermittlung**

1.  Konfigurieren Sie den Host und den Client so, dass sie über das Netzwerk ausgeführt werden .(Stellen Sie also sicher, dass der Host und der Client auf verschiedenen Computern ausgeführt werden.)
2.  Installieren Sie die Paketanalyse (Netmon) entweder auf dem Client oder auf dem Host.
3.  Konfigurieren Sie die Paketanalyse, um Datenverkehr auf dem Netzwerkadapter zu erfassen, der den Host und den Client verbindet.
4.  Reproduzieren Sie den Fehler, indem Sie host und client starten oder F5 im Netzwerk-Explorer drücken.
5.  Filtern Sie die Ergebnisse, um WS-Discovery- und Metadatenaustauschdatenverkehr zu isolieren. Informationen zum Anzeigen von Netmon-Beispielfiltern finden Sie unter [Herunterladen von Netmon- und DPWS-Beispielfiltern.](downloading-netmon-and-sample-dpws-filters.md)
    > [!Note]  
    > Dieser Schritt ist optional.

     

6.  Vergewissern Sie sich, dass zwischen Client und Host gesendete Nachrichten die grundlegenden Datenverkehrsanforderungen erfüllen.

## <a name="verifying-that-messages-meet-traffic-requirements"></a>Überprüfen, ob Nachrichten die Datenverkehrsanforderungen erfüllen

WSDAPI-Clients und -Hosts müssen Nachrichten senden, die den folgenden Kriterien entsprechen. Allgemeine Informationen zu Nachrichtenmustern finden Sie unter [Ermittlungs- und Metadatenaustausch-Nachrichtenmuster.](discovery-and-metadata-exchange-message-patterns.md)

-   [Testnachrichten](probe-message.md) müssen über HTTP oder HTTPS gesendet werden, normalerweise an Port 5357 oder 5358.
-   Das **Types-Element** einer [Probe-Nachricht](probe-message.md) muss vorhanden sein und darf nicht leer sein. Sie muss die Typen enthalten, auf die ein Host antwortet.
-   Eine [ProbeMatches-Nachricht](probematches-message.md) muss an den HTTP- oder HTTPS-Port gesendet werden, von dem der [Test](probe-message.md) gesendet wurde.
-   Das **RelatesTo-Element** einer [ProbeMatches-Nachricht](probematches-message.md) muss vorhanden sein und darf nicht leer sein. Der Wert muss mit dem Wert des **MessageId-Elements** aus der entsprechenden [Probe-Nachricht](probe-message.md) übereinstimmen.
-   Wenn ein **XAddrs-Element** in der [ProbeMatches-Nachricht](probematches-message.md) enthalten war, müssen die angegebenen Transportadressen überprüft werden. Weitere Informationen finden Sie unter [XAddr-Validierungsregeln.](xaddr-validation-rules.md)
-   Eine [ProbeMatches-Nachricht](probematches-message.md) muss innerhalb von 4 Sekunden nach der entsprechenden [Testnachricht](probe-message.md) gesendet werden. Die Windows-Firewall kann eine ProbeMatches-Nachricht löschen, die mehr als 4 Sekunden nach einer Testmeldung gesendet wurde.
-   Wenn kein **XAddrs-Element** in der [ProbeMatches-Nachricht](probematches-message.md) enthalten war und der Client oder Host eine HTTP-Nachricht sendet (z. B. eine [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange-Anforderung oder eine Dienstnachricht), muss der Client oder Host eine [Resolve-Nachricht](resolve-message.md) per HTTP oder HTTPS senden. Diese Nachricht wird normalerweise an Port 5357 oder 5358 gesendet.
-   Wenn eine [Resolve-Nachricht](resolve-message.md) gesendet wird, muss eine [ResolveMatches-Nachricht](resolvematches-message.md) an den HTTP- oder HTTPS-Port gesendet werden, von dem die Resolve-Nachricht gesendet wurde.
-   Eine [ResolveMatches-Nachricht](resolvematches-message.md) muss innerhalb von 4 Sekunden nach der entsprechenden [Resolve-Nachricht](resolve-message.md) gesendet werden. Die Windows-Firewall kann eine ResolveMatches-Nachricht löschen, die mehr als 4 Sekunden nach einer Resolve-Nachricht gesendet wurde.

Wenn die vom Programm gesendeten Nachrichten diesen Nachrichtenanforderungen nicht entsprechen, wurde die Ursache des Problems erfolgreich identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Schreiben Sie das Programm so um, dass es konforme Nachrichten generiert, und testen Sie das Programm erneut.

Wenn die Ursache des Problems weiterhin nicht identifiziert werden kann, wenden Sie sich an den Microsoft-Support, um Unterstützung zu erhalten. Bevor Sie sich an den Support wenden, sammeln Sie die entsprechenden Protokolldateien, um die Grundursache des Problems zu ermitteln. Weitere Informationen finden Sie unter [Aktivieren der WSDAPI-Ablaufverfolgung.](enabling-wsdapi-tracing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Problembehandlung bei Anwendungen mithilfe der gerichteten Ermittlung](troubleshooting-applications-using-directed-discovery.md)
</dt> <dt>

[WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Erste Schritte mit WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Herunterladen von Netmon- und DPWS-Beispielfiltern](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



