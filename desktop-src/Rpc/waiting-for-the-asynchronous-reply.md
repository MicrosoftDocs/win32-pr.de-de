---
title: Warten auf die asynchrone Antwort
description: Welche Aktionen der Client durchführt, während er darauf wartet, dass eine Antwort vom Server benachrichtigt wird, hängt vom ausgewählten Benachrichtigungs Mechanismus ab.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- Remote Prozedur Aufruf RPC, Tasks, warten auf asynchrone Antworten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0890b3024a05bb704f7b5a803c4b1e517c65ee21
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315885"
---
# <a name="waiting-for-the-asynchronous-reply"></a>Warten auf die asynchrone Antwort

Welche Aktionen der Client durchführt, während er darauf wartet, dass eine Antwort vom Server benachrichtigt wird, hängt vom ausgewählten Benachrichtigungs Mechanismus ab.

Wenn der Client ein Ereignis für die Benachrichtigung verwendet, wird in der Regel die [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion oder die [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) -Funktion aufgerufen. Der Client wechselt in einen blockierten Zustand, wenn er eine dieser Funktionen aufruft. Dies ist effizient, da der Client keine CPU-Lauf Zyklen beansprucht, während er blockiert ist.

Wenn Abruf verwendet wird, um auf seine Ergebnisse zu warten, wechselt das Client Programm in eine Schleife, die die Funktion [**rpcasyncgetcallstatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus)wiederholt aufruft. Dies ist eine effiziente Methode, um zu warten, ob das Client Programm in der Abruf Schleife eine andere Verarbeitung durchführt. Beispielsweise kann die Daten in kleinen Blöcken für einen nachfolgenden asynchronen Remote Prozedur Aufrufvorgang vorbereitet werden. Nachdem jeder Block abgeschlossen ist, kann der Client den ausstehenden asynchronen Remote Prozedur Aufrufs Abfragen, um zu prüfen, ob er abgeschlossen ist.

Das Client Programm kann einen asynchronen Prozedur Aufruf (APC) bereitstellen, bei dem es sich um eine Rückruffunktion handelt, die von der RPC-Lauf Zeit Bibliothek beim Abschluss des asynchronen Remote Prozedur Aufrufs aufgerufen wird. Ihr Client Programm muss den Wartezustand "Warnung" aufweisen. Dies bedeutet in der Regel, dass der Client eine Windows-API-Funktion aufruft, um sich in einen blockierten Zustand zu versetzen. Weitere Informationen finden Sie unter [asynchrone Prozedur Aufrufe](/windows/desktop/Sync/asynchronous-procedure-calls).

> [!Note]  
> Die Benachrichtigung über den Abschluss wird von einer asynchronen RPC-Routine nicht zurückgegeben, wenn während eines asynchronen Aufrufs eine RPC-Ausnahme ausgelöst wird.

 

Wenn Ihr Client Programm einen e/a-Abschlussport verwendet, um Abschluss Benachrichtigungen zu empfangen, muss er die [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion aufrufen. Wenn dies der Fall ist, kann es entweder unbegrenzt auf eine Antwort warten oder die andere Verarbeitung fortsetzen. Wenn beim Warten auf eine Antwort andere Verarbeitungsvorgänge durchführt, muss der Abschlussport mit der **GetQueuedCompletionStatus** -Funktion abgefragt werden. In diesem Fall muss die *dwMilliseconds* in der Regel auf NULL festgelegt werden. Dies bewirkt, dass **GetQueuedCompletionStatus** sofort zurückgegeben wird, auch wenn der asynchrone-Befehl nicht abgeschlossen wurde.

Client Programme können auch eine Vervollständigungs Benachrichtigung über die Fenster Nachrichten Warteschlangen empfangen. In diesem Fall wird die Abschluss Nachricht einfach wie jede beliebige Windows-Nachricht verarbeitet.

In einer Multithreadanwendung kann ein asynchroner-Rückruf nur vom Client abgebrochen werden, nachdem der Thread, der den-Befehl ausgelöst hat, erfolgreich vom-Befehl zurückgegeben wurde. Dadurch wird sichergestellt, dass der-Vorgang nicht asynchron von einem anderen Thread abgebrochen wird, nachdem er einen synchronen-Befehl nicht Als Standardübung sollte ein asynchroner Rückruf, der synchron fehlschlägt, nicht asynchron abgebrochen werden. Die Client Anwendung muss dieses Verhalten beobachten, wenn Aufrufe für verschiedene Threads ausgegeben und abgebrochen werden können. Nachdem der-Befehl abgebrochen wurde, muss der Client Code außerdem auf die Abschluss Benachrichtigung warten und den-Vorgang abschließen. Die Funktion [**rpcasynccancelcallruft**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) einfach die Abschluss Benachrichtigung auf. Es ist kein Ersatz für den Abschluss des Aufrufes.

Das folgende Code Fragment veranschaulicht, wie ein-Client Programm ein Ereignis verwenden kann, um auf eine asynchrone Antwort zu warten.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



Client Programme, die eine APC zum Empfangen von Benachrichtigungen über eine asynchrone Antwort verwenden, versetzen sich in der Regel in einen blockierten Zustand. Dies wird im folgenden Code Fragment veranschaulicht.


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



In diesem Fall wechselt das Client Programm in den Standbymodus und beansprucht keine CPU-Zyklen, bis die RPC-Lauf Zeit Bibliothek das APC aufruft (nicht angezeigt).

Das nächste Beispiel zeigt einen Client, der einen e/a-Abschlussport verwendet, um auf eine asynchrone Antwort zu warten.


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



Im vorherigen Beispiel wartet der [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Aufrufe unbegrenzt, bis der asynchrone Remote Prozedur Aufrufvorgang abgeschlossen ist.

Beim Schreiben von Multithreadanwendungen kommt es zu einem möglichen Problem. Wenn ein Thread einen Remote Prozedur Aufruf aufruft und dann beendet wird, bevor er benachrichtigt wird, dass der Sendevorgang abgeschlossen ist, kann der Remote Prozedur Aufruf fehlschlagen, und der Client-Stub kann die Verbindung mit dem Server schließen. Daher sollten Threads, die eine Remote Prozedur aufzurufen, nicht beendet werden, bevor der-Rückruf abgeschlossen oder abgebrochen wird, wenn das Verhalten nicht erwünscht ist.

 

 