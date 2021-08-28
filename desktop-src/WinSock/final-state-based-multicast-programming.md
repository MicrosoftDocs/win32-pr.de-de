---
description: In diesem Abschnitt wird die endzustandsbasierte Multicastprogrammierung mit IOCTLs anstelle von Socketoptionen beschrieben. Eine Übersicht darüber, wie sich die endzustandsbasierte Multicastprogrammierung von der änderungsbasierten Multicastprogrammierung unterscheidet, finden Sie unter Multicastprogrammierung.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Final-State-Based Multicast Programming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad31f0c840228e1fea729582f5e259ec92c4a04381752ed9ee50db2586b3b29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132513"
---
# <a name="final-state-based-multicast-programming"></a>Final-State-Based Multicast Programming

In diesem Abschnitt wird die endzustandsbasierte Multicastprogrammierung mit IOCTLs anstelle von Socketoptionen beschrieben. Eine Übersicht darüber, wie sich die endzustandsbasierte Multicastprogrammierung von der änderungsbasierten Multicastprogrammierung unterscheidet, finden Sie unter [Multicastprogrammierung.](multicast-programming.md)

In der folgenden Tabelle werden die Windows Sockets-IOCTLs beschrieben, die für die Multicastprogrammierung auf Windows verwendet werden. 

| Ioctl                       | Argumenttyp                                   |
|-----------------------------|-------------------------------------------------|
| SIOCSMSFILTER               | [**GROUP \_ FILTER-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) |
| SIOCGMSFILTER               | [**GROUP \_ FILTER-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) |
| SIO \_ GET \_ MULTICAST \_ FILTER | [**ip \_ msfilter-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |
| SIO \_ SET \_ MULTICAST \_ FILTER | [**ip \_ msfilter-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |



 

Beachten Sie, dass **SIOCSMSFILTER** und **SIOCGMSFILTER** IOCTLS auf Windows Vista und höher verfügbar sind.

Die Verwendung dieser IOCTLs für die Multicastprogrammierung bietet Leistungsvorteile bei der Arbeit mit großen Quelllisten. Weitere Informationen zu den Parametern und Einstellungen, die mit der Verwendung von SIO \_ GET \_ MULTICAST \_ FILTER oder SIO SET MULTICAST FILTER verknüpft \_ \_ \_ sind, finden Sie auf der [**Referenzseite \_ GRUPPENFILTER.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Weitere Informationen zu den Parametern und Einstellungen, die mit der Verwendung von SIO \_ GET \_ MULTICAST \_ FILTER oder SIO SET MULTICAST FILTER verknüpft \_ \_ \_ sind, finden Sie auf der [**\_ Ip-Msfilter-Referenzseite.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)

 

 



