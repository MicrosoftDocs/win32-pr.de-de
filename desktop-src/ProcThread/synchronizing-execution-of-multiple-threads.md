---
description: Um Racebedingungen und Deadlocks zu vermeiden, ist es erforderlich, den Zugriff mehrerer Threads auf freigegebene Ressourcen zu synchronisieren. Die Synchronisierung ist auch erforderlich, um sicherzustellen, dass abhängiger Code in der richtigen Reihenfolge ausgeführt wird.
ms.assetid: 74af0502-dae1-438c-8e4b-7663093b3fe3
title: Synchronisieren der Ausführung mehrerer Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04a7e80f3c1d4ffdd874d9627a8212e26ee4923a5f2349bdebc4ff09299936c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793093"
---
# <a name="synchronizing-execution-of-multiple-threads"></a>Synchronisieren der Ausführung mehrerer Threads

Um Racebedingungen und Deadlocks zu vermeiden, ist es erforderlich, den Zugriff mehrerer Threads auf freigegebene Ressourcen zu synchronisieren. Die Synchronisierung ist auch erforderlich, um sicherzustellen, dass abhängiger Code in der richtigen Reihenfolge ausgeführt wird.

Es gibt eine Reihe von -Objekten, deren Handles zum Synchronisieren mehrerer Threads verwendet werden können. Zu diesen Objekten gehören:

-   Konsoleneingabepuffer
-   Ereignisse
-   Mutexe
-   Prozesse
-   Semaphoren
-   Threads
-   Timer

Der Zustand jedes dieser Objekte wird entweder signalisiert oder nicht signalisiert. Wenn Sie ein Handle für eines dieser Objekte in einem Aufruf einer der [Wartefunktionen](../sync/wait-functions.md)angeben, wird die Ausführung des aufrufenden Threads blockiert, bis der Zustand des angegebenen Objekts signalisiert wird.

Einige dieser Objekte sind nützlich, um einen Thread zu blockieren, bis ein Ereignis eintritt. Beispielsweise wird ein Konsoleneingabepufferhandle signalisiert, wenn ungelesene Eingaben vorhanden sind, z. B. eine Tastatureingabe oder ein Mausklick. Prozess- und Threadhandles werden signalisiert, wenn der Prozess oder Thread beendet wird. Dadurch kann ein Prozess z. B. einen untergeordneten Prozess erstellen und dann seine eigene Ausführung blockieren, bis der neue Prozess beendet wurde.

Andere Objekte sind nützlich, um freigegebene Ressourcen vor gleichzeitigen Zugriffen zu schützen. Beispielsweise können mehrere Threads jeweils über ein Handle für ein Mutexobjekt verfügen. Vor dem Zugriff auf eine freigegebene Ressource müssen die Threads eine der [Wartefunktionen](../sync/wait-functions.md) aufrufen, um auf die Signalisierung des Status des Mutex zu warten. Wenn der Mutex signalisiert wird, wird nur ein wartenden Thread für den Zugriff auf die Ressource freigegeben. Der Status des Mutex wird sofort auf nicht signalisiert zurückgesetzt, sodass alle anderen wartenden Threads blockiert bleiben. Wenn der Thread mit der Ressource fertig ist, muss er den Status des Mutex auf signalisiert festlegen, damit andere Threads auf die Ressource zugreifen können.

Für die Threads eines einzelnen Prozesses stellen Critical-Section-Objekte ein effizienteres Synchronisierungsverfahren als Mutexe bereit. Ein kritischer Abschnitt wird wie ein Mutex verwendet, um jeweils einen Thread für die Verwendung der geschützten Ressource zu aktivieren. Ein Thread kann die [**EnterCriticalSection-Funktion**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) verwenden, um den Besitz eines kritischen Abschnitts anzufordern. Wenn er bereits im Besitz eines anderen Threads ist, wird der anfordernde Thread blockiert. Ein Thread kann die [**TryEnterCriticalSection-Funktion**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) verwenden, um den Besitz eines kritischen Abschnitts anzufordern, ohne bei einem Fehler beim Abrufen des kritischen Abschnitts zu blockieren. Nachdem er den Besitz erhalten hat, kann der Thread die geschützte Ressource verwenden. Die Ausführung der anderen Threads des Prozesses ist nicht betroffen, es sei denn, sie versuchen, in denselben kritischen Abschnitt zu gelangen.

Mit [**der WaitForInputIdle-Funktion**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle) wartet ein Thread, bis ein angegebener Prozess initialisiert wird, und wartet auf Benutzereingaben ohne ausstehende Eingabe. Das Aufrufen von **WaitForInputIdle** kann nützlich sein, um übergeordnete und untergeordnete Prozesse zu synchronisieren, da [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) zurückgibt, ohne auf den Abschluss der Initialisierung des untergeordneten Prozesses zu warten.

Weitere Informationen finden Sie unter [Synchronisierung.](../sync/synchronization.md)

 

 
