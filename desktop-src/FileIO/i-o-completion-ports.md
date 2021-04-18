---
description: E/a-Abschlussports stellen ein effizientes Threading Modell für die Verarbeitung mehrerer asynchroner e/a-Anforderungen auf einem Multiprozessorsystem dar.
ms.assetid: 213c48e8-bb21-43ed-9c00-2a5cf8ac25f0
title: E/a-Abschlussports
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 882363ef99821a0b0b40810f45d609c5b5f7760c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352306"
---
# <a name="io-completion-ports"></a>E/a-Abschlussports

E/a-Abschlussports stellen ein effizientes Threading Modell für die Verarbeitung mehrerer asynchroner e/a-Anforderungen auf einem Multiprozessorsystem dar. Wenn ein Prozess einen e/a-Abschlussport erstellt, erstellt das System ein zugeordnetes Warteschlangen Objekt für Anforderungen, deren einziger Zweck darin besteht, diese Anforderungen zu verarbeiten. Prozesse, die viele gleichzeitige asynchrone e/a-Anforderungen verarbeiten, können dies schneller und effizienter tun, indem Sie e/a-Abschlussports in Verbindung mit einem vorab zugeordneten Thread Pool verwenden, als indem Sie Threads zu dem Zeitpunkt erstellen, an dem Sie eine e/a-Anforderung erhalten.

## <a name="how-io-completion-ports-work"></a>Funktionsweise von e/a-Abschlussports

Die Funktion " [**deeieiocompletionport**](createiocompletionport.md) " erstellt einen e/a-Abschlussport und ordnet ein oder mehrere Datei Handles diesem Port zu. Wenn ein asynchroner e/a-Vorgang für einen dieser Datei Handles abgeschlossen ist, wird ein e/a-abschlusspaket in der FIFO-Reihenfolge (First-in-First-Out) an den zugeordneten e/a-Abschlussport in die Warteschlange eingereiht. Eine leistungsstarke Verwendung für diesen Mechanismus besteht darin, den Synchronisierungs Punkt für mehrere Datei Handles in einem einzelnen Objekt zu kombinieren, obwohl auch andere nützliche Anwendungen vorhanden sind. Beachten Sie, dass die Pakete zwar in der FIFO-Reihenfolge in die Warteschlange eingereiht werden, Sie werden jedoch möglicherweise in einer anderen Reihenfolge entfernt

> [!Note]
>
> Der hier verwendete Begriff " *Datei Handle* " bezieht sich auf eine System Abstraktion, die einen überlappenden e/a-Endpunkt darstellt, nicht nur eine Datei auf dem Datenträger. Beispielsweise kann es sich um einen Netzwerk Endpunkt, einen TCP-Socket, Named Pipe oder einen e-Mail-Slot handeln. Jedes Systemobjekt, das überlappende e/a unterstützt, kann verwendet werden. Eine Liste der zugehörigen e/a-Funktionen finden Sie am Ende dieses Themas.

 

