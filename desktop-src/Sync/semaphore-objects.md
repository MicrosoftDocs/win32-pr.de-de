---
description: Ein Semaphorobjekt ist ein Synchronisierungsobjekt, das eine Anzahl zwischen 0 (null) und einem angegebenen Maximalwert beibehält.
ms.assetid: d9da1d98-a306-4e2d-a149-1eef6a724751
title: Semaphorobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c814be0ab2fafe7fbabfdeca5b640cfb550172a09e465dddc71629dfa5b0068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886259"
---
# <a name="semaphore-objects"></a>Semaphorobjekte

Ein *Semaphorobjekt* ist ein Synchronisierungsobjekt, das eine Anzahl zwischen 0 (null) und einem angegebenen Maximalwert beibehält. Die Anzahl wird jedes Mal dekrementiert, wenn ein Thread ein Warten auf das Semaphorobjekt abschließt, und jedes Mal erhöht, wenn ein Thread das Semaphor freigibt. Wenn die Anzahl 0 (null) erreicht, können keine weiteren Threads erfolgreich warten, bis der Zustand des Semaphorobjekts signalisiert wird. Der Status eines Semaphors wird auf „signalisiert“ festgelegt, wenn die Anzahl größer als Null ist, bzw. wird auf „nicht signalisiert“ gesetzt, wenn die Anzahl Null ist.

Das Semaphorobjekt ist nützlich, um eine freigegebene Ressource zu steuern, die eine begrenzte Anzahl von Benutzern unterstützen kann. Es fungiert als Gate, das die Anzahl der Threads, die die Ressource gemeinsam nutzen, auf eine angegebene maximale Anzahl beschränkt. Beispielsweise kann eine Anwendung die Anzahl von Fenstern begrenzen, die sie erstellt. Es wird ein Semaphor mit einer maximalen Anzahl verwendet, die dem Fensterlimit entspricht, wobei die Anzahl bei jeder Erstellung eines Fensters dekrementiert und erhöht wird, wenn ein Fenster geschlossen wird. Die Anwendung gibt das Semaphorobjekt beim Aufruf einer der [Wartefunktionen](wait-functions.md) an, bevor jedes Fenster erstellt wird. Wenn die Anzahl 0 (null) ist, was angibt, dass das Fensterlimit erreicht wurde, blockiert die Wait-Funktion die Ausführung des Fenstererstellungscodes.

Ein Thread verwendet die [**CreateSemaphore-**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) oder [**CreateSemaphoreEx-Funktion,**](/windows/desktop/api/WinBase/nf-winbase-createsemaphoreexa) um ein Semaphorobjekt zu erstellen. Der erstellende Thread gibt die Anfängliche Anzahl und den Höchstwert der Anzahl für das Objekt an. Die anfängliche Anzahl darf weder kleiner als 0 (null) noch größer als der Maximalwert sein. Der erstellende Thread kann auch einen Namen für das Semaphorobjekt angeben. Threads in anderen Prozessen können ein Handle für ein vorhandenes Semaphorobjekt öffnen, indem sie seinen Namen in einem Aufruf der [**OpenSemaphore-Funktion**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew) angeben. Weitere Informationen zu Namen für Mutex-, Ereignis-, Semaphor- und Timerobjekte finden Sie unter [Prozessübergreifende Synchronisierung.](interprocess-synchronization.md)

Wenn mehr als ein Thread auf ein Semaphor wartet, wird ein wartender Thread ausgewählt. Gehen Sie nicht von einer FIFO-Reihenfolge (First In, First Out) aus. Externe Ereignisse wie Kernelmodus-APCs können die Wartereihenfolge ändern.

Jedes Mal, wenn eine der [Wartefunktionen](wait-functions.md) zurückgibt, weil der Zustand eines Semaphors auf signalisiert festgelegt wurde, wird die Anzahl des Semaphors um eins verringert. Die [**ReleaseSemaphore-Funktion**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) erhöht die Anzahl eines Semaphors um einen angegebenen Betrag. Die Anzahl darf nie kleiner als 0 (null) oder größer als der Maximalwert sein.

Die anfängliche Anzahl eines Semaphors wird in der Regel auf den Höchstwert festgelegt. Die Anzahl wird dann von dieser Ebene heraufgesetzt, wenn die geschützte Ressource verbraucht wird. Alternativ können Sie ein Semaphor mit der anfangs 0 (null) Anzahl erstellen, um den Zugriff auf die geschützte Ressource zu blockieren, während die Anwendung initialisiert wird. Nach der Initialisierung können Sie [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) verwenden, um die Anzahl auf den Höchstwert zu erhöhen.

Ein Thread, der ein Mutexobjekt besitzt, kann wiederholt warten, bis dasselbe Mutexobjekt signalisiert wird, ohne dass dessen Ausführung blockiert wird. Ein Thread, der wiederholt auf das gleiche Semaphorobjekt wartet, jedoch die Anzahl des Semaphors bei jedem Abschluss eines Wartevorgangs dekrementiert. Der Thread wird blockiert, wenn die Anzahl auf 0 (null) festgelegt wird. Ebenso kann nur der Thread, der einen Mutex besitzt, die [**ReleaseMutex-Funktion**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) erfolgreich aufrufen, obwohl jeder Thread [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) verwenden kann, um die Anzahl eines Semaphorobjekts zu erhöhen.

Ein Thread kann die Anzahl eines Semaphors mehrmals dekrementieren, indem er wiederholt das gleiche Semaphorobjekt in Aufrufen einer der [Wartefunktionen](wait-functions.md)angibt. Das Aufrufen einer der Wartefunktionen mit mehreren Objekten mit einem Array, das mehrere Handles desselben Semaphors enthält, führt jedoch nicht zu mehreren Dekrementen.

Wenn Sie die Verwendung des Semaphorobjekts abgeschlossen haben, rufen Sie die [**CloseHandle-Funktion**](/windows/win32/api/handleapi/nf-handleapi-closehandle) auf, um das Handle zu schließen. Das Semaphorobjekt wird zerstört, wenn das letzte Handle geschlossen wurde. Das Schließen des Handles wirkt sich nicht auf die Semaphoranzahl aus. Rufen Sie daher [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) auf, bevor Sie das Handle schließen oder bevor der Prozess beendet wird. Andernfalls tritt bei ausstehenden Wartevorgängen entweder ein Time out oder eine unbegrenzte Fortsetzung auf, je nachdem, ob ein Time out-Wert angegeben wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Semaphorobjekten](using-semaphore-objects.md)
</dt> </dl>

 

 
