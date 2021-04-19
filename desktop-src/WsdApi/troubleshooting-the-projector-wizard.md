---
description: Listet die Diagnose Prozeduren auf, die bei der Problembehandlung für den Projektor-Assistenten
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Problembehandlung beim Projektor-Assistenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3776e86d3a156fa86873900aa9e804df9830ec64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360033"
---
# <a name="troubleshooting-the-projector-wizard"></a>Problembehandlung beim Projektor-Assistenten

Der Projektor-Assistent:

-   Verwendet für die Geräte Ermittlung immer UDP-WS-Discovery
-   Verwendet immer http für Metadatenaustausch
-   Verwendet manchmal die gesteuerte Ermittlung

Die folgenden Diagnose Prozeduren sollten (in der richtigen Reihenfolge) verwendet werden, um Probleme mit dem Projektor-Assistenten zu identifizieren.

**So beheben Sie Probleme mit dem Projektor-Assistenten**

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

 

 



