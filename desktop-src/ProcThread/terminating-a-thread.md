---
description: 'Das Beenden eines Threads hat die folgenden Ergebnisse: alle Ressourcen, die sich im Besitz des Threads befinden, z. b. Windows und Hooks, werden freigegeben. Der Thread Exitcode wird festgelegt. Das Thread Objekt wird signalisiert. Wenn der Thread der einzige aktive Thread im Prozess ist, wird der Prozess beendet. Weitere Informationen finden Sie unter Beenden eines Prozesses.'
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: Beenden eines Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada421356666316072aabff8281787cc140ad114
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348608"
---
# <a name="terminating-a-thread"></a>Beenden eines Threads

Das Beenden eines Threads hat die folgenden Ergebnisse:

-   Alle Ressourcen, die sich im Besitz des Threads befinden, z. b. Windows und Hooks, werden freigegeben.
-   Der Thread Exitcode wird festgelegt.
-   Das Thread Objekt wird signalisiert.
-   Wenn der Thread der einzige aktive Thread im Prozess ist, wird der Prozess beendet. Weitere Informationen finden Sie unter [Beenden eines Prozesses](terminating-a-process.md).

Die [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread) -Funktion gibt den Beendigungs Status eines Threads zurück. Während der Ausführung eines Threads ist der Beendigungs Status immer noch \_ aktiv. Wenn ein Thread beendet wird, ändert sich der Beendigungs Status von noch \_ aktiv in den Exitcode des Threads.

Wenn ein Thread beendet wird, ändert sich der Status des Thread Objekts in signalisiert und gibt alle anderen Threads frei, die auf das Beenden des Threads gewartet haben. Weitere Informationen zur Synchronisierung finden Sie unter [Synchronisieren der Ausführung mehrerer Threads](synchronizing-execution-of-multiple-threads.md).

Wenn ein Thread beendet wird, wird das zugehörige Thread Objekt erst freigegeben, wenn alle geöffneten Handles für den Thread geschlossen sind.

## <a name="how-threads-are-terminated"></a>Beenden von Threads

Ein Thread wird ausgeführt, bis eines der folgenden Ereignisse eintritt:

-   Der Thread ruft die [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) -Funktion auf.
-   Jeder Thread des Prozesses Ruft die [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) -Funktion auf.
-   Die Thread Funktion gibt zurück.
-   Jeder Thread ruft die [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) -Funktion mit einem Handle für den Thread auf.
-   Jeder Thread ruft die Funktion [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) mit einem Handle für den Prozess auf.

Der Exitcode für einen Thread ist entweder der Wert, der im [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)-, [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)-, [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)-oder [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)-Befehl angegeben ist, oder der Wert, der von der Thread Funktion zurückgegeben wird.

Wenn ein Thread durch [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)beendet wird, ruft das System die Einstiegspunkt Funktion der einzelnen angefügten dll mit einem Wert auf, der angibt, dass der Thread von der DLL getrennt wird (es sei denn, Sie rufen die Funktion [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) auf). Wenn ein Thread durch [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)beendet wird, werden die DLL-Einstiegspunkt Funktionen einmal aufgerufen, um anzugeben, dass der Prozess getrennt wird. DLLs werden nicht benachrichtigt, wenn ein Thread von [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) oder [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)beendet wird. Weitere Informationen zu DLLs finden Sie unter [Dynamic Link Libraries (Dynamic Link Libraries](../dlls/dynamic-link-libraries.md)).

Die Funktionen [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) und [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) sollten nur in extremen Fällen verwendet werden, da Sie keine Bereinigung von Threads, das Benachrichtigen von angefügten DLLs und das Freigeben des Anfangs Stapels nicht zulassen. Außerdem werden Handles zu Objekten, die sich im Besitz des Threads befinden, erst geschlossen, wenn der Prozess beendet wird. Die folgenden Schritte bieten eine bessere Lösung:

-   Erstellen Sie ein Ereignis Objekt mithilfe der Funktion " [**kreateevent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) ".
-   Erstellen Sie die Threads.
-   Jeder Thread überwacht den Ereignis Zustand durch Aufrufen der [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion. Verwenden Sie ein Timeout Intervall von 0 (null).
-   Jeder Thread beendet seine eigene Ausführung, wenn das Ereignis auf den signalisierten Zustand festgelegt ist ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) gibt Wait- \_ Objekt \_ 0 zurück).

 

 
