---
title: Warten auf die asynchrone Antwort
description: Was der Client während der Benachrichtigung über eine Antwort vom Server tut, hängt vom ausgewählten Benachrichtigungsmechanismus ab.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- REMOTE PROCEDURE Call RPC , Tasks, Warten auf asynchrone Antworten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff50357402d96c32444f077d07558c01ed93d0367514e947643a28bf3041f204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010478"
---
# <a name="waiting-for-the-asynchronous-reply"></a>Warten auf die asynchrone Antwort

Was der Client während der Benachrichtigung über eine Antwort vom Server tut, hängt vom ausgewählten Benachrichtigungsmechanismus ab.

Wenn der Client ein Ereignis für die Benachrichtigung verwendet, wird in der Regel die [**WaitForSingleObject-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) oder die [**WaitForSingleObjectEx-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) aufrufen. Der Client geht in einen blockierten Zustand über, wenn er eine dieser Funktionen aufruft. Dies ist effizient, da der Client keine CPU-Ausführungszyklen verbraucht, während er blockiert ist.

Wenn das Clientprogramm abruft, um auf seine Ergebnisse zu warten, gibt es eine Schleife ein, die wiederholt die [**Funktion RpcAsyncGetCallStatus aufruft.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus) Dies ist eine effiziente Methode, um zu warten, ob Ihr Clientprogramm andere Verarbeitungen in der Abrufschleife vor sich hat. Beispielsweise können Daten in kleinen Blocken für einen nachfolgenden asynchronen Remoteprozeduraufruf vorbereitet werden. Nachdem jeder Block abgeschlossen ist, kann Der Client den ausstehenden asynchronen Remoteprozeduraufruf abrufen, um zu sehen, ob er abgeschlossen ist.

Ihr Clientprogramm kann einen asynchronen Prozeduraufruf (APC) bereitstellen. Dabei handelt es sich um eine Rückruffunktion, die von der RPC-Laufzeitbibliothek aufgerufen wird, wenn der asynchrone Remoteprozeduraufruf abgeschlossen ist. Ihr Clientprogramm muss sich in einem warnbaren Wartezustand befingen. Dies bedeutet in der Regel, dass der Client eine Windows-API-Funktion aufruft, um sich selbst in einen blockierten Zustand zu bringen. Weitere Informationen finden Sie unter [Asynchrone Prozeduraufrufe.](/windows/desktop/Sync/asynchronous-procedure-calls)

> [!Note]  
> Die Benachrichtigung über den Abschluss wird nicht von einer asynchronen RPC-Routine zurückgegeben, wenn während eines asynchronen Aufrufs eine RPC-Ausnahme ausgelöst wird.

 

Wenn Ihr Clientprogramm einen E/A-Abschlussport zum Empfangen von Abschlussbenachrichtigungen verwendet, muss es die [**GetQueuedCompletionStatus-Funktion**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) aufrufen. Wenn dies der Prozess ist, kann er entweder unbegrenzt auf eine Antwort warten oder andere Verarbeitungen fortsetzen. Wenn eine andere Verarbeitung erfolgt, während auf eine Antwort gewartet wird, muss der Abschlussport mit der **GetQueuedCompletionStatus-Funktion abruft** werden. In diesem Fall muss *dwMilliseconds* in der Regel auf 0 (null) festgelegt werden. Dies **bewirkt, dass GetQueuedCompletionStatus** sofort zurückkommt, auch wenn der asynchrone Aufruf nicht abgeschlossen wurde.

Clientprogramme können auch Abschlussbenachrichtigungen über ihre Fensternachrichtenwarteschlangen empfangen. In diesem Fall verarbeiten sie einfach die Abschlussmeldung wie jede andere Windows Nachricht.

In einer Multithreadanwendung kann ein asynchroner Aufruf vom Client nur abgebrochen werden, nachdem der Thread, von dem der Aufruf stammt, erfolgreich vom Aufruf zurückgegeben wurde. Dadurch wird sichergestellt, dass der Aufruf nicht asynchron von einem anderen Thread abgebrochen wird, nachdem ein synchroner Aufruf fehlgeschlagen ist. Standardmäßig sollte ein asynchroner Aufruf, der synchron fehlschlägt, nicht asynchron abgebrochen werden. Die Clientanwendung muss dieses Verhalten beobachten, wenn Aufrufe in verschiedenen Threads ausgegeben und abgebrochen werden können. Außerdem muss der Clientcode nach dem Abbrechen des Aufrufs auf die Abschlussbenachrichtigung warten und den Aufruf abschließen. Die [**RpcAsyncCancelCall-Funktion**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) überlastet einfach die Abschlussbenachrichtigung. es ist kein Ersatz für die Durchführung des Aufrufs.

Das folgende Codefragment veranschaulicht, wie ein Clientprogramm ein Ereignis verwenden kann, um auf eine asynchrone Antwort zu warten.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



Clientprogramme, die einen APC zum Empfangen von Benachrichtigungen über eine asynchrone Antwort verwenden, setzen sich in der Regel selbst in einen blockierten Zustand. Dies wird im folgenden Codefragment veranschaulicht.


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



In diesem Fall geht das Clientprogramm in den Ruhezustand und verbraucht keine CPU-Zyklen, bis die RPC-Laufzeitbibliothek den APC aufruft (nicht gezeigt).

Im nächsten Beispiel wird ein Client veranschaulicht, der einen E/A-Abschlussport verwendet, um auf eine asynchrone Antwort zu warten.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (!GetQueuedCompletionStatus(
         Async.u.IOC.hIOPort,
         &Async.u.IOC.dwNumberOfBytesTransferred,
         &Async.u.IOC.dwCompletionKey,
         &Async.u.IOC.lpOverlapped,
         INFINITE))
{
    RpcRaiseException(APP_ERROR);
}
```



Im vorherigen Beispiel wartet der Aufruf von [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) unbegrenzt, bis der asynchrone Remoteprozeduraufruf abgeschlossen ist.

Ein potenzieller Fehler tritt beim Schreiben von Multithreadanwendungen auf. Wenn ein Thread einen Remoteprozeduraufruf aufruft und dann beendet wird, bevor er eine Benachrichtigung empfängt, dass der Sendevorgang abgeschlossen wurde, kann der Remoteprozeduraufruf fehlschlagen, und der Clientstub kann die Verbindung mit dem Server schließen. Daher sollten Threads, die eine Remoteprozedur aufrufen, nicht beendet werden, bevor der Aufruf abgeschlossen oder abgebrochen wird, wenn das Verhalten unerwünscht ist.

 

 