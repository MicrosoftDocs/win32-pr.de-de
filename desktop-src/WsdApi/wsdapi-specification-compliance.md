---
description: Die Web Services on Devices-API (WSDAPI) bietet Unterstützung für das Geräte Profil für Webdienste (DPWS) unter Windows Vista, das die Kommunikation zwischen Windows-basierten PCs und Netzwerkgeräten ermöglicht.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: WSDAPI-Spezifikation Konformität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216154"
---
# <a name="wsdapi-specification-compliance"></a>WSDAPI-Spezifikation Konformität

Die Web Services on Devices-API (WSDAPI) bietet Unterstützung für das [Geräte Profil für Webdienste](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) unter Windows Vista, das die Kommunikation zwischen Windows-basierten PCs und Netzwerkgeräten ermöglicht. DPWS assembliert grundlegende WS-Spezifikationen wie [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)und [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/)und erweitert oder beschränkt Sie, um einen grundlegenden Satz von Funktionen für Ressourcen eingeschränkte Geräte bereitzustellen. Diese grundlegende Spezifikation enthält erforderliche Funktionen, wie z. b. die Möglichkeit, die Eigenschaften des Geräts durch Metadaten zu beschreiben, und optionale Funktionen, wie z. b. die Möglichkeit, bestimmte Nachrichten aus Sicherheitsgründen abzulehnen.

Die WSDAPI-Implementierung in Windows Vista ist die erste Version der expliziten Unterstützung für die DPWS und eine nicht verwaltete DPWS-Implementierung, die von anderen Webdienst Implementierungen (z. b. [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) oder [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/)) getrennt und unterschiedlich ist.

Die folgenden Themen sind für Gerätehersteller und andere geräteimplementierer von Interesse, die Geräte erstellen, die mit Windows-basierten WSDAPI-Clients und-Hosts interagieren, ohne WSDAPI zu verwenden. In diesen Themen wird die Implementierung von WSDAPI in Bezug auf die zugrunde liegenden Spezifikationen beschrieben. Sie umfassen die Implementierung von erforderlichen Funktionen, optionalen Funktionen und zusätzlichen Funktionen, die nicht in der Spezifikation definiert sind.

-   [Konformität der DPWS-Spezifikation](dpws-specification-compliance.md)
-   [Konformität der WS-Discovery-Spezifikation](ws-discovery-specification-compliance.md)
-   [Konformität mit WS-MetadataExchange und WS-Transfer Spezifikation](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Zusätzliche WS-Discovery Funktionen](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WSD-Geräteentwicklung](wsd-device-development.md)
</dt> <dt>

[Empfehlungen zur Implementierung der WSD-Geräte](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
