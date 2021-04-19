---
description: Um Racebedingungen und Deadlocks zu vermeiden, ist es erforderlich, den Zugriff von mehreren Threads auf freigegebene Ressourcen zu synchronisieren. Die Synchronisierung ist auch erforderlich, um sicherzustellen, dass der abhängige Code in der richtigen Reihenfolge ausgeführt wird.
ms.assetid: 74af0502-dae1-438c-8e4b-7663093b3fe3
title: Synchronisieren der Ausführung mehrerer Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6a1b3dd51d666d507771476792e679f7980fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360531"
---
# <a name="synchronizing-execution-of-multiple-threads"></a>Synchronisieren der Ausführung mehrerer Threads

Um Racebedingungen und Deadlocks zu vermeiden, ist es erforderlich, den Zugriff von mehreren Threads auf freigegebene Ressourcen zu synchronisieren. Die Synchronisierung ist auch erforderlich, um sicherzustellen, dass der abhängige Code in der richtigen Reihenfolge ausgeführt wird.

Es gibt eine Reihe von Objekten, deren Handles zum Synchronisieren mehrerer Threads verwendet werden können. Zu diesen Objekten gehören:

-   Konsolen Eingabepuffer
-   Ereignisse
-   Mutexe
-   Prozesse
-   Semaphoren
-   Threads
-   Timer

Der Status der einzelnen Objekte wird entweder signalisiert oder nicht signalisiert. Wenn Sie ein Handle für eines dieser Objekte in einem Aufruf einer der [Wait-Funktionen](../sync/wait-functions.md)angeben, wird die Ausführung des aufrufenden Threads blockiert, bis der Zustand des angegebenen Objekts signalisiert wird.

Einige dieser Objekte sind nützlich, um einen Thread zu blockieren, bis ein Ereignis eintritt. Beispielsweise wird ein Konsolen Eingabe-Puffer Handle signalisiert, wenn ungelesene Eingaben vorhanden sind, z. b. Tastatureingaben oder Mausklicks. Prozess-und Thread Handles werden signalisiert, wenn der Prozess oder Thread beendet wird. Dies ermöglicht es einem Prozess z. b., einen untergeordneten Prozess zu erstellen und dann seine eigene Ausführung zu blockieren, bis der neue Prozess beendet wurde.

Andere Objekte sind nützlich, um freigegebene Ressourcen vor gleichzeitigem Zugriff zu schützen. Beispielsweise können mehrere Threads jeweils über ein Handle für ein Mutex-Objekt verfügen. Vor dem Zugriff auf eine freigegebene Ressource müssen die Threads eine der [Wait-Funktionen](../sync/wait-functions.md) aufrufen, um zu warten, bis der Zustand des Mutex signalisiert wird. Wenn der Mutex signalisiert wird, wird nur ein wartender Thread freigegeben, um auf die Ressource zuzugreifen. Der Zustand des Mutex wird sofort auf "nicht signalisiert" zurückgesetzt, sodass alle anderen wartenden Threads blockiert bleiben. Wenn der Thread mit der Ressource fertig ist, muss er den Zustand des Mutex auf "signalisiert" festlegen, damit andere Threads auf die Ressource zugreifen können.

Bei den Threads eines einzelnen Prozesses bieten kritische Abschnitts Objekte eine effizientere Methode der Synchronisierung als Mutexes. Ein kritischer Abschnitt wird wie ein Mutex verwendet, um einen Thread gleichzeitig für die Verwendung der geschützten Ressource zu aktivieren. Ein Thread kann die [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) -Funktion verwenden, um den Besitz eines kritischen Abschnitts anzufordern. Wenn Sie bereits im Besitz eines anderen Threads ist, wird der anfordernde Thread blockiert. Ein Thread kann die [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) -Funktion verwenden, um den Besitz eines kritischen Abschnitts anzufordern, ohne dass bei einem Fehler das Abrufen des kritischen Abschnitts blockiert wird. Nachdem Sie den Besitz erhalten hat, kann der Thread die geschützte Ressource verwenden. Die Ausführung der anderen Threads des Prozesses ist nicht betroffen, es sei denn, Sie versuchen, denselben kritischen Abschnitt einzugeben.

Mit der [**WaitForInputIdle**](/windows/desktop/api/Winuser/nf-winuser-waitforinputidle) -Funktion wird ein Thread gewartet, bis ein angegebener Prozess initialisiert wird und auf die Benutzereingabe wartet, ohne dass eine Eingabe aussteht. Der Aufruf von **WaitForInputIdle** kann zum Synchronisieren von über-und untergeordneten Prozessen nützlich sein, da [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) zurückgibt, ohne darauf zu warten, dass der untergeordnete Prozess die Initialisierung abschließt.

Weitere Informationen finden Sie unter [Synchronisierung](../sync/synchronization.md).

 

 
