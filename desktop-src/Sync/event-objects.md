---
description: Ein Ereignisobjekt ist ein Synchronisierungsobjekt, dessen Zustand mithilfe der SetEvent-Funktion explizit auf signalisiert festgelegt werden kann. Es folgen die beiden Typen von Ereignisobjekten.
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: Ereignisobjekte (Synchronisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9ea7c77fd61723b6ab927616817a5de2c323bf800431547800e2a96f33deee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886313"
---
# <a name="event-objects-synchronization"></a>Ereignisobjekte (Synchronisierung)

Ein *Ereignisobjekt* ist ein Synchronisierungsobjekt, dessen Zustand mithilfe der [**SetEvent-Funktion**](/windows/win32/api/synchapi/nf-synchapi-setevent) explizit auf signalisiert festgelegt werden kann. Es folgen die beiden Typen von Ereignisobjekten.



| Object             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ereignis für manuelles Zurücksetzen | Ein Ereignisobjekt, dessen Zustand signalisiert bleibt, bis es von der [**ResetEvent-Funktion**](/windows/win32/api/synchapi/nf-synchapi-resetevent) explizit auf nicht signalisiert zurückgesetzt wird. Während der Signalisierung kann eine beliebige Anzahl von wartenden Threads oder Threads, die anschließend dasselbe Ereignisobjekt in einer der [Wartefunktionen](wait-functions.md)angeben, freigegeben werden.                                                                                                        |
| Ereignis für automatisches Zurücksetzen   | Ein Ereignisobjekt, dessen Zustand signalisiert bleibt, bis ein einzelner wartenden Thread freigegeben wird. Zu diesem Zeitpunkt legt das System den Zustand automatisch auf nicht signalisiert fest. Wenn sich keine Threads in Warteposition befinden, verbleibt das Ereignisobjekt im signalisierten Zustand. Wenn mehr als ein Thread wartet, wird ein wartenden Thread ausgewählt. Gehen Sie nicht von einer FIFO-Reihenfolge (First In, First Out) aus. Externe Ereignisse wie Kernelmodus-APCs können die Wartereihenfolge ändern.<br/> |



 

Das Ereignisobjekt ist nützlich, um ein Signal an einen Thread zu senden, der angibt, dass ein bestimmtes Ereignis aufgetreten ist. Beispielsweise legt das System bei überlappender Eingabe und Ausgabe ein angegebenes Ereignisobjekt auf den signalisierten Zustand fest, wenn der überlappende Vorgang abgeschlossen wurde. Ein einzelner Thread kann verschiedene Ereignisobjekte in mehreren gleichzeitig überlappenden Vorgängen angeben und dann eine der [Wartefunktionen](wait-functions.md) mit mehreren Objekten verwenden, um auf den Zustand eines beliebigen Ereignisobjekts zu warten, das signalisiert wird.

Ein Thread verwendet die [**CreateEvent-**](/windows/win32/api/synchapi/nf-synchapi-createeventa) oder [**CreateEventEx-Funktion,**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) um ein Ereignisobjekt zu erstellen. Der erstellende Thread gibt den Anfangszustand des -Objekts an und gibt an, ob es sich um ein Ereignisobjekt mit manueller oder automatischer Zurücksetzung handelt. Der erstellende Thread kann auch einen Namen für das Ereignisobjekt angeben. Threads in anderen Prozessen können ein Handle für ein vorhandenes Ereignisobjekt öffnen, indem sie seinen Namen in einem Aufruf der [**OpenEvent-Funktion**](/windows/win32/api/synchapi/nf-synchapi-openeventa) angeben. Weitere Informationen zu Namen für Mutex-, Ereignis-, Semaphor- und Timerobjekte finden Sie unter [Prozessübergreifende Synchronisierung.](interprocess-synchronization.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Ereignisobjekten](using-event-objects.md)
</dt> </dl>

 

 
