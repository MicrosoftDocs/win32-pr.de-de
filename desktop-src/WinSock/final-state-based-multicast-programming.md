---
description: In diesem Abschnitt wird die endgültige Zustands basierte Multicast Programmierung mithilfe von IOCTLs anstelle von Socketoptionen beschrieben. Eine Übersicht über die Unterschiede zwischen der auf dem Endzustand basierenden Multicast Programmierung und der Änderungs basierten Multicast Programmierung finden Sie unter Multicast Programmierung.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Abschließende Zustands basierte Multicast Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360037"
---
# <a name="final-state-based-multicast-programming"></a>Abschließende Zustands basierte Multicast Programmierung

In diesem Abschnitt wird die endgültige Zustands basierte Multicast Programmierung mithilfe von IOCTLs anstelle von Socketoptionen beschrieben. Eine Übersicht über die Unterschiede zwischen der auf dem Endzustand basierenden Multicast Programmierung und der Änderungs basierten Multicast Programmierung finden Sie unter [Multicast Programmierung](multicast-programming.md).

In der folgenden Tabelle werden die Windows Sockets-IOCTLs beschrieben, die für die Multicast Programmierung unter Windows verwendet werden. 

| IOCTL                       | Argumenttyp                                   |
|-----------------------------|-------------------------------------------------|
| Siocsmsfilter               | [**Gruppe \_ Filter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Struktur |
| Siocgmsfilter               | [**Gruppe \_ Filter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Struktur |
| Prozessor \_ get- \_ Multicast \_ Filter | [**IP- \_ msfilter-**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) Struktur   |
| \_ \_ Multicast Filter für die SIO-Gruppe \_ | [**IP- \_ msfilter-**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) Struktur   |



 

Beachten Sie, dass **siocsmsfilter** und **siocgmsfilter** IOCTLs unter Windows Vista und höher verfügbar sind.

Die Verwendung dieser IOCTLs für Multicast Programmierung bietet bei der Arbeit mit großen Quell Listen Leistungsvorteile. Weitere Informationen zu den Parametern und Einstellungen, die mit der Verwendung von "sio \_ get \_ Multicast \_ Filter" oder "sio Set Multicast Filter" verknüpft sind, finden Sie auf \_ \_ \_ der Seite [**Gruppen \_ Filter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Referenz Weitere Informationen zu den Parametern und Einstellungen, die mit der Verwendung von " \_ mget \_ -Multicast \_ Filter" oder "sio \_ \_ -Multicast Filter" verknüpft sind, finden Sie auf \_ der Referenzseite zu [**IP \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)

 

 



