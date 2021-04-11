---
description: In dieser Revision wird die Beispielanwendung neu gestaltet, um unnötige Verbindungen auszuschließen.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 'Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131028"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a>Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen

In dieser Revision wird die Beispielanwendung neu gestaltet, um unnötige Verbindungen auszuschließen.

> [!WARNING]
> Diese Anwendungsbeispiele sorgen auch für eine absichtlich schlechte Leistung, um mit Codeänderungen mögliche Leistungsverbesserungen zu veranschaulichen. Verwenden Sie dieses Codebeispiel nicht in Ihrer Anwendung. Dies dient nur zur Veranschaulichung.

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a>Verbleibende Probleme

Durch die Änderungen in Revision 2 wurde die Anwendung neu gestaltet, sodass nur eine Verbindung pro Update hergestellt werden konnte. Die Anwendung beinhaltet weiterhin folgende Leistungsprobleme:

-   Die Anwendung wird immer noch serialisiert und ist unterteilt.
-   Die Anwendung hat immer noch ein FAT-Design. Es gibt viele Sende Vorgänge, für die in diesem Entwurf kein Vorgang erforderlich ist.
-   Die Sende Vorgänge sind immer noch nur 3 Bytes, was zu einem schlechten Streaming gehört.

## <a name="key-performance-metrics"></a>Wichtige Leistungsmetriken

Die folgenden Leistungsmetriken werden in Roundtripzeit (RTT), goodput und Protokoll Mehraufwand ausgedrückt. Eine Erläuterung dieser Begriffe finden Sie im Thema zur [Netzwerkterminologie](network-terminology-2.md) .

Diese Version reflektiert die folgenden Leistungsmetriken:

-   Zellzeit – 1 \* RTT
-   Goodput – 4 Bytes/RTT
-   Protokoll Aufwand – 96,8%

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

[Revision 3: komprimierte Block-Sendevorgang](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Zukünftige Verbesserungen](future-improvements-2.md)
</dt> </dl>

 

 



