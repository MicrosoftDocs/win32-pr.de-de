---
description: E/A-Abschlussports bieten ein effizientes Threadingmodell für die Verarbeitung mehrerer asynchroner E/A-Anforderungen auf einem Multiprozessorsystem.
ms.assetid: 213c48e8-bb21-43ed-9c00-2a5cf8ac25f0
title: E/A-Abschlussports
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2133bb14c661580eaf8004bd92c6f947b3b8777a4b1a5f6b330fe631b2be6c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050830"
---
# <a name="io-completion-ports"></a>E/A-Abschlussports

E/A-Abschlussports bieten ein effizientes Threadingmodell für die Verarbeitung mehrerer asynchroner E/A-Anforderungen auf einem Multiprozessorsystem. Wenn ein Prozess einen E/A-Abschlussport erstellt, erstellt das System ein zugeordnetes Warteschlangenobjekt für Anforderungen, deren einziger Zweck die Verarbeitung dieser Anforderungen ist. Prozesse, die viele gleichzeitige asynchrone E/A-Anforderungen verarbeiten, können dies schneller und effizienter durchführen, indem E/A-Vervollständigungsports in Verbindung mit einem vorab zugeordneten Threadpool verwendet werden, anstatt Threads zum Zeitpunkt des Empfangs einer E/A-Anforderung zu erstellen.

## <a name="how-io-completion-ports-work"></a>Funktionsweise von E/A-Vervollständigungsports

Die [**CreateIoCompletionPort-Funktion**](createiocompletionport.md) erstellt einen E/A-Vervollständigungsport und ordnet diesem Port einen oder mehrere Dateihandles zu. Wenn ein asynchroner E/A-Vorgang für einen dieser Dateihandles abgeschlossen wird, wird ein E/A-Vervollständigungspaket in fiFO-Reihenfolge (First-in-First-Out) an den zugeordneten E/A-Abschlussport in die Warteschlange gestellt. Eine leistungsstarke Verwendung dieses Mechanismus besteht in der Kombination des Synchronisierungspunkts für mehrere Dateihandles in einem einzigen Objekt, obwohl es auch andere nützliche Anwendungen gibt. Beachten Sie, dass die Pakete in der FIFO-Reihenfolge in der Warteschlange stehen und in einer anderen Reihenfolge aus der Warteschlange entfernt werden können.

> [!Note]
>
> Der hier *verwendete Begriff Dateihandl* bezieht sich auf eine Systemabstraktion, die einen überlappenden E/A-Endpunkt darstellt, nicht nur eine Datei auf dem Datenträger. Dies kann z. B. ein Netzwerkendpunkt, ein TCP-Socket, eine Named Pipe oder ein E-Mail-Slot sein. Jedes Systemobjekt, das überlappende E/A unterstützt, kann verwendet werden. Eine Liste verwandter E/A-Funktionen finden Sie am Ende dieses Themas.

 

Wenn ein Dateihand handle einem Vervollständigungsport zugeordnet ist, wird der übergebene Statusblock erst aktualisiert, wenn das Paket aus dem Vervollständigungsport entfernt wird. Die einzige Ausnahme ist, wenn der ursprüngliche Vorgang synchron mit einem Fehler zurückgegeben wird. Ein Thread (entweder vom Hauptthread oder vom Hauptthread selbst erstellt) verwendet die [**GetQueuedCompletionStatus-Funktion,**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) um auf die Warteschlange eines Abschlusspakets am E/A-Abschlussport zu warten, anstatt direkt auf den Abschluss der asynchronen E/A zu warten. Threads, die ihre Ausführung an einem E/A-Abschlussport blockieren, werden in LIFO-Reihenfolge (Last-in-First-Out) freigegeben, und das nächste Vervollständigungspaket wird aus der FIFO-Warteschlange des E/A-Abschlussports für diesen Thread gezogen. Wenn ein Vervollständigungspaket an einen Thread freigegeben wird, gibt das System den letzten (letzten) Thread frei, der diesem Port zugeordnet ist, und überlässt ihm die Abschlussinformationen für die älteste E/A-Vervollständigung.