Wenn ein Datei Handle einem Abschlussport zugeordnet ist, wird der Status Block nicht aktualisiert, bis das Paket aus dem Abschlussport entfernt wurde. Die einzige Ausnahme ist, wenn der ursprüngliche Vorgang synchron mit einem Fehler zurückgegeben wird. Ein Thread (entweder vom Haupt Thread oder dem Haupt Thread selbst erstellt) verwendet die [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion, um zu warten, bis ein abschlusspaket in die Warteschlange für den e/a-Abschlussport eingereiht wird, anstatt direkt auf den Abschluss der asynchronen e/a-Vorgänge zu warten. Threads, die ihre Ausführung an einem e/a-Abschlussport blockieren, werden in LIFO-Reihenfolge (Last-in-First-Out) freigegeben, und das nächste Vervollständigungs Paket wird aus der FIFO-Warteschlange des e/a-Abschluss Ports für diesen Thread abgerufen. Dies bedeutet, dass beim Freigeben eines Vervollständigungs Pakets in einem Thread das System den letzten (neuesten) Thread freigibt, der diesem Port zugeordnet ist, und ihm die Abschluss Informationen für den ältesten e/a-Abschluss übergibt.

Obwohl eine beliebige Anzahl von Threads [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) für einen angegebenen e/a-Abschlussport aufrufen kann, wenn ein angegebener Thread beim ersten Mal **GetQueuedCompletionStatus** aufruft, wird er dem angegebenen e/a-Abschlussport zugeordnet, bis eines von drei Dingen Eintritt Anders ausgedrückt: ein einzelner Thread kann höchstens einem e/a-Abschlussport zugeordnet werden.

Wenn ein Vervollständigungs Paket an einen e/a-Abschlussport eingereiht wird, prüft das System zunächst, wie viele Threads ausgeführt werden, die diesem Port zugeordnet sind. Wenn die Anzahl der ausgeführten Threads kleiner ist als der Parallelitäts Wert (im nächsten Abschnitt erläutert), ist einer der wartenden Threads (der aktuellste) für die Verarbeitung des Vervollständigungs Pakets zulässig. Wenn ein laufender Thread seine Verarbeitung abschließt, ruft er normalerweise erneut [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) auf. an diesem Punkt gibt er entweder mit dem nächsten Vervollständigungs Paket zurück oder wartet, wenn die Warteschlange leer ist.

Threads können die [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) -Funktion verwenden, um Vervollständigungs Pakete in der Warteschlange eines e/a-Abschlussports zu platzieren. Dadurch kann der Abschlussport zusätzlich zum Empfang von e/a-Abschluss Paketen vom e/a-System verwendet werden, um die Kommunikation von anderen Threads des Prozesses zu empfangen. Die Funktion " **PostQueuedCompletionStatus** " ermöglicht einer Anwendung, ihre eigenen speziellen Abschluss Pakete in die Warteschlange für den e/a-Abschlussport zu stellen, ohne einen asynchronen e/a-Vorgang zu starten. Dies ist beispielsweise hilfreich, um Arbeitsthreads externer Ereignisse zu benachrichtigen.

Der e/a-Abschluss Port Handle und jedes Datei Handle, das diesem bestimmten e/a-Abschlussport zugeordnet ist, werden als *Verweise auf den e/* a-Abschlussport bezeichnet. Der e/a-Abschlussport wird freigegeben, wenn keine Verweise mehr vorhanden sind. Daher müssen alle diese Handles ordnungsgemäß geschlossen werden, um den e/a-Abschlussport und seine zugeordneten Systemressourcen freizugeben. Nachdem diese Bedingungen erfüllt sind, sollte eine Anwendung den e/a-Abschluss Port handle schließen, indem Sie die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion aufrufen.

> [!Note]
>
> Es ist ein e/a-Abschlussport mit dem Prozess verknüpft, der ihn erstellt hat und der nicht zwischen Prozessen freigegeben werden kann. Ein einzelnes Handle kann jedoch zwischen Threads im gleichen Prozess freigegeben werden.

 

## <a name="threads-and-concurrency"></a>Threads und Parallelität

Die wichtigste Eigenschaft eines e/a-Abschlussports, der berücksichtigt werden muss, ist der Parallelitäts Wert. Der Parallelitäts Wert eines Abschlussports wird angegeben, wenn er mit " [**forateiocompletionport**](createiocompletionport.md) " über den Parameter " *numofconcurrentthreads* " erstellt wird. Dieser Wert schränkt die Anzahl der ausführbaren Threads ein, die dem Abschlussport zugeordnet sind. Wenn die Gesamtzahl der ausführbaren Threads, die dem Abschlussport zugeordnet sind, den Parallelitäts Wert erreicht, blockiert das System die Ausführung aller nachfolgenden Threads, die diesem Abschlussport zugeordnet sind, bis die Anzahl der ausführbaren Threads unter den Parallelitäts Wert fällt.

Das effizienteste Szenario tritt auf, wenn Abschluss Pakete in der Warteschlange warten, aber keine warte Vorgänge möglich sind, da der Port das Parallelitäts Limit erreicht hat. Beachten Sie, was mit einem Parallelitäts Wert von einem und mehreren Threads passiert, die auf den [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktions aufzurufen warten. Wenn in diesem Fall für die Warteschlange immer Abschluss Pakete gewartet werden, wenn der laufende Thread **GetQueuedCompletionStatus** aufruft, wird die Ausführung nicht blockiert, weil die Thread Warteschlange wie bereits erwähnt LIFO ist. Stattdessen übernimmt dieser Thread sofort das nächste ablaufschlangen-abschlusspaket. Es treten keine Thread Kontextwechsel auf, da der laufende Thread ständig Abschluss Pakete aufnimmt und die anderen Threads nicht ausgeführt werden können.

> [!Note]
>
> Im vorherigen Beispiel scheinen die zusätzlichen Threads nutzlos und nie ausgeführt zu werden. dabei wird jedoch davon ausgegangen, dass der laufende Thread nie von einem anderen Mechanismus in einen Wartezustand versetzt wird, beendet oder anderweitig den zugeordneten e/a-Abschlussport schließt. Beachten Sie beim Entwerfen der Anwendung alle Auswirkungen der Thread Ausführung.

 

Der beste maximale Gesamtwert für den Parallelitäts Wert ist die Anzahl der CPUs auf dem Computer. Wenn für die Transaktion eine lange Berechnung erforderlich ist, können durch einen größeren Parallelitäts Wert mehr Threads ausgeführt werden. Es dauert möglicherweise länger, bis das abschlusspaket abgeschlossen ist, aber es werden gleichzeitig weitere Abschluss Pakete verarbeitet. Sie können mit dem Parallelitäts Wert zusammen mit den Profil Erstellungs Tools experimentieren, um die bestmögliche Auswirkung für Ihre Anwendung zu erzielen.

Das System ermöglicht außerdem einem Thread, der auf [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) wartet, ein abschlusspaket zu verarbeiten, wenn ein anderer laufender Thread, der demselben e/a-Abschlussport zugeordnet ist, aus anderen Gründen in den Wartezustand wechselt, z. b. die [**SuspendThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-suspendthread) -Funktion Wenn der Thread im Wartezustand erneut ausgeführt wird, kann es zu einem kurzen Zeitpunkt kommen, wenn die Anzahl aktiver Threads den Parallelitäts Wert überschreitet. Das System reduziert diese Anzahl jedoch schnell, indem es keine neuen aktiven Threads zulässt, bis die Anzahl aktiver Threads unter den Parallelitäts Wert fällt. Dies ist ein Grund dafür, dass Ihre Anwendung mehr Threads im Thread Pool als der Parallelitäts Wert erstellt. Die Thread Pool Verwaltung geht über den Rahmen dieses Themas hinaus, aber eine gute Faustregel besteht darin, dass Sie mindestens doppelt so viele Threads im Thread Pool haben, wie Prozessoren auf dem System vorhanden sind. Weitere Informationen zum Thread Pooling finden Sie unter [Thread Pools](/windows/desktop/ProcThread/thread-pools).

## <a name="supported-io-functions"></a>Unterstützte e/a-Funktionen

Die folgenden Funktionen können verwendet werden, um e/a-Vorgänge zu starten, die mithilfe von e/a-Abschlussports abgeschlossen werden. Zum Aktivieren des e/a-Abschlussport-Mechanismus müssen Sie der Funktion eine Instanz der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur und ein Datei Handle übergeben, das zuvor mit einem e/a-Abschlussport (durch Aufrufen von " [**anateiocompletionport**](createiocompletionport.md)") verknüpft ist:

-   [**Connectnamedpipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
-   [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
-   [**Lockfileex**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
-   [**"Read directoriychangesw"**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
-   [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
-   [**Transactnamedpipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
-   [**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
-   [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
-   [**Wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
-   [**WSASendTo**](/windows/desktop/api/winsock2/nf-winsock2-wsasendto)
-   [**Wsasend**](/windows/desktop/api/winsock2/nf-winsock2-wsasend)
-   [**WSARecvFrom**](/windows/desktop/api/winsock2/nf-winsock2-wsarecvfrom)
-   [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
-   [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>


</dt> <dt>

[About Processes and Threads (Informationen zu Prozessen und Threads)](/windows/desktop/ProcThread/about-processes-and-threads)
</dt> <dt>

[**' Bindiocompletioncallback '**](/windows/desktop/api/winbase/nf-winbase-bindiocompletioncallback)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatus usex**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**' PostQueuedCompletionStatus '**](postqueuedcompletionstatus.md)
</dt> </dl>

 

 
