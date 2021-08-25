---
description: Listet die Diagnoseverfahren auf, die bei der Problembehandlung des Assistenten zum Hinzufügen von Druckern verwendet werden sollen.
ms.assetid: 3ffee09b-e980-4a14-97ad-270444457dd7
title: Problembehandlung beim Assistenten zum Hinzufügen von Druckern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6c6971108b0f6fb46a373be47943a3ccbc7fcd97b830733c139653f991debd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860050"
---
# <a name="troubleshooting-the-add-printer-wizard"></a>Problembehandlung beim Assistenten zum Hinzufügen von Druckern

Der Assistent zum Hinzufügen von Druckern:

-   Verwendet immer UDP-WS-Discovery für die Geräteermittlung.
-   Initiiert immer eine HTTP- oder HTTPS-Verbindung für den Metadatenaustausch.
-   Manchmal wird die gerichtete Ermittlung verwendet.
-   Manchmal wird ein sicherer Kanal (HTTPS) für den Metadatenaustausch verwendet.

Die folgenden Diagnoseverfahren sollten (in der Reihenfolge) verwendet werden, um Probleme mit dem Assistenten zum Hinzufügen von Druckern zu identifizieren.

**So beheben Sie probleme mit dem Assistenten zum Hinzufügen von Druckern**

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
</dt> <dt>

[Problembehandlung bei Anwendungen mithilfe der gerichteten Ermittlung](troubleshooting-applications-using-directed-discovery.md)
</dt> </dl>

 

 