Obwohl eine beliebige Anzahl von Threads [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) für einen angegebenen E/A-Abschlussport aufrufen kann, wird er dem angegebenen E/A-Abschlussport zugeordnet, wenn ein angegebener Thread **GetQueuedCompletionStatus** zum ersten Mal aufruft, bis einer der drei Folgenden eintritt: Der Thread wird beendet, gibt einen anderen E/A-Abschlussport an oder schließt den E/A-Abschlussport. Anders ausgedrückt: Ein einzelner Thread kann mindestens einem E/A-Abschlussport zugeordnet werden.

Wenn ein Vervollständigungspaket an einem E/A-Abschlussport in die Warteschlange gestellt wird, überprüft das System zunächst, wie viele Threads ausgeführt werden, die diesem Port zugeordnet sind. Wenn die Anzahl der ausgeführten Threads kleiner ist als der Parallelitätswert (im nächsten Abschnitt erläutert), darf einer der wartenden Threads (der letzte) das Abschlusspaket verarbeiten. Wenn die Verarbeitung eines ausgeführten Threads abgeschlossen ist, ruft er in der Regel [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) erneut auf. An diesem Punkt wird entweder mit dem nächsten Vervollständigungspaket zurückgegeben, oder es wird gewartet, wenn die Warteschlange leer ist.

Threads können die [**PostQueuedCompletionStatus-Funktion**](postqueuedcompletionstatus.md) verwenden, um Vervollständigungspakete in der Warteschlange eines E/A-Abschlussports zu platzieren. Dadurch kann der Abschlussport verwendet werden, um zusätzlich zum Empfangen von E/A-Vervollständigungspaketen vom E/A-System Kommunikation von anderen Threads des Prozesses zu empfangen. Mit **der PostQueuedCompletionStatus-Funktion** kann eine Anwendung ihre eigenen speziellen Vervollständigungspakete an den E/A-Abschlussport in die Warteschlange stellen, ohne einen asynchronen E/A-Vorgang zu starten. Dies ist beispielsweise nützlich, um Arbeitsthreads über externe Ereignisse zu benachrichtigen.

Das Handle für den E/A-Abschlussport und jedes Dateihand handle, das diesem bestimmten E/A-Vervollständigungsport zugeordnet ist, werden als Verweise auf den *E/A-Abschlussport bezeichnet.* Der E/A-Vervollständigungsport wird freigegeben, wenn keine Verweise mehr darauf stehen. Daher müssen alle diese Handles ordnungsgemäß geschlossen werden, um den E/A-Abschlussport und die zugehörigen Systemressourcen frei zu geben. Nachdem diese Bedingungen erfüllt sind, sollte eine Anwendung das Porthandle für die E/A-Vervollständigung schließen, indem sie die [**CloseHandle-Funktion**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) aufruft.

> [!Note]
>
> Ein E/A-Vervollständigungsport ist dem Prozess zugeordnet, von dem er erstellt wurde, und kann zwischen Prozessen nicht sharable werden. Ein einzelnes Handle kann jedoch zwischen Threads im gleichen Prozess zwischen zwei Threads verwendet werden.

 

## <a name="threads-and-concurrency"></a>Threads und Parallelität

Die wichtigste Eigenschaft eines E/A-Abschlussports, der sorgfältig zu berücksichtigen ist, ist der Parallelitätswert. Der Parallelitätswert eines Vervollständigungsport wird angegeben, wenn er mit [**CreateIoCompletionPort über**](createiocompletionport.md) den *NumberOfConcurrentThreads-Parameter erstellt* wird. Dieser Wert schränkt die Anzahl der ausführungsfähige Threads ein, die dem Abschlussport zugeordnet sind. Wenn die Gesamtzahl der dem Abschlussport zugeordneten ausführungsfähige Threads den Parallelitätswert erreicht, blockiert das System die Ausführung aller nachfolgenden Threads, die diesem Vervollständigungsport zugeordnet sind, bis die Anzahl der ausführungsfähige Threads unter den Parallelitätswert fällt.

