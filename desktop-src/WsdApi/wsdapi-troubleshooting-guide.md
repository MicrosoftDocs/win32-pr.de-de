---
description: Der Zweck dieses Handbuchs besteht darin, Benutzern zu helfen, Probleme zu beheben, die bei der Verwendung von WSDAPI-Ermittlungs-APIs auftreten, beim Erstellen eines WSDAPI-Hosts oder-Geräte Proxys oder bei Verwendung von Betriebssystemfunktionen (z. b. der Funktions Ermittlung oder des Netzwerk-Explorers), die WSDAPI
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: WSDAPI-Handbuch zur Problembehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c28e9a1fe4cc5b24b386cfb88e39276edc14cb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345234"
---
# <a name="wsdapi-troubleshooting-guide"></a>WSDAPI-Handbuch zur Problembehandlung

Der Zweck dieses Handbuchs besteht darin, Benutzern zu helfen, Probleme zu beheben, die bei der Verwendung von WSDAPI-Ermittlungs-APIs auftreten, beim Erstellen eines WSDAPI-Hosts oder-Geräte Proxys oder bei Verwendung von Betriebssystemfunktionen (z. b. der [Funktions](/previous-versions/windows/desktop/fundisc/fd-portal) Ermittlung oder des Netzwerk-Explorers), die WSDAPI Das Hauptziel besteht darin, Probleme zu beheben, wenn ein Client und Host sich nicht gegenseitig im Netzwerk befinden.

Für WSDAPI-Benutzer enthält dieses Handbuch Informationen, die Ihnen bei der erfolgreichen Problembehandlung eines Geräte Proxys (mit [**wsdkreatedeviceproxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)), einem Ermittlungs Anbieter (mit [**wsdkreatediscoveryprovider**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider)) oder einem Discovery Publisher (mit [**wsdkreatediscoverypublisher**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher)) helfen.

In dieser Anleitung wird davon ausgegangen, dass sowohl der Client als auch der Host in einer kontrollierten Umgebung ordnungsgemäß mit WSDAPI interagieren können. Dementsprechend soll dieses Handbuch nicht zur Problembehandlung bei DPWS-Stapeln dienen, die möglicherweise falsche WS-Nachrichten erzeugen. Informationen zum Testen der Interoperabilität mit WSDAPI finden Sie unter [WSDAPI Basic Interoperabilitäts Tool (wsdbit)](https://msdn.microsoft.com/library/cc264250.aspx) im Windows-Treiberkit (WDK).

Bevor Sie mit der Problembehandlung der Anwendung beginnen, sollten Sie sich mit den Nachrichten Mustern für die Ermittlung [und den Metadatenaustausch](discovery-and-metadata-exchange-message-patterns.md)vertraut machen

Dieses Handbuch enthält die folgenden Abschnitte:

-   [Ersten Schritte mit der WSDAPI-Problembehandlung](getting-started-with-wsdapi-troubleshooting.md)
-   [WSDAPI-Diagnose Prozeduren](wsdapi-diagnostic-procedures.md)
