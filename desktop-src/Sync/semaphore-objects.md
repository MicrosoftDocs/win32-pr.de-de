---
description: Ein Semaphor-Objekt ist ein Synchronisierungs Objekt, das eine Anzahl zwischen null und einem angegebenen maximalen Wert beibehält.
ms.assetid: d9da1d98-a306-4e2d-a149-1eef6a724751
title: Semaphore-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77f36313d76c5d98c786a76f10ad8439965f180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350892"
---
# <a name="semaphore-objects"></a>Semaphore-Objekte

Ein *Semaphor-Objekt* ist ein Synchronisierungs Objekt, das eine Anzahl zwischen null und einem angegebenen maximalen Wert beibehält. Die Anzahl wird jedes Mal dekrementiert, wenn ein Thread eine Wartezeit für das Semaphor-Objekt abschließt und jedes Mal erhöht wird, wenn ein Thread das Semaphor freigibt. Wenn die Anzahl Null erreicht, können keine weiteren Threads mehr darauf warten, dass der Semaphor-Objektzustand signalisiert wird. Der Status eines Semaphors wird auf „signalisiert“ festgelegt, wenn die Anzahl größer als Null ist, bzw. wird auf „nicht signalisiert“ gesetzt, wenn die Anzahl Null ist.

Das Semaphor-Objekt ist hilfreich beim Steuern einer freigegebenen Ressource, die eine begrenzte Anzahl von Benutzern unterstützen kann. Es fungiert als Gate, das die Anzahl der Threads einschränkt, die die Ressource auf eine angegebene maximale Anzahl freigeben. Beispielsweise kann eine Anwendung eine Beschränkung für die Anzahl der erstellten Fenster festlegen. Dabei wird ein Semaphor mit einer maximalen Anzahl gleich dem Fenster Limit verwendet. dabei wird die Anzahl verringert, wenn ein Fenster erstellt wird, und jedes Mal erhöht, wenn ein Fenster geschlossen wird. Die Anwendung gibt das Semaphor-Objekt an, das in einem der [warte Funktionen](wait-functions.md) aufgerufen wird, bevor jedes Fenster erstellt wird. Wenn die Anzahl Null ist – gibt an, dass das Fenster Limit erreicht wurde – wird die Ausführung des Code Erstellungs Codes durch die wait-Funktion blockiert.

Ein Thread verwendet die Funktion " [**foratesemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) " oder " [**foratesemaphoreex**](/windows/desktop/api/WinBase/nf-winbase-createsemaphoreexa) ", um ein Semaphor-Objekt zu erstellen. Der Erstellungsthread gibt die anfängliche Anzahl und den maximalen Wert der Anzahl für das Objekt an. Die anfängliche Anzahl darf nicht kleiner als 0 (null) oder größer als der Maximalwert sein. Der Erstellungsthread kann auch einen Namen für das Semaphor-Objekt angeben. Threads in anderen Prozessen können ein Handle für ein vorhandenes Semaphor-Objekt öffnen, indem Sie den Namen in einem Befehl der [**opensemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew) -Funktion angeben. Weitere Informationen zu den Namen von Mutex-, Ereignis-, Semaphore-und Timer-Objekten finden Sie unter [prozessübergreifende Synchronisierung](interprocess-synchronization.md).

Wenn mehr als ein Thread auf eine Semaphore wartet, wird ein wartender Thread ausgewählt. Nehmen Sie keine Voraussetzung für eine FIFO-Reihenfolge (First in, First Out). Externe Ereignisse wie z. b. kernelmodusapcs können die Warte Reihenfolge ändern.

Jedes Mal, wenn eine der [Wait-Funktionen](wait-functions.md) zurückgibt, da der Zustand eines Semaphors auf "signalisiert" festgelegt wurde, wird die Anzahl der Semaphor um eins verringert. Die [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) -Funktion vergrößert die Anzahl der Semaphore um einen angegebenen Betrag. Die Anzahl kann nie kleiner als 0 (null) oder größer als der Maximalwert sein.

Die anfängliche Anzahl eines Semaphors wird in der Regel auf den maximalen Wert festgelegt. Die Anzahl wird dann von dieser Ebene verringert, wenn die geschützte Ressource verwendet wird. Alternativ können Sie ein Semaphor mit einer anfänglichen Anzahl von NULL erstellen, um den Zugriff auf die geschützte Ressource zu blockieren, während die Anwendung initialisiert wird. Nach der Initialisierung können Sie [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) verwenden, um die Anzahl auf den maximalen Wert zu erhöhen.

Ein Thread, der ein Mutex-Objekt besitzt, kann wiederholt warten, bis das gleiche Mutex-Objekt signalisiert wird, ohne dass die Ausführung blockiert wird. Ein Thread, der wiederholt für dasselbe Semaphor-Objekt wartet, verringert jedoch die Anzahl der Semaphor, wenn ein warte Vorgang abgeschlossen ist. der Thread wird blockiert, wenn die Anzahl Null erreicht wird. Ebenso kann nur der Thread, der einen Mutex besitzt, die [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) -Funktion abrufen, obwohl jeder Thread [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) verwenden kann, um die Anzahl eines Semaphor-Objekts zu erhöhen.

Ein Thread kann den Zähler eines Semaphors mehrmals verringern, indem er das gleiche Semaphor-Objekt in Aufrufen einer beliebigen [Wartefunktion](wait-functions.md)wiederholt angibt. Das Aufrufen einer der Multiple-Object-Wait-Funktionen mit einem Array, das mehrere Handles desselben Semaphors enthält, führt jedoch nicht zu mehreren dekrements.

Wenn Sie mit dem Semaphor-Objekt fertig sind, müssen Sie die [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) -Funktion zum Schließen des Handles verwenden. Das Semaphor-Objekt wird zerstört, wenn sein letztes Handle geschlossen wurde. Das Schließen des Handles wirkt sich nicht auf die Anzahl der Semaphor aus. Stellen Sie daher vor dem Schließen des Handles oder vor dem Beenden des Prozesses sicher, dass Sie [**ReleaseSemaphore**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) aufruft. Andernfalls tritt für ausstehende warte Vorgänge entweder ein Timeout oder eine unbegrenzte Fortsetzung auf, je nachdem, ob ein Timeout Wert angegeben wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Semaphore-Objekten](using-semaphore-objects.md)
</dt> </dl>

 

 
