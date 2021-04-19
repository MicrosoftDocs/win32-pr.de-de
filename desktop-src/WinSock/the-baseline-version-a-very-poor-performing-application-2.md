---
description: Die Baselineversion einer sehr schlechten Leistung in Windows Sockets (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'Baselineversion: eine sehr schlechte leistungsfähige Anwendung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373083"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a>Baselineversion: eine sehr schlechte leistungsfähige Anwendung

Das anfängliche, schlechte Codebeispiel, das zum Berechnen der Updates verwendet wird, lautet wie folgt:

> [!Note]  
> Der Einfachheit halber gibt es in den folgenden Beispielen keine Fehlerbehandlung. Alle Produktionsanwendungen überprüfen immer Rückgabewerte.

 

> [!WARNING]
> Die ersten Beispiele der Anwendung sorgen für eine absichtlich schlechte Leistung, um mit Codeänderungen mögliche Leistungsverbesserungen zu veranschaulichen. Verwenden Sie diese Codebeispiele nicht in Ihrer Anwendung. Sie dienen nur zur Veranschaulichung.

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



In diesem Zustand hat die Anwendung eine möglichst schlechteste Netzwerkleistung. Folgende Probleme sind in dieser Version der Beispielanwendung zu finden:

-   Die Anwendung ist unterteilt. Jede Transaktion ist zu klein – die Zellen müssen nicht nacheinander aktualisiert werden.
-   Die Transaktionen werden streng serialisiert, auch wenn die Zellen gleichzeitig aktualisiert werden könnten.
-   Der Sendepuffer ist auf NULL festgelegt, und die Anwendung verursacht eine Verzögerung von 200 Millisekunden für jede Sende – dreimal pro Zelle.
-   Die Anwendung stellt eine hohe Verbindung her und stellt für jede Zelle eine Verbindung her. Anwendungen sind aufgrund des Zeit warte Zustands in der Anzahl der Verbindungen pro Sekunde für ein bestimmtes Ziel beschränkt, dies ist jedoch kein Problem, da jede Transaktion mehr als 600 Millisekunden benötigt.
-   Die Anwendung ist FAT. viele Transaktionen haben keine Auswirkung auf den Serverstatus, da viele Zellen nicht von Update zum Update geändert werden.
-   Die Anwendung zeigt ein schlechtes Streaming an. kleine Sende Vorgänge beanspruchen viel CPU und RAM.
-   Die Anwendung setzt eine Little-Endian-Darstellung für Ihre Sendungen voraus. Dies ist eine natürliche Annahme für die aktuelle Windows-Plattform, kann aber für lang gelebten Code gefährlich sein.

## <a name="key-performance-metrics"></a>Wichtige Leistungsmetriken

Die folgenden Leistungsmetriken werden in Roundtripzeit (RTT), goodput und Protokoll Mehraufwand ausgedrückt. Eine Erläuterung dieser Begriffe finden Sie im Thema zur [Netzwerkterminologie](network-terminology-2.md) .

-   Zellzeit, Netzwerk Zeit für das Update einer einzelnen Zelle, erfordert 4 \* RTT + 600 Millisekunden für Nagle und verzögerte ACK-Interaktionen.
-   Goodput ist kleiner als 6 Bytes.
-   Der Protokoll Mehraufwand beträgt 99,6%.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbessern einer langsamen Anwendung](improving-a-slow-application-2.md)
</dt> <dt>

[Netzwerkterminologie](network-terminology-2.md)
</dt> <dt>

[Revision 1: Bereinigen der offensichtlichen](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revision 2: Neuentwerfen für eine geringere Anzahl von Verbindungen](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revision 3: komprimierte Block-Sendevorgang](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Zukünftige Verbesserungen](future-improvements-2.md)
</dt> </dl>

 

 



