---
description: Listet die bei der Problembehandlung für den Netzwerk-Explorer zu verwendenden Diagnoseverfahren auf.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Problembehandlung für den Netzwerk-Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09afe7acbcb20d706c8645d84c68014b0e33d799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958919"
---
# <a name="troubleshooting-the-network-explorer"></a>Problembehandlung für den Netzwerk-Explorer

Der Netzwerk-Explorer:

-   Verwendet für die Geräte Ermittlung immer UDP-WS-Discovery
-   Initiiert immer eine HTTP-oder HTTPS-Verbindung für den Metadatenaustausch.
-   Verwendet manchmal einen sicheren Kanal (HTTPS) für den Metadatenaustausch

Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit dem Netzwerk-Explorer zu identifizieren.

**So beheben Sie Probleme mit dem Netzwerk-Explorer**

1.  Über [Prüfen der Adapter-und Firewalleinstellungen](inspecting-adapter-and-firewall-settings.md).
2.  [Verwenden Sie einen generischen Host und Client für UDP-WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Überprüfen Sie Multicast Datenverkehr mithilfe des WSD-Debugclients](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Überprüfen Sie die Netzwerk Ablauf Verfolgungen für UDP-WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Überprüfen Sie den Datenverkehr mithilfe der WinHTTP-Protokollierung](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Überprüfen von Netzwerk Ablauf Verfolgungen für http-Metadatenaustausch](inspecting-network-traces-for-http-metadata-exchange.md)

Der Netzwerk-Explorer verwendet die [Funktions](/previous-versions/windows/desktop/fundisc/fd-portal) Ermittlung zum Auflisten von Netzwerkgeräten. Weitere Informationen zur Problembehandlung finden Sie unter Problembehandlung bei [Funktions Ermittlungs Clients](troubleshooting-function-discovery-clients.md).

Wenn die Ursache des Problems nicht mithilfe der obigen Diagnose Prozeduren identifiziert werden kann, befolgen Sie die Anweisungen unter [Aktivieren der WSDAPI](enabling-wsdapi-tracing.md) -Ablauf Verfolgung und wenden Sie sich an den Microsoft Support.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Problembehandlung bei Funktions Ermittlungs Clients](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
