---
description: In dieser Version der Anwendung wird ein komprimierter Blockversand der Daten verwendet. Diese Änderung führt zu einer erheblichen Leistungsverbesserung.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revision Three: Compressed Block Send'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bba84010a09755c5b978665cbd8aa1b29068ec42294ab7b1e499c631fc6b472
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121280"
---
# <a name="revision-three-compressed-block-send"></a>Revision Three: Compressed Block Send

In dieser Version der Anwendung wird ein komprimierter Blockversand der Daten verwendet. Diese Änderung führt zu einer erheblichen Leistungsverbesserung.


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

-   Zellenupdates werden nicht mehr serialisiert.
-   Da ein Block send verwendet wird, wird die Anwendung nicht mehr überschattet.
-   Die Datenkomprimierung wird verwendet, was zu einer weniger fetten Anwendung führt.

Es besteht weiterhin ein Problem mit dieser Version der Anwendung. das Deadlockrisiko besteht, da ein großer Sendesenden ohne Empfang verwendet wird. Der Server sendet ein Byte für alle 3 empfangenen Bytes. Dies kann zu einem Deadlock führen, wenn die Empfangspuffergröße für diese Beispielanwendung kleiner als 1.000 Bytes ist.

## <a name="key-performance-metrics"></a>Wichtige Leistungsmetriken

Die folgenden Leistungsmetriken werden in Roundtripzeit (ROUND Trip Time, RTT), Goodput und Protokollmoverhead ausgedrückt. Eine Erläuterung dieser Begriffe finden Sie im Thema [Netzwerkterminologie.](network-terminology-2.md)

Diese Version spiegelt die folgenden Leistungsmetriken wider:

-   Zellenzeit – .002 \* RTT
-   Goodput – 2 Kilobyte/RTT
-   Protokollaufwand – 14 %

6 % des Mehraufwands von 14 % stammen aus den Ethernet-Headern, und die anderen 8 % stammen aus dem Start und der Entfernung der Verbindung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern einer langsamen Anwendung](improving-a-slow-application-2.md)
</dt> <dt>

[Netzwerkterminologie](network-terminology-2.md)
</dt> <dt>

[Baselineversion: Eine Anwendung mit sehr schlechter Leistung](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revision 1: Bereinigen des Offensichtlichen](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revision 2: Neugestaltung für weniger Verbindungen](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Zukünftige Verbesserungen](future-improvements-2.md)
</dt> </dl>

 

 



