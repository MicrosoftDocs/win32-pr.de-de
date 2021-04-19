---
description: In dieser Version des Beispiel Programms wurden einige offensichtliche Änderungen vorgenommen, die den ersten Schritten bei der Verbesserung der Leistung in Kauf nehmen.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Revision 1: Bereinigen der offensichtlichen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348920"
---
# <a name="revision-one-cleaning-up-the-obvious"></a>Revision 1: Bereinigen der offensichtlichen

In dieser Version des Beispiel Programms wurden einige offensichtliche Änderungen vorgenommen, die den ersten Schritten bei der Verbesserung der Leistung in Kauf nehmen. Diese Version des Codes ist weit von der Leistungsoptimierung entfernt. es handelt sich jedoch um einen guten inkrementellen Schritt, der die Untersuchung der Auswirkungen von inkrementellen besseren Ansätzen ermöglicht.

> [!WARNING]
> Dieses Beispiel für die Anwendung bietet absichtlich eine schlechte Leistung, um mit Codeänderungen mögliche Leistungsverbesserungen zu veranschaulichen. Verwenden Sie dieses Codebeispiel nicht in Ihrer Anwendung. Dies dient nur zur Veranschaulichung.

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a>Änderungen in dieser Version

Diese Version spiegelt die folgenden Änderungen wider:

-   "Sndbuf = 0" wurde entfernt. Die 200 Millisekunden Verzögerungen aufgrund von ungepufferten Sende-und verzögerten Bestätigungen werden entfernt.
-   Das Sende-Send-Receive-Verhalten wurde entfernt. Diese Änderung beseitigt 200-Millisekunden-Verzögerungen aufgrund von Nagle-und verzögerten ACK-Interaktionen.
-   Die Little-d-Annahme wurde entfernt. Die Bytes sind nun in der richtigen Reihenfolge.

## <a name="remaining-problems"></a>Verbleibende Probleme

In dieser Version verbleiben die folgenden Probleme:

-   Die Anwendung stellt immer noch eine hohe Verbindung her. Da die Verzögerungen von 600 MS Millisekunden entfernt werden, erreicht die Anwendung jetzt die 12 Verbindungen pro Sekunde. Viele gleichzeitige Verbindungen werden nun zu einem Problem.
-   Die Anwendung ist immer noch FAT. unveränderte Zellen werden weiterhin an den Server weitergegeben.
-   Die Anwendung weist immer noch ein schlechtes Streaming auf. 3-Byte-Sendungen sind immer noch kleine Sende Vorgänge.
-   Die Anwendung sendet jetzt 2 Bytes/RTT, was bei einem direkt verbundenen Ethernet 4 KB/s beträgt. Dies ist nicht zu schnell, aber die Wartezeit führt wahrscheinlich zunächst zu Problemen.
-   Der Aufwand liegt bei bis zu 99,3%, was jedoch immer noch keinen guten Verwaltungs Prozentsatz zur Folge hat.

## <a name="key-performance-metrics"></a>Wichtige Leistungsmetriken

Die folgenden wichtigen Leistungsmetriken werden in Roundtripzeit (RTT), goodput und Protokoll Mehraufwand ausgedrückt. Eine Erläuterung dieser Begriffe finden Sie im Thema zur [Netzwerkterminologie](network-terminology-2.md) .

Diese Version reflektiert die folgenden Leistungsmetriken:

-   Zellzeit – 2 × RTT
-   Goodput – 2 Bytes/RTT
-   Protokoll Aufwand – 99,3 Prozent

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern einer langsamen Anwendung](improving-a-slow-application-2.md)
</dt> <dt>

[Netzwerkterminologie](network-terminology-2.md)
</dt> <dt>

[Baselineversion: eine sehr schlechte leistungsfähige Anwendung](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revision 3: komprimierte Block-Sendevorgang](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Zukünftige Verbesserungen](future-improvements-2.md)
</dt> </dl>

 

 



