---
description: Listet die Diagnoseverfahren auf, die bei der Problembehandlung des Netzwerk-Explorers verwendet werden sollen.
ms.assetid: 56052a82-d3a6-4749-9010-6796558dcb17
title: Problembehandlung für den Netzwerk-Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a7c8e270fa3f1e07ce9b44fb9ce619d9fe5225e2c4d3ae87896d5e7cf20a2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120580"
---
# <a name="troubleshooting-the-network-explorer"></a>Problembehandlung für den Netzwerk-Explorer

Netzwerk-Explorer:

-   Verwendet immer UDP-WS-Discovery für die Geräteermittlung.
-   Initiiert immer eine HTTP- oder HTTPS-Verbindung für den Metadatenaustausch.
-   Manchmal wird ein sicherer Kanal (HTTPS) für den Metadatenaustausch verwendet.

Die folgenden Diagnoseverfahren sollten (in der Reihenfolge) verwendet werden, um Probleme mit dem Netzwerk-Explorer zu identifizieren.

**So beheben Sie probleme mit dem Netzwerk-Explorer**

1.  [Überprüfen Sie die Adapter- und Firewalleinstellungen.](inspecting-adapter-and-firewall-settings.md)
2.  [Verwenden Sie einen generischen Host und Client für die UDP-WS-Ermittlung.](using-a-generic-host-and-client-for-udp-ws-discovery.md)
3.  Verwenden Sie den [WSD-Debugclient, um multicast-Datenverkehr zu überprüfen.](using-wsddebug-client-to-verify-multicast-traffic.md)
4.  [Überprüfen Sie Die Netzwerkablaufverfolgungen für die UDP-WS-Ermittlung.](inspecting-network-traces-for-udp-ws-discovery.md)
5.  [Verwenden Sie einen generischen Host und Client für den HTTP-Metadatenaustausch.](using-a-generic-host-and-client-for-http-metadata-exchange.md)
6.  [Verwenden Sie die WinHTTP-Protokollierung, um datenverkehr abrufen zu überprüfen.](using-winhttp-logging-to-verify-get-traffic.md)
7.  [Überprüfen Sie Die Netzwerkablaufverfolgungen für den HTTP-Metadatenaustausch.](inspecting-network-traces-for-http-metadata-exchange.md)

Der Netzwerk-Explorer verwendet [die Funktionsermittlung,](/previous-versions/windows/desktop/fundisc/fd-portal) um Netzwerkgeräte aufzuzählen. Weitere Informationen zur Problembehandlung finden Sie unter [Problembehandlung bei Funktionsermittlungsclients.](troubleshooting-function-discovery-clients.md)

Wenn die Ursache des Problems mithilfe der oben genannten Diagnoseverfahren nicht identifiziert werden kann, befolgen Sie die Anweisungen unter Aktivieren der [WSDAPI-Ablaufverfolgung,](enabling-wsdapi-tracing.md) und wenden Sie sich an den Microsoft-Support.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erste Schritte mit WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[Problembehandlung für Funktionsermittlungsclients](troubleshooting-function-discovery-clients.md)
</dt> </dl>

 

 
