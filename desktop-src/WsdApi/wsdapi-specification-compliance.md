---
description: Die Web Services on Devices-API (WSDAPI) bietet Unterstützung für das Geräteprofil für Webdienste (Devices Profile for Web Services, DPWS) auf Windows Vista, das die WS-Kommunikation (Web Services) zwischen Windows-basierten PCs und verbundenen Netzwerkgeräten ermöglicht.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: WSDAPI-Spezifikationskonformität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dcf649d8d2771d17f24e983a739c0119a0fe8af67f70b706ba35bcddec20d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991390"
---
# <a name="wsdapi-specification-compliance"></a>WSDAPI-Spezifikationskonformität

Die Web Services on Devices-API (WSDAPI) bietet Unterstützung für das [Geräteprofil für Webdienste (Devices Profile for Web Services,](https://specs.xmlsoap.org/ws/2006/02/devprof/) DPWS) auf Windows Vista, das die WS-Kommunikation (Web Services) zwischen Windows-basierten PCs und mit dem Netzwerk verbundenen Geräten ermöglicht. DPWS stellt grundlegende WS-Spezifikationen wie [WS-Eventing,](https://schemas.xmlsoap.org/ws/2004/08/eventing/) [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)und [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/)zusammen und erweitert oder beschränkt sie, um einen Baselinesatz von Funktionen für geräteeinschränkungen bereitzustellen. Diese Baselinespezifikation enthält erforderliche Funktionen, z. B. die Möglichkeit, Eigenschaften des Geräts über Metadaten zu beschreiben, und optionale Funktionen, z. B. die Möglichkeit, bestimmte Nachrichten aus Sicherheitsgründen abzulehnen.

Die WSDAPI-Implementierung in Windows Vista ist das erste Release der expliziten Unterstützung für DPWS und eine nicht verwaltete Implementierung von DPWS, die getrennt und von anderen Webdienstimplementierungen (z. [B.](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) der Windows Communication Foundation oder [WS-Management)](https://schemas.xmlsoap.org/ws/2005/06/management/)getrennt ist.

Die folgenden Themen sind für Gerätehersteller und andere Geräte implementierer von Interesse, die Geräte erstellen, die mit Windows-basierten WSDAPI-Clients und -Hosts zusammenarbeiten, ohne WSDAPI zu verwenden. In diesen Themen wird die Implementierung von WSDAPI relativ zu den zugrunde liegenden Spezifikationen beschrieben. Sie decken die Implementierung der erforderlichen Funktionalität, optionalen Funktionen und zusätzlichen Funktionen ab, die nicht in der Spezifikation definiert sind.

-   [DPWS-Spezifikationskonformität](dpws-specification-compliance.md)
-   [WS-Discovery Specification Compliance](ws-discovery-specification-compliance.md)
-   [WS-MetadataExchange- und WS-Transfer-Spezifikationskonformität](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Zusätzliche WS-Discovery-Funktionalität](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSD-Geräteentwicklung](wsd-device-development.md)
</dt> <dt>

[WSD-Geräteimplementierungen Empfehlungen](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
