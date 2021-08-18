---
description: Listet die Diagnoseverfahren auf, die bei der Problembehandlung des Projektor-Assistenten verwendet werden sollen.
ms.assetid: 54efc88c-0b8e-4652-8655-817a288863d1
title: Problembehandlung für den Projektor-Assistenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5767e9827174d2d8135ac6dfb96c335d49acb82f0a0162b06f22a89c4dbdebef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856070"
---
# <a name="troubleshooting-the-projector-wizard"></a>Problembehandlung für den Projektor-Assistenten

Der Projektor-Assistent:

-   Verwendet immer UDP-WS-Discovery für die Geräteermittlung.
-   Verwendet immer HTTP für den Metadatenaustausch.
-   Manchmal wird die gerichtete Ermittlung verwendet.

Die folgenden Diagnoseverfahren sollten (in der Reihenfolge) verwendet werden, um Probleme mit dem Projektor-Assistenten zu identifizieren.

**So beheben Sie probleme mit dem Projektor-Assistenten**

1.  Wenn die gerichtete Ermittlung verwendet wird, beheben Sie die Problembehandlung bei [der gerichteten Ermittlung.](troubleshooting-applications-using-directed-discovery.md)
2.  [Überprüfen Sie die Adapter- und Firewalleinstellungen.](inspecting-adapter-and-firewall-settings.md)
3.  [Verwenden Sie einen generischen Host und Client für die UDP-WS-Ermittlung.](using-a-generic-host-and-client-for-udp-ws-discovery.md)
4.  Verwenden Sie den [WSD-Debugclient, um multicast-Datenverkehr zu überprüfen.](using-wsddebug-client-to-verify-multicast-traffic.md)
5.  [Überprüfen Sie Die Netzwerkablaufverfolgungen für die UDP-WS-Ermittlung.](inspecting-network-traces-for-udp-ws-discovery.md)
6.  [Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
7.  [Verwenden Sie die WinHTTP-Protokollierung, um datenverkehr abrufen zu überprüfen.](using-winhttp-logging-to-verify-get-traffic.md)
8.  [Überprüfen Sie Die Netzwerkablaufverfolgungen für den HTTP-Metadatenaustausch.](inspecting-network-traces-for-http-metadata-exchange.md)

Wenn die Ursache des Problems nicht mithilfe der oben genannten Diagnoseverfahren identifiziert werden kann, befolgen Sie die Anweisungen unter Aktivieren der [WSDAPI-Ablaufverfolgung,](enabling-wsdapi-tracing.md) und wenden Sie sich an den Microsoft-Support.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit WSDAPI–Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



