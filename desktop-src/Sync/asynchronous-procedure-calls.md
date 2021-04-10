---
description: Bei einem asynchronen Prozedur Aufruf(APC) handelt es sich um eine Funktion, die asynchron im Kontext eines bestimmten Threads ausgeführt wird.
ms.assetid: 0197d78e-a4dc-414b-88ba-c5ec5f2ed614
title: Asynchrone Prozedur Aufrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd95e9afd663e2a462335b3c47bfe99462b449e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960247"
---
# <a name="asynchronous-procedure-calls"></a>Asynchrone Prozedur Aufrufe

Bei einem *asynchronen Prozedur Aufruf(* APC) handelt es sich um eine Funktion, die asynchron im Kontext eines bestimmten Threads ausgeführt wird. Wenn ein APC in die Warteschlange eines Threads eingereiht wird, gibt das System einen Software unterbrechungs Fehler aus. Wenn der Thread das nächste Mal geplant wird, wird die APC-Funktion ausgeführt. Ein vom System generiertes APC wird als *kernelmodusapc* bezeichnet. Ein APC, das von einer Anwendung generiert wird, wird als *APC im Benutzermodus* bezeichnet. Ein Thread muss sich in einem wartungstabellenzustand befinden, um ein APC im Benutzermodus auszuführen.

Jeder Thread verfügt über eine eigene APC-Warteschlange. Eine Anwendung fügt eine APC in eine Warteschlange ein, indem Sie die [**queueuserapc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) -Funktion aufrufen. Der aufrufende Thread gibt die Adresse einer APC-Funktion im Aufruf von **queueuserapc** an. Die Warteschlange eines APC ist eine Anforderung, dass der Thread die APC-Funktion aufruft.

Wenn ein APC im Benutzermodus in die Warteschlange eingereiht wird, wird der Thread, in der er in die Warteschlange eingereiht wird, nicht so weitergeleitet, dass die APC-Funktion aufgerufen wird Ein Thread wechselt in einen mindestwarnzeit-Zustand, wenn er die Funktion " [**sleepex**](/windows/win32/api/synchapi/nf-synchapi-sleepex)", " [**signalobjectandwait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)", " [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)", " [**WaitForMultipleObjectsEx**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)" oder " [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) " aufruft. Wenn der Warte Vorgang erfüllt ist, bevor das APC in die Warteschlange eingereiht wird, befindet sich der Thread nicht mehr in einem Warteschlangen-Wartestatus, sodass die APC-Funktion nicht ausgeführt wird. Das APC wird jedoch immer noch in die Warteschlange eingereiht, sodass die APC-Funktion ausgeführt wird, wenn der Thread eine andere Warteschlangen-wait-Funktion aufruft.

Die Funktionen "read [**fileex**](/windows/win32/api/fileapi/nf-fileapi-readfileex)", " [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer)", " [**setwaitabletimerex**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)" und " [**Write fileex**](/windows/win32/api/fileapi/nf-fileapi-writefileex) " werden mithilfe eines APC als Rückrufmechanismus für Abschluss Benachrichtigungen implementiert.

Wenn Sie einen [Thread Pool](../procthread/thread-pools.md)verwenden, beachten Sie, dass APCs nicht ebenso wie andere Signalmechanismen funktionieren, da das System die Lebensdauer von Threads im Thread Pool steuert. Daher ist es möglich, dass ein Thread beendet wird, bevor die Benachrichtigung übermittelt wird. Verwenden Sie anstelle eines APC-basierten Signalisierungs Mechanismus, wie z. b. den *pfncompletionroutine* -Parameter von [**setwaitabletimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) oder [**setwaitabletimerex**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex), ein Objekt, das für [](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer)die Wiederverwendbarkeit verwendet wurde Verwenden Sie für die e/a-Vorgänge ein e/a-Abschluss Objekt, das mit " [**kreatethcdpoolio**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio) " erstellt wurde, oder eine auf *hevent* basierende [**über**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur, wobei das Ereignis an die Funktion " [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait) " übergeben werden kann.

## <a name="synchronization-internals"></a>Synchronisierungs internale

Wenn eine e/a-Anforderung ausgegeben wird, wird eine Struktur zugeordnet, um die Anforderung darzustellen. Diese Struktur wird als e/a-Anforderungspaket bezeichnet. Bei synchronen e/a-Vorgängen erstellt der Thread das unp, sendet es an den Geräte Stapel und wartet im Kernel, bis der unp-Vorgang beendet ist. Bei der asynchronen e/a erstellt der Thread das unp und sendet es an den Geräte Stapel. Der Stapel kann das unp sofort beenden, oder er gibt möglicherweise einen ausstehenden Status zurück, der angibt, dass die Anforderung ausgeführt wird. Wenn dies der Fall ist, ist das unp noch dem Thread zugeordnet, sodass es abgebrochen wird, wenn der Thread beendet wird oder eine Funktion wie [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio)aufruft. In der Zwischenzeit kann der Thread weiterhin andere Aufgaben durchführen, während der Geräte Stapel die Verarbeitung von "unp" fortsetzt.

Es gibt mehrere Möglichkeiten, wie das System angeben kann, dass das unp abgeschlossen wurde:

-   Aktualisieren Sie die überlappende Struktur durch das Ergebnis des Vorgangs, damit der Thread Abfragen kann, um zu bestimmen, ob der Vorgang abgeschlossen wurde.
-   Signalisieren Sie das Ereignis in der überlappenden Struktur, sodass ein Thread für das Ereignis synchronisiert und nach Abschluss des Vorgangs erneut aktiviert werden kann.
-   Fügen Sie das Gerät in die Warteschlange des ausstehenden APC-Threads ein, damit der Thread die APC-Routine ausführt, wenn er in einen warteschlangenwartestatus wechselt und vom warte Vorgang mit einem Status zurückkehrt, der angibt, dass eine oder mehrere APC-Routinen ausgeführt wurden.
-   Stellen Sie den Benutzer in eine Warteschlange für den e/a-Abschlussport, wo er vom nächsten Thread ausgeführt wird, der auf den Abschlussport wartet.

Threads, die auf einen e/a-Abschlussport warten, warten nicht in einem Warn baren Zustand. Wenn die Threads daher unps ausgeben, die als APCs an den Thread festgelegt sind, werden diese IPC-Vervollständigungen nicht rechtzeitig durchgeführt. Sie treten nur auf, wenn der Thread eine Anforderung vom e/a-Abschlussport abruft und dann eine warterattabellenwartezeit eingibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden eines aufnutzbaren Timers mit einem asynchronen Prozedur Befehl](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
