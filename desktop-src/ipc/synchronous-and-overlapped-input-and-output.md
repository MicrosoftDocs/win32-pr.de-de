---
description: E/a-Vorgänge für synchrone Pipe und asynchrone Pipe-e/a. Die Funktionen ReadFile, Write File, transactnamedpipe und connectnamedpipe können Eingabe-und Ausgabe Vorgänge in einer Pipe entweder synchron oder asynchron ausführen.
ms.assetid: 5ab9bb7f-1f99-4041-bba8-2863f34dbcaf
title: Synchrone und überlappende Pipe-e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3becfb19dfe5fa49d4121246a576fb3200226b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352735"
---
# <a name="synchronous-and-overlapped-pipe-io"></a>Synchrone und überlappende Pipe-e/a

Die Funktionen [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile), [**transactnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)und [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) können Eingabe-und Ausgabe Vorgänge in einer Pipe entweder synchron oder asynchron ausführen. Wenn eine Funktion synchron ausgeführt wird, wird Sie erst zurückgegeben, wenn der ausgeführte Vorgang abgeschlossen ist. Dies bedeutet, dass die Ausführung des aufrufenden Threads für einen unbestimmten Zeitraum blockiert werden kann, während er darauf wartet, dass ein zeitaufwendiger Vorgang abgeschlossen wird. Wenn eine Funktion asynchron ausgeführt wird, wird Sie sofort zurückgegeben, auch wenn der Vorgang nicht abgeschlossen wurde. Dadurch kann ein zeitaufwändiger Vorgang im Hintergrund ausgeführt werden, während der aufrufende Thread kostenlos andere Aufgaben ausführen kann.

Durch die Verwendung asynchroner e/a kann ein Pipeserver eine Schleife verwenden, die die folgenden Schritte ausführt:

1.  Geben Sie mehrere Ereignis Objekte in einem Rückruf der wait-Funktion an, und warten Sie, bis eines der Objekte auf den signalisierten Zustand festgelegt ist.
2.  Verwenden Sie den Rückgabewert der wait-Funktion, um zu bestimmen, welcher überlappende Vorgang abgeschlossen wurde.
3.  Führen Sie die erforderlichen Aufgaben zum Bereinigen des abgeschlossenen Vorgangs aus, und initiieren Sie den nächsten Vorgang für dieses Pipehandle. Dies kann dazu führen, dass ein weiterer überlappende Vorgang für das gleiche Pipehandle gestartet wird.

Überlappende Vorgänge ermöglichen es einer Pipe, gleichzeitig Daten zu lesen und zu schreiben, und für einen einzelnen Thread, um gleichzeitige e/a-Vorgänge für mehrere Pipehandles auszuführen. Dies ermöglicht es einem Single Thread-Pipe-Server, die Kommunikation mit mehreren Pipe-Clients effizient zu verarbeiten. Ein Beispiel finden Sie unter [Named Pipe-Server mit über](named-pipe-server-using-overlapped-i-o.md)Lapp enden e/a-Vorgängen.

Damit ein Pipe-Server synchrone Vorgänge für die Kommunikation mit mehr als einem Client verwendet, muss für jeden Pipeclient ein separater Thread erstellt werden, damit ein oder mehrere Threads ausgeführt werden können, während andere Threads warten. Ein Beispiel für einen Multithread Pipe-Server, der synchrone Vorgänge verwendet, finden Sie unter [Multithread Pipe-Server](multithreaded-pipe-server.md).

## <a name="enabling-asynchronous-operation"></a>Aktivieren des asynchronen Vorgangs

Die Funktionen " [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)", " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)", " [**transactnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)" und " [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) " können nur dann asynchron ausgeführt werden, wenn Sie den überlappenden Modus für das angegebene Pipehandle aktivieren und einen gültigen Zeiger auf eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur angeben. Wenn der **über** Lapp Ende Zeiger **null** ist, kann der Rückgabewert der Funktion fälschlicherweise anzeigen, dass der Vorgang abgeschlossen wurde. Daher wird dringend empfohlen, dass Sie immer eine gültige überlappende Struktur angeben, wenn Sie ein Handle mit überlappenden \_ Dateiflag erstellen \_ und das asynchrone Verhalten wünschen. 

Das **hevent** -Element der angegebenen [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur muss ein Handle für ein Ereignis Objekt für manuelles Zurücksetzen enthalten. Hierbei handelt es sich um ein Synchronisierungs Objekt [**, das von der Funktion**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) "-Funktion Der Thread, der den überlappenden Vorgang initiiert, verwendet das Ereignis Objekt, um zu bestimmen, wann der Vorgang abgeschlossen wurde. Sie sollten das Pipehandle nicht für die Synchronisierung verwenden, wenn Sie gleichzeitige Vorgänge für denselben handle ausführen, da es keine Möglichkeit gibt, zu ermitteln, welcher Vorgang durchgeführt wurde, um den Pipehandle zu signalisieren. Die einzige zuverlässige Methode für die Ausführung gleichzeitiger Vorgänge auf demselben Pipehandle besteht darin, eine separate **über** Lapp Ende Struktur mit einem eigenen Ereignis Objekt für jeden Vorgang zu verwenden. Weitere Informationen zu Ereignis Objekten finden Sie unter [Synchronisierung](/windows/desktop/Sync/synchronization).

Außerdem können Sie benachrichtigt werden, wenn ein überlappende Vorgang mit den Funktionen [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) oder [**getqueuedcompletionstatusex**](/windows/desktop/FileIO/getqueuedcompletionstatusex-func) abgeschlossen wird. In diesem Fall müssen Sie das manuelle Zurücksetzungs Ereignis nicht in der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur zuweisen, und der Abschluss erfolgt mit dem Pipehandle auf die gleiche Weise wie ein asynchroner Lese-oder Schreibvorgang. Weitere Informationen finden Sie unter e [/a-Abschlussports](/windows/desktop/FileIO/i-o-completion-ports).

Bei der asynchronen Ausführung von [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)-, [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)-, [**transactnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)-und [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) -Vorgängen tritt Folgendes auf:

-   Wenn der Vorgang abgeschlossen ist, wenn die Funktion zurückgibt, gibt der Rückgabewert an, ob der Vorgang erfolgreich war oder fehlgeschlagen ist. Wenn ein Fehler auftritt, ist der Rückgabewert 0 (null), und die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt etwas anderes als Fehler-e/a steht \_ \_ aus.
-   Wenn der Vorgang nicht abgeschlossen ist, wenn die Funktion zurückgibt, ist der Rückgabewert 0 (null) und [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) gibt eine ausstehende Fehler-e/a zurück \_ \_ In diesem Fall muss der aufrufende Thread warten, bis der Vorgang abgeschlossen ist. Der aufrufende Thread muss dann die [**GetOverLappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) -Funktion aufrufen, um die Ergebnisse zu ermitteln.

## <a name="using-completion-routines"></a>Verwenden von Vervollständigungs Routinen

Die Funktionen "read [**fileex**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) " und " [**Write fileex**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) " bieten eine andere Form von überlappenden e/a-Vorgängen. Im Gegensatz zu den überlappenden Funktionen "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " und " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) ", die ein Ereignis Objekt verwenden, um den Abschluss zu signalisieren, geben die erweiterten Funktionen eine *Abschluss Routine* an. Eine Vervollständigungs Routine ist eine Funktion, die in die Warteschlange eingereiht wird, wenn der Lese-oder Schreibvorgang abgeschlossen ist. Die Vervollständigungs Routine wird erst ausgeführt, wenn der Thread, der "read **fileex** " und " **Write fileex** " aufgerufen hat, einen Warn *baren warte Vorgang* startet, indem eine der [wartetabellenwartefunktionen](/windows/desktop/Sync/wait-functions) aufgerufen wird, bei denen der Parameter " *falertable* " auf **true** Bei einem Warteschlangen-Wait-Vorgang geben die Funktionen auch dann zurück, wenn eine "Write **fileex** "-oder " **Write fileex** "-Abschluss Routine zur Ausführung in die Warteschlange Ein Pipeserver kann mithilfe der erweiterten Funktionen eine Sequenz von Lese-und Schreibvorgängen für jeden Client ausführen, der eine Verbindung mit dem Server herstellt. Jeder Lese-oder Schreibvorgang in der Sequenz gibt eine Abschluss Routine an, und jede Abschluss Routine initiiert den nächsten Schritt in der Sequenz. Ein Beispiel finden Sie unter [Named Pipe Server Using completion Routinen](named-pipe-server-using-completion-routines.md).

 

 
