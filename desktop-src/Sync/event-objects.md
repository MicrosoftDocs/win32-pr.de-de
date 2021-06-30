---
description: Ein Ereignisobjekt ist ein Synchronisierungsobjekt, dessen Zustand mithilfe der SetEvent-Funktion explizit auf signalisiert festgelegt werden kann. Es folgen die beiden Typen von Ereignisobjekten.
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: Ereignisobjekte (Synchronisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ef4f5102df91cabb76529c9d4a9958859418aa
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102133"
---
# <a name="event-objects-synchronization"></a>Ereignisobjekte (Synchronisierung)

Ein *Ereignisobjekt ist* ein Synchronisierungsobjekt, dessen Zustand mithilfe der SetEvent-Funktion explizit auf [**signalisiert festgelegt werden**](/windows/win32/api/synchapi/nf-synchapi-setevent) kann. Es folgen die beiden Typen von Ereignisobjekten.



| Object             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manuelles Zurücksetzen des Ereignisses | Ein Ereignisobjekt, dessen Zustand signalisiert bleibt, bis es von der ResetEvent-Funktion explizit auf nicht [**signalisiert zurückgesetzt**](/windows/win32/api/synchapi/nf-synchapi-resetevent) wird. Während dies signalisiert wird, kann eine beliebige Anzahl von wartenden Threads oder Threads, die anschließend das gleiche Ereignisobjekt in einer der Wartefunktionen [angeben,](wait-functions.md)freigegeben werden.                                                                                                        |
| Ereignis für automatisches Zurücksetzen   | Ein Ereignisobjekt, dessen Zustand signalisiert bleibt, bis ein einzelner wartender Thread freigegeben wird. Zu diesem Zeitpunkt legt das System den Zustand automatisch auf nicht signalisiert fest. Wenn sich keine Threads in Warteposition befinden, verbleibt das Ereignisobjekt im signalisierten Zustand. Wenn mehrere Threads warten, wird ein wartender Thread ausgewählt. Gehen Sie nicht von einer FIFO-Reihenfolge (First In, First Out) aus. Externe Ereignisse wie Kernelmodus-APCs können die Wartereihen reihenfolge ändern.<br/> |



 

Das Ereignisobjekt ist nützlich, um ein Signal an einen Thread zu senden, das angibt, dass ein bestimmtes Ereignis aufgetreten ist. Beispielsweise legt das System bei überlappenden Eingaben und Ausgaben ein angegebenes Ereignisobjekt auf den signalisierten Zustand fest, wenn der überlappende Vorgang abgeschlossen wurde. Ein einzelner Thread kann verschiedene Ereignisobjekte in mehreren gleichzeitig überlappenden [](wait-functions.md) Vorgängen angeben und dann eine der Wartefunktionen mit mehreren Objekten verwenden, um auf den Zustand eines der Ereignisobjekte zu warten, die signalisiert werden.

Ein Thread verwendet die [**CreateEvent- oder**](/windows/win32/api/synchapi/nf-synchapi-createeventa) [**CreateEventEx-Funktion,**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) um ein Ereignisobjekt zu erstellen. Der erstellende Thread gibt den Anfangszustand des Objekts an und gibt an, ob es sich um ein Ereignisobjekt mit manueller oder automatischer Zurücksetzung handelt. Der erstellende Thread kann auch einen Namen für das Ereignisobjekt angeben. Threads in anderen Prozessen können ein Handle für ein vorhandenes Ereignisobjekt öffnen, indem sie ihren Namen in einem Aufruf der [**OpenEvent-Funktion**](/windows/win32/api/synchapi/nf-synchapi-openeventa) angeben. Weitere Informationen zu Namen für Mutex-, Ereignis-, Semaphor- und Timerobjekte finden Sie unter [Interprocess Synchronization](interprocess-synchronization.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Ereignisobjekten](using-event-objects.md)
</dt> </dl>

 

 
