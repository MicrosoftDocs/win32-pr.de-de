---
description: Ein asynchroner Prozeduraufruf (APC) ist eine Funktion, die asynchron im Kontext eines bestimmten Threads ausgeführt wird.
ms.assetid: 0197d78e-a4dc-414b-88ba-c5ec5f2ed614
title: Asynchrone Prozeduraufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1c024506c2afc9a895db645fd386ed76f915f6e1178c6b8ce3a257aa7d40fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661450"
---
# <a name="asynchronous-procedure-calls"></a>Asynchrone Prozeduraufrufe

Ein *asynchroner Prozeduraufruf* (APC) ist eine Funktion, die asynchron im Kontext eines bestimmten Threads ausgeführt wird. Wenn ein APC in die Warteschlange eines Threads eingereiht wird, gibt das System einen Softwareunterbruch aus. Wenn der Thread das nächste Mal geplant wird, wird die APC-Funktion ausgeführt. Ein vom System generierter APC wird als *Kernelmodus-APC* bezeichnet. Ein von einer Anwendung generierter APC wird als *APC im Benutzermodus* bezeichnet. Ein Thread muss sich in einem warnungsfähigen Zustand befinden, um ein APC im Benutzermodus auszuführen.

Jeder Thread verfügt über eine eigene APC-Warteschlange. Eine Anwendung stellt einen APC in die Warteschlange eines Threads, indem die [**QueueUserAPC-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) aufgerufen wird. Der aufrufende Thread gibt die Adresse einer APC-Funktion im Aufruf von **QueueUserAPC** an. Das Warteschlangening eines APC ist eine Anforderung an den Thread, die APC-Funktion aufzurufen.

Wenn ein Benutzermodus-APC in die Warteschlange eingereiht wird, wird der Thread, in dem er in die Warteschlange eingereiht wird, nicht zum Aufrufen der APC-Funktion weitergeleitet, es sei denn, er befindet sich in einem warnungsfähigen Zustand. Ein Thread wechselt in einen warnungsfähigen Zustand, wenn er die [**SleepEx-,**](/windows/win32/api/synchapi/nf-synchapi-sleepex) [**SignalObjectAndWait-,**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) [**MsgWaitForMultipleObjectsEx-,**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) [**WaitForMultipleObjectsEx-**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)oder [**WaitForSingleObjectEx-Funktion**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) aufruft. Wenn der Wartezustand erfüllt ist, bevor der APC in die Warteschlange eingereiht wird, befindet sich der Thread nicht mehr in einem warnungsfähigen Wartezustand, sodass die APC-Funktion nicht ausgeführt wird. Der APC befindet sich jedoch weiterhin in der Warteschlange, sodass die APC-Funktion ausgeführt wird, wenn der Thread eine andere warnungsfähige Wartefunktion aufruft.

Die Funktionen [**ReadFileEx,**](/windows/win32/api/fileapi/nf-fileapi-readfileex) [**SetWaitableTimer,**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)und [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) werden mithilfe eines APC als Rückrufmechanismus für Abschlussbenachrichtigungen implementiert.

Wenn Sie einen [Threadpool](../procthread/thread-pools.md)verwenden, beachten Sie, dass APCs nicht so gut funktionieren wie andere Signalisierungsmechanismen, da das System die Lebensdauer von Threadpoolthreads steuert, sodass es möglich ist, dass ein Thread beendet wird, bevor die Benachrichtigung übermittelt wird. Anstatt einen APC-basierten Signalisierungsmechanismus wie den *pfnCompletionRoutine-Parameter* von [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) oder [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)zu verwenden, verwenden Sie ein wartebares Objekt, z. B. einen timer, der mit [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)erstellt wurde. Verwenden Sie für E/A ein E/A-Vervollständigungsobjekt, das mit [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio) erstellt wurde, oder eine *hEvent-basierte* [**OVERLAPPED-Struktur,**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) in der das Ereignis an die [**SetThreadpoolWait-Funktion**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait) übergeben werden kann.

## <a name="synchronization-internals"></a>Interne Synchronisierungsvorgänge

Wenn eine E/A-Anforderung ausgegeben wird, wird eine -Struktur zugeordnet, um die Anforderung darzustellen. Diese Struktur wird als E/A-Anforderungspaket (IRP) bezeichnet. Bei synchroner E/A erstellt der Thread das IRP, sendet es an den Gerätestapel und wartet im Kernel auf den Abschluss des IRP. Bei asynchroner E/A erstellt der Thread das IRP und sendet es an den Gerätestapel. Der Stapel kann den IRP sofort abschließen oder den Status "Ausstehend" zurückgeben, der angibt, dass die Anforderung ausgeführt wird. In diesem Fall ist das IRP weiterhin dem Thread zugeordnet, sodass er abgebrochen wird, wenn der Thread beendet wird oder eine Funktion wie [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio)aufruft. In der Zwischenzeit kann der Thread weitere Aufgaben ausführen, während der Gerätestapel die Verarbeitung des IRP fortsetzt.

Es gibt mehrere Möglichkeiten, wie das System angeben kann, dass das IRP abgeschlossen wurde:

-   Aktualisieren Sie die überlappende Struktur mit dem Ergebnis des Vorgangs, damit der Thread abfragen kann, ob der Vorgang abgeschlossen wurde.
-   Signalisieren Sie das Ereignis in der überlappenden Struktur, damit ein Thread für das Ereignis synchronisiert werden kann und nach Abschluss des Vorgangs aufgeweckt wird.
-   Stellen Sie das IRP dem ausstehenden APC des Threads in die Warteschlange, damit der Thread die APC-Routine ausführt, wenn er in einen warnungsfähigen Wartezustand wechselt, und vom Wartevorgang mit dem Status zurückgegeben wird, dass mindestens eine APC-Routine ausgeführt wurde.
-   Stellen Sie das IRP an einen E/A-Abschlussport in die Warteschlange, wo er vom nächsten Thread ausgeführt wird, der auf den Abschlussport wartet.

Threads, die auf einen E/A-Abschlussport warten, warten nicht in einem warnungsfähigen Zustand. Wenn diese Threads IRPs ausstellen, die als APCs für den Thread abgeschlossen werden sollen, treten diese IPC-Vervollständigungen daher nicht rechtzeitig auf. sie treten nur auf, wenn der Thread eine Anforderung vom E/A-Abschlussport übernimmt und dann einen warnungsfähigen Wartezustand eingibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden eines wartebaren Timers mit einem asynchronen Prozeduraufruf](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
