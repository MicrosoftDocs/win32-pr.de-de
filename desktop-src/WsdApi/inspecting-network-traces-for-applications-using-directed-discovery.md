---
description: Alle Network Packet Analyzer, die unformatierte Pakete anzeigen können, können zum Überprüfen von http-metadatenaustauschanforderungen verwendet werden. Microsoft-Netzwerkmonitor 3 (NetMon) wird empfohlen. Weitere Informationen zu Netmon finden Sie unter Herunterladen von Netmon und Beispiel-DPWS-filtern.
ms.assetid: 9b124117-06e7-4637-9863-0f9650861526
title: Überprüfen von Netzwerk Ablauf Verfolgungen für Anwendungen, die die gesteuerte Ermittlung verwenden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a424117896c18a5fcf84c883ba824b8223ef01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350123"
---
# <a name="inspecting-network-traces-for-applications-using-directed-discovery"></a>Überprüfen von Netzwerk Ablauf Verfolgungen für Anwendungen, die die gesteuerte Ermittlung verwenden

Alle Network Packet Analyzer, die unformatierte Pakete anzeigen können, können zum Überprüfen von http-metadatenaustauschanforderungen verwendet werden. Microsoft-Netzwerkmonitor 3 (NetMon) wird empfohlen. Weitere Informationen zu Netmon finden Sie unter [Herunterladen von Netmon und Beispiel-DPWS-Filtern](downloading-netmon-and-sample-dpws-filters.md).

**So überprüfen Sie die Netzwerk Ablauf Verfolgungen für die gesteuerte Ermittlung**

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

-   Test [Nachrichten müssen](probe-message.md) von http oder HTTPS gesendet werden, in der Regel an Port 5357 oder 5358.
-   Das **types** -Element einer [Testnachricht muss](probe-message.md) vorhanden sein und darf nicht leer sein. Sie muss die Typen enthalten, auf die ein Host antwortet.
-   Eine [Probe Matches](probematches-message.md) -Nachricht muss an den HTTP-oder HTTPS-Port gesendet werden, von dem aus der Test [gesendet wurde.](probe-message.md)
-   Das **RelatesTo** -Element einer [Probe Matches](probematches-message.md) -Nachricht muss vorhanden sein und darf nicht leer sein. Der Wert muss mit dem Wert des **MessageId** -Elements aus [der entsprechenden Test](probe-message.md) Nachricht übereinstimmen.
-   Wenn ein **xaddrs** -Element in der [probematches](probematches-message.md) -Nachricht enthalten war, müssen die angegebenen Transport Adressen überprüft werden. Weitere Informationen finden Sie unter [xaddr-Validierungsregeln](xaddr-validation-rules.md).
-   Eine [Probe Matches](probematches-message.md) -Nachricht muss innerhalb von 4 Sekunden [der entsprechenden Test](probe-message.md) Nachricht gesendet werden. Die Windows-Firewall kann eine Probe Matches-Nachricht löschen, die nach einer Testnachricht mehr als 4 Sekunden gesendet wurde.
-   Wenn in der [probematches](probematches-message.md) -Nachricht kein **xaddrs** -Element enthalten ist und der Client bzw. der Host eine HTTP-Nachricht (z. b. eine [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange-Anforderung oder eine Dienst Nachricht) sendet, muss der Client oder der Host eine [Auflösungs](resolve-message.md) Nachricht über HTTP oder HTTPS senden. Diese Meldung wird normalerweise an den Port 5357 oder 5358 gesendet.
-   Wenn eine [Resolve](resolve-message.md) -Nachricht gesendet wird, muss eine [resolvematches](resolvematches-message.md) -Nachricht an den HTTP-oder HTTPS-Port gesendet werden, von dem die Auflösungs Nachricht gesendet wurde.
-   Eine [resolvematches](resolvematches-message.md) -Nachricht muss innerhalb von 4 Sekunden der entsprechenden [Auflösungs](resolve-message.md) Nachricht gesendet werden. Die Windows-Firewall löscht möglicherweise eine resolvematchesmessage, die mehr als 4 Sekunden nach einer Auflösungs Meldung gesendet wird.

Wenn die vom Programm gesendeten Nachrichten den Nachrichten Anforderungen nicht entsprechen, wurde die Ursache des Problems erfolgreich identifiziert, und es sind keine weiteren Schritte zur Problembehandlung erforderlich. Schreiben Sie das Programm so um, dass konforme Nachrichten generiert werden, und testen Sie das Programm erneut.

Wenn die Ursache des Problems weiterhin nicht identifiziert werden kann, wenden Sie sich an den Microsoft Support, um Hilfe zu erhalten. Bevor Sie sich an den Support wenden, erfassen Sie die entsprechenden Protokolldateien, um die Ursache des Problems zu identifizieren. Weitere Informationen finden Sie unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md)-Ablauf Verfolgung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Problembehandlung bei Anwendungen mithilfe der gesteuerten Ermittlung](troubleshooting-applications-using-directed-discovery.md)
</dt> <dt>

[WSDAPI-Diagnose Prozeduren](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Herunterladen von Netmon und Beispiel-DPWS-Filtern](downloading-netmon-and-sample-dpws-filters.md)
</dt> </dl>

 

 



