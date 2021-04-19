---
description: In dieser Version der Anwendung wird ein komprimierter Block zum Senden der Daten verwendet. Diese Änderung führt zu einer erheblichen Verbesserung der Leistung.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revision 3: komprimierte Block-Sendevorgang'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348306"
---
# <a name="revision-three-compressed-block-send"></a>Revision 3: komprimierte Block-Sendevorgang

In dieser Version der Anwendung wird ein komprimierter Block zum Senden der Daten verwendet. Diese Änderung führt zu einer erheblichen Verbesserung der Leistung.


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a>Änderungen in dieser Version

Diese Version spiegelt die folgenden Änderungen wider:

-   Zell Aktualisierungen werden nicht mehr serialisiert.
-   Da ein Block-Sendevorgang verwendet wird, ist die Anwendung nicht mehr im Kopf.
-   Die Datenkomprimierung wird verwendet, was zu einer weniger FAT-Anwendung führt.

Es gibt immer noch ein Problem mit dieser Version der Anwendung. das Risiko eines Deadlocks besteht darin, dass ein großer Sendevorgang ohne empfangene Vorgänge verwendet wird. Der Server sendet pro 3 empfangener Bytes ein Byte. Dies kann zu einem Deadlock führen, wenn die Empfangs Puffergröße für diese Beispielanwendung weniger als 1000 Bytes beträgt.

## <a name="key-performance-metrics"></a>Wichtige Leistungsmetriken

Die folgenden Leistungsmetriken werden in Roundtripzeit (RTT), goodput und Protokoll Mehraufwand ausgedrückt. Eine Erläuterung dieser Begriffe finden Sie im Thema zur [Netzwerkterminologie](network-terminology-2.md) .

Diese Version reflektiert die folgenden Leistungsmetriken:

-   Zellzeit –. 002 \* RTT
-   Goodput – 2 Kilobyte/RTT
-   Protokoll Aufwand – 14%

Der mehr Aufwand von 14% beträgt 6% von den Ethernet-Headern und die anderen 8% vom Start bis zum Start der Verbindung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern einer langsamen Anwendung](improving-a-slow-application-2.md)
</dt> <dt>

[Netzwerkterminologie](network-terminology-2.md)
</dt> <dt>

[Baselineversion: eine sehr schlechte leistungsfähige Anwendung](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revision 1: Bereinigen der offensichtlichen](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Zukünftige Verbesserungen](future-improvements-2.md)
</dt> </dl>

 

 



