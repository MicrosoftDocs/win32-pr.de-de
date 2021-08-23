---
description: 'Das Beenden eines Threads hat die folgenden Ergebnisse: Alle Ressourcen im Besitz des Threads, z. B. Fenster und Hooks, werden freigegeben. Der Threadendungscode ist festgelegt. Das Threadobjekt wird signalisiert. Wenn der Thread der einzige aktive Thread im Prozess ist, wird der Prozess beendet. Weitere Informationen finden Sie unter Beenden eines Prozesses.'
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: Beenden eines Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef64729db5490ebdab3ba759b34a105c31d2cbc421a404d07b041aa9b611ba08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799040"
---
# <a name="terminating-a-thread"></a>Beenden eines Threads

Das Beenden eines Threads hat die folgenden Ergebnisse:

-   Alle Ressourcen im Besitz des Threads, z. B. Fenster und Hooks, werden freigegeben.
-   Der Threadendungscode ist festgelegt.
-   Das Threadobjekt wird signalisiert.
-   Wenn der Thread der einzige aktive Thread im Prozess ist, wird der Prozess beendet. Weitere Informationen finden Sie unter [Beenden eines Prozesses.](terminating-a-process.md)

Die [**GetExitCodeThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread) gibt den Beendigungsstatus eines Threads zurück. Während ein Thread ausgeführt wird, lautet sein Beendigungsstatus STILL \_ ACTIVE. Wenn ein Thread beendet wird, ändert sich sein Beendigungsstatus von STILL \_ ACTIVE in den Exitcode des Threads.

Wenn ein Thread beendet wird, ändert sich der Zustand des Threadobjekts in signalisiert und gibt alle anderen Threads frei, die auf die Beendigung des Threads gewartet haben. Weitere Informationen zur [Synchronisierung](synchronizing-execution-of-multiple-threads.md)finden Sie unter Synchronisieren der Ausführung mehrerer Threads.

Wenn ein Thread beendet wird, wird sein Threadobjekt erst freigegeben, wenn alle geöffneten Handles für den Thread geschlossen sind.

## <a name="how-threads-are-terminated"></a>Beenden von Threads

Ein Thread wird ausgeführt, bis eines der folgenden Ereignisse eintritt:

-   Der Thread ruft die [**ExitThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) auf.
-   Jeder Thread des Prozesses ruft die [**ExitProcess-Funktion auf.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)
-   Die Threadfunktion gibt zurück.
-   Jeder Thread ruft die [**TerminateThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) mit einem Handle für den Thread auf.
-   Jeder Thread ruft die [**TerminateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) mit einem Handle für den Prozess auf.

Der Exitcode für einen Thread ist entweder der Wert, der im Aufruf von [**ExitThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) [**ExitProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread)oder [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)angegeben ist, oder der von der Threadfunktion zurückgegebene Wert.

Wenn ein Thread durch [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread)beendet wird, ruft das System die Einstiegspunktfunktion jeder angefügten DLL mit einem Wert auf, der angibt, dass der Thread von der DLL getrennt wird (es sei denn, Sie rufen die [**DisableThreadLibraryCalls-Funktion**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) auf). Wenn ein Thread durch [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess)beendet wird, werden die DLL-Einstiegspunktfunktionen einmal aufgerufen, um anzugeben, dass der Prozess getrennt wird. DLLs werden nicht benachrichtigt, wenn ein Thread durch [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) oder [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)beendet wird. Weitere Informationen zu DLLs finden Sie unter [Dynamic Link Libraries](../dlls/dynamic-link-libraries.md).

Die [**Funktionen TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) und [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) sollten nur unter extremen Umständen verwendet werden, da sie keine Bereinigung von Threads zulassen, keine angefügten DLLs benachrichtigen und den anfänglichen Stapel nicht freigeben. Darüber hinaus werden Handles für Objekte, die sich im Besitz des Threads befinden, erst geschlossen, wenn der Prozess beendet wird. Die folgenden Schritte bieten eine bessere Lösung:

-   Erstellen Sie ein Ereignisobjekt mithilfe der [**CreateEvent-Funktion.**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
-   Erstellen Sie die Threads.
-   Jeder Thread überwacht den Ereigniszustand durch Aufrufen der [**WaitForSingleObject-Funktion.**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) Verwenden Sie ein Wartezeitintervall von 0 (null).
-   Jeder Thread beendet seine eigene Ausführung, wenn das Ereignis auf den signalisierten Zustand festgelegt ist ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) gibt WAIT \_ OBJECT \_ 0 zurück).

 

 
