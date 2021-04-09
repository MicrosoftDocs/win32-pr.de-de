---
description: Listet die Diagnose Prozeduren auf, die bei der Problembehandlung von Funktions Ermittlungs Clients verwendet
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Problembehandlung bei Funktions Ermittlungs Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753665"
---
# <a name="troubleshooting-function-discovery-clients"></a>Problembehandlung bei Funktions Ermittlungs Clients

Funktions Ermittlungs Clients:

-   Verwenden Sie für die Geräte Ermittlung stets UDP-WS-Discovery.
-   HTTP-oder HTTPS-Verbindungen für Metadatenaustausch immer initiieren
-   Manchmal gesteuerte Ermittlung verwenden
-   Verwenden Sie manchmal einen sicheren Kanal (HTTPS) für den Metadatenaustausch.

In der folgenden Liste wird die typische Abfolge von Nachrichten angezeigt, die von Funktions Ermittlungs Clients gesendet und empfangen werden. Nicht alle Nachrichten sind obligatorisch.

1.  Vom Client [wird eine Testnachricht gesendet,](probe-message.md) um Geräte und Dienste zu ermitteln. Wenn der Client die gesteuerte Ermittlung verwendet, wird diese Nachricht über HTTP oder HTTPS gesendet. Andernfalls wird die Nachricht von UDP-Multicast an Port 3702 gesendet.
2.  Der Client empfängt [Probe Matches](probematches-message.md) -Nachrichten von übereinstimmenden Geräten oder Diensten. Gesteuerte Ermittlungs Meldungen werden über HTTP oder HTTPS gesendet. Andernfalls werden diese Nachrichten von UDP-Unicast gesendet und stammen von Port 3702.
3.  Wenn keine xaddrs in der probematches-Nachricht enthalten sind, sendet der Client eine [Auflösungs](resolve-message.md) Meldung von UDP-Multicast an Port 3702.
4.  Wenn eine [Resolve](resolve-message.md) -Nachricht gesendet wurde, empfängt der Client eine [resolvematches](resolvematches-message.md) -Nachricht von übereinstimmenden Diensten. Diese Meldung wird von UDP-Unicast von Port 3702 an den Port gesendet, von dem die Auflösungs Nachricht stammt.
5.  Der Client sendet eine [Get](get--metadata-exchange--http-request-and-message.md) -Nachricht, um Metadaten vom Gerät oder Dienst anzufordern. Diese Meldung wird von http oder HTTPS gesendet.
6.  Der Client empfängt eine [GetResponse](getresponse--metadata-exchange--message.md) -Nachricht mit dem Gerät oder den Dienst Metadaten. Diese Meldung wird von http oder HTTPS gesendet.

Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit einem funktionermittlungs Client zu identifizieren.

**So beheben Sie Probleme mit einem Funktions Ermittlungs Client**

1.  Wenn die gesteuerte Ermittlung verwendet wird, beheben Sie die Fehler bei der [gesteuerten](troubleshooting-applications-using-directed-discovery.md)Ermittlung.
2.  Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).
3.  [Verwenden Sie einen generischen Host und Client für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
4.  [Überprüfen Sie Multicast Datenverkehr mithilfe des WSD-Debugclients](using-wsddebug-client-to-verify-multicast-traffic.md).
5.  [Überprüfen Sie die Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
6.  [Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).
7.  [Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).
8.  [Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)

Wenn die Ursache des Problems nicht mithilfe der obigen Diagnose Prozeduren identifiziert werden kann, befolgen Sie die Anweisungen unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md) -Ablauf Verfolgung und wenden Sie sich an den Microsoft Support.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



