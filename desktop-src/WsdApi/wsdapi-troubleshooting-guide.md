---
description: Dieser Leitfaden soll Benutzern helfen, Fehler zu beheben, die bei der Verwendung von WSDAPI-Ermittlungs-APIs, beim Erstellen eines WSDAPI-Hosts oder -Geräteproxys oder bei der Verwendung von Betriebssystemfunktionen (z. B. Funktionsermittlung oder Netzwerk-Explorer), die auf WSDAPI basieren, auftreten.
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: WSDAPI – Leitfaden zur Problembehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a904b2bf4072721e6c0e9c01191aa1b3d5f55224b096434062b7aa8535fa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860031"
---
# <a name="wsdapi-troubleshooting-guide"></a>WSDAPI – Leitfaden zur Problembehandlung

Dieser Leitfaden soll Benutzern helfen, Fehler zu beheben, die bei der Verwendung von WSDAPI-Ermittlungs-APIs, beim Erstellen eines WSDAPI-Hosts oder -Geräteproxys oder bei der Verwendung von Betriebssystemfunktionen (z. B. [Funktionsermittlung](/previous-versions/windows/desktop/fundisc/fd-portal) oder Netzwerk-Explorer), die auf WSDAPI basieren, auftreten. Das Hauptziel besteht darin, bei der Problembehandlung zu helfen, wenn sich client und host im Netzwerk nicht gegenseitig sehen können.

Für WSDAPI-Benutzer enthält dieses Handbuch Informationen, die Ihnen bei der erfolgreichen Problembehandlung eines Geräteproxys (mit [**WSDCreateDeviceProxy),**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)eines Ermittlungsanbieters (mit [**WSDCreateDiscoveryProvider)**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider)oder eines Ermittlungsherausgebers (mit [**WSDCreateDiscoveryPublisher)**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher)helfen.

In diesem Leitfaden wird davon ausgegangen, dass sowohl der Client als auch der Host ordnungsgemäß mit WSDAPI in einer kontrollierten Umgebung zusammenarbeiten können. Entsprechend ist dieser Leitfaden nicht als Hilfe bei der Problembehandlung von DPWS-Stapeln gedacht, die möglicherweise falsche WS-Nachrichten generieren. Informationen zum Testen der Interoperabilität mit WSDAPI finden Sie im [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) im Windows Driver Kit (WDK).

Bevor Sie mit der Problembehandlung Ihrer Anwendung beginnen, sollten Sie sich mit [Ermittlung und Metadaten Exchange Nachrichtenmustern](discovery-and-metadata-exchange-message-patterns.md)vertraut machen.

Dieses Handbuch enthält die folgenden Abschnitte:

-   [Erste Schritte mit WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
-   [WSDAPI-Diagnoseverfahren](wsdapi-diagnostic-procedures.md)