Das effizienteste Szenario tritt auf, wenn Vervollständigungspakete in der Warteschlange warten, aber keine Warteschleifen erfüllt werden können, da der Port das Parallelitätslimit erreicht hat. Überlegen Sie, was mit einem Parallelitätswert von einem und mehreren Threads geschieht, die auf den [**GetQueuedCompletionStatus-Funktionsaufruf**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) warten. In diesem Fall wird die Ausführung nicht blockiert, wenn in der Warteschlange immer Abschlusspakete warten, wenn der ausgeführte Thread **GetQueuedCompletionStatus** aufruft, da die Threadwarteschlange, wie bereits erwähnt, LIFO ist. Stattdessen nimmt dieser Thread sofort das nächste Vervollständigungspaket in der Warteschlange auf. Es treten keine Threadkontextwechsel auf, da der ausgeführte Thread fortlaufend Vervollständigungspakete aufsammelt und die anderen Threads nicht ausgeführt werden können.

> [!Note]
>
> Im vorherigen Beispiel scheinen die zusätzlichen Threads unbnädig zu sein und nie ausgeführt zu werden. Dabei wird jedoch davon ausgegangen, dass der ausgeführte Thread nie durch einen anderen Mechanismus in einen Wartezustand gerät, den zugehörigen E/A-Abschlussport beendet oder anderweitig schließt. Berücksichtigen Sie beim Entwerfen der Anwendung alle Auswirkungen auf die Threadausführung.

 

Der beste maximal zulässige Wert für den Parallelitätswert ist die Anzahl der CPUs auf dem Computer. Wenn ihre Transaktion eine langwierige Berechnung erfordert, ermöglicht ein größerer Parallelitätswert die Ausführung von mehr Threads. Die Beendigung jedes Vervollständigungspakets kann länger dauern, aber es werden mehr Vervollständigungspakete gleichzeitig verarbeitet. Sie können mit dem Parallelitätswert in Verbindung mit Profilerstellungstools experimentieren, um die beste Wirkung für Ihre Anwendung zu erzielen.

Das System ermöglicht auch, dass ein Thread, der in [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) wartet, ein Vervollständigungspaket verarbeiten kann, wenn ein anderer ausgeführter Thread, der dem gleichen E/A-Abschlussport zugeordnet ist, aus anderen Gründen in den Wartezustand eintritt, z. B. die [**SuspendThread-Funktion.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread) Wenn der Thread im Wartezustand erneut ausgeführt wird, kann es einen kurzen Zeitraum geben, in dem die Anzahl der aktiven Threads den Parallelitätswert überschreitet. Das System verringert diese Anzahl jedoch schnell, indem es keine neuen aktiven Threads zu lässt, bis die Anzahl der aktiven Threads unter den Parallelitätswert fällt. Dies ist ein Grund dafür, dass Ihre Anwendung mehr Threads im Threadpool erstellt als der Parallelitätswert. Die Threadpoolverwaltung geht über den Rahmen dieses Themas hinaus, aber eine gute Faustregel ist, mindestens doppelt so viele Threads im Threadpool zu haben wie Prozessoren im System. Weitere Informationen zum Threadpooling finden Sie unter [Threadpools](/windows/desktop/ProcThread/thread-pools).

## <a name="supported-io-functions"></a>Unterstützte E/A-Funktionen

Die folgenden Funktionen können verwendet werden, um E/A-Vorgänge zu starten, die mithilfe von E/A-Vervollständigungsports abgeschlossen werden. Sie müssen der Funktion eine Instanz der [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) und ein Dateihandle übergeben, die zuvor einem E/A-Vervollständigungsport zugeordnet waren (durch einen Aufruf von [**CreateIoCompletionPort),**](createiocompletionport.md)um den E/A-Vervollständigungsportmechanismus zu aktivieren:

-   [**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
-   [**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
-   [**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
-   [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
-   [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
-   [**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
-   [**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
-   [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
-   [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
-   [**WSASendTo**](/windows/desktop/api/winsock2/nf-winsock2-wsasendto)
-   [**WSASend**](/windows/desktop/api/winsock2/nf-winsock2-wsasend)
-   [**WSARecvFrom**](/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom)
-   [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
-   [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>


</dt> <dt>

[About Processes and Threads (Informationen zu Prozessen und Threads)](/windows/desktop/ProcThread/about-processes-and-threads)
</dt> <dt>

[**BindIoCompletionCallback**](/windows/desktop/api/winbase/nf-winbase-bindiocompletioncallback)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> </dl>

 

 
