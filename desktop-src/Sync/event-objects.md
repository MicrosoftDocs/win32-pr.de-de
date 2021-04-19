---
description: Ein Ereignis Objekt ist ein Synchronisierungs Objekt, dessen Zustand explizit mithilfe der SetEvent-Funktion auf "signalisiert" festgelegt werden kann. Im folgenden werden die beiden Typen von Ereignis Objekten angezeigt.
ms.assetid: 63dc2991-e070-4981-9e2d-90b4fdaaee7a
title: Ereignis Objekte (Synchronisierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365b42bb7550507fe3522f07d950dac74c88843d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363252"
---
# <a name="event-objects-synchronization"></a>Ereignis Objekte (Synchronisierung)

Ein *Ereignis Objekt* ist ein Synchronisierungs Objekt, dessen Zustand explizit mithilfe der [**SetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) -Funktion auf "signalisiert" festgelegt werden kann. Im folgenden werden die beiden Typen von Ereignis Objekten angezeigt.



| Object             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ereignis für manuelles Zurücksetzen | Ein Ereignis Objekt, dessen Zustand signalisiert bleibt, bis es von der [**ResetEvent**](/windows/win32/api/synchapi/nf-synchapi-resetevent) -Funktion explizit auf "nicht signalisiert" zurückgesetzt wird. Während der Signalisierung kann eine beliebige Anzahl von wartenden Threads oder Threads, die anschließend dasselbe Ereignis Objekt in einer der [warte Funktionen](wait-functions.md)angeben, freigegeben werden.                                                                                                        |
| Ereignis automatisch zurücksetzen   | Ein Ereignis Objekt, dessen Zustand signalisiert bleibt, bis ein einzelner wartender Thread freigegeben wird. zu diesem Zeitpunkt legt das System automatisch den Zustand auf "nicht signalisiert" fest. Wenn sich keine Threads in Warteposition befinden, verbleibt das Ereignisobjekt im signalisierten Zustand. Wenn mehr als ein Thread wartet, wird ein wartender Thread ausgewählt. Nehmen Sie keine Voraussetzung für eine FIFO-Reihenfolge (First in, First Out). Externe Ereignisse wie z. b. kernelmodusapcs können die Warte Reihenfolge ändern.<br/> |



 

Das Ereignis Objekt ist hilfreich beim Senden eines Signals an einen Thread, der angibt, dass ein bestimmtes Ereignis aufgetreten ist. Beispielsweise legt das System in überlappenden Eingaben und Ausgaben ein angegebenes Ereignis Objekt auf den signalisierten Zustand fest, wenn der überlappende Vorgang abgeschlossen wurde. Ein einzelner Thread kann verschiedene Ereignis Objekte in mehreren gleichzeitig überlappenden Vorgängen angeben und dann mithilfe einer der Wait- [Funktionen](wait-functions.md) mit mehreren Objekten darauf warten, dass der Status eines beliebigen Ereignis Objekts signalisiert wird.

Ein Thread verwendet die Funktion " [**forateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) " oder die Funktion " [**kreateeventex**](/windows/win32/api/synchapi/nf-synchapi-createeventexa) ", um ein Ereignis Objekt zu erstellen. Der Erstellungsthread gibt den ursprünglichen Zustand des-Objekts an und gibt an, ob es sich um ein manuelles Zurücksetzen oder Zurücksetzen-Ereignis Objekt handelt. Der Erstellungsthread kann auch einen Namen für das Ereignis Objekt angeben. Threads in anderen Prozessen können ein Handle für ein vorhandenes Ereignis Objekt öffnen, indem Sie den Namen in einem aufzurufenden [**OpenEvent**](/windows/win32/api/synchapi/nf-synchapi-openeventa) -Funktion angeben. Weitere Informationen zu den Namen von Mutex-, Ereignis-, Semaphore-und Timer-Objekten finden Sie unter [prozessübergreifende Synchronisierung](interprocess-synchronization.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Ereignis Objekten](using-event-objects.md)
</dt> </dl>

 

 
