---
description: Die Klasse "camthread" ist eine abstrakte Klasse zum Verwalten von Arbeitsthreads.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: Camthread-Klasse (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368392"
---
# <a name="camthread-class"></a>Camthread-Klasse

Die- `CAMThread` Klasse ist eine abstrakte Klasse zum Verwalten von Arbeitsthreads.



| Geschützte Member-Variablen                                 | BESCHREIBUNG                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [**m \_ hThread**](camthread-m-hthread.md)                  | Handle für den Thread.                                                        |
| Öffentliche Element Variablen                                    | BESCHREIBUNG                                                                  |
| [**m \_ accesslock**](camthread-m-accesslock.md)            | Kritischer Abschnitt, der den Zugriff auf den Thread durch andere Threads sperrt. |
| [**m \_ workerlock**](camthread-m-workerlock.md)            | Kritischer Abschnitt, der die von Threads gemeinsam genutzten Daten sperrt.                       |
| Öffentliche Methoden                                             | BESCHREIBUNG                                                                  |
| [**Camthread**](camthread-camthread.md)                   | Konstruktormethode.                                                          |
| [**~ Camthread**](camthread--camthread.md)                | Dekonstruktormethode. Virtu.                                                  |
| [**Initialthumproc**](camthread-initialthreadproc.md)   | Ruft die ThreadProc-Methode auf, wenn der Thread erstellt wird.                      |
| [**Stelle**](camthread-create.md)                         | Erstellt den Thread.                                                          |
| [**Callworker**](camthread-callworker.md)                 | Signalisiert dem Thread eine Anforderung.                                           |
| [**Schließen**](camthread-close.md)                           | Wartet, bis der Thread beendet wird, und gibt dann seine Ressourcen frei.                   |
| [**Threadexists**](camthread-threadexists.md)             | Fragt ab, ob der Thread vorhanden ist.                                           |
| [**GetRequest**](camthread-getrequest.md)                 | Wartet auf die nächste Anforderung.                                                  |
| [**Check Request**](camthread-checkrequest.md)             | Überprüft, ob eine Anforderung vorhanden ist, ohne zu blockieren.                              |
| [**Antwort**](camthread-reply.md)                           | Antwortet auf eine Anforderung.                                                        |
| [**Getrequesthandle**](camthread-getrequesthandle.md)     | Ruft ein Handle für das Ereignis ab, das von der callworker-Methode signalisiert wird.           |
| [**Getrequestparam**](camthread-getrequestparam.md)       | Ruft die aktuelle Anforderung ab.                                                |
| [**Coinitializehelper**](camthread-coinitializehelper.md) | Ruft CoInitializeEx am Anfang des Threads auf.                             |
| Reine virtuelle Methoden                                       | BESCHREIBUNG                                                                  |
| [**ThreadProc**](camthread-threadproc.md)                 | Thread Prozedur.                                                            |



 

## <a name="remarks"></a>Bemerkungen

Diese Klasse stellt Methoden zum Erstellen eines Arbeits Thread, zum Übergeben von Anforderungen an den Thread und zum warten auf das Beenden des Threads bereit. Gehen Sie folgendermaßen vor, um diese Klasse zu verwenden:

-   Leiten Sie eine Klasse von ab, `CAMThread` und überschreiben Sie die reine virtuelle Methode " [**camthread:: ThreadProc**](camthread-threadproc.md)". Bei dieser Methode handelt es sich um die Thread Prozedur, die am Anfang des Threads aufgerufen wird.
-   Erstellen Sie in Ihrer Anwendung eine Instanz der abgeleiteten Klasse. Beim Erstellen des Objekts wird der Thread nicht erstellt. Um den Thread zu erstellen, rufen Sie die Methode " [**camthread:: Create**](camthread-create.md) " auf.
-   Rufen Sie die Methode " [**camthread:: callworker**](camthread-callworker.md) " auf, um Anforderungen an den Thread zu senden. Diese Methode nimmt einen DWORD-Parameter an, dessen Bedeutung von ihrer Klasse definiert wird. Die-Methode wird blockiert, bis der Thread antwortet (siehe unten).
-   Antworten Sie in ihrer Thread Prozedur auf Anforderungen, indem Sie entweder " [**camthread:: GetRequest**](camthread-getrequest.md) " oder " [**camthread:: CheckRequest**](camthread-checkrequest.md)" aufrufen. Die GetRequest-Methode blockiert, bis ein anderer Thread callworker aufruft. Die CheckRequest-Methode ist nicht blockierend, sodass der Thread bei asynchroner Arbeit auf neue Anforderungen prüfen kann.
-   Wenn der Thread eine Anforderung empfängt, rufen Sie " [**camthread:: Reply**](camthread-reply.md) " auf, um die Blockierung des aufrufenden Threads aufzulösen. Die Reply-Methode nimmt einen DWORD-Parameter an, der als Rückgabewert für callworker an den aufrufenden Thread übergeben wird.

Wenn Sie mit dem Thread abgeschlossen sind, können Sie die Methode " [**camthread:: Close**](camthread-close.md) " aufzurufen. Diese Methode wartet darauf, dass der Thread beendet wird, und schließt dann das Thread handle. Es ist sichergestellt, dass Ihre ThreadProc-Nachricht entweder eigenständig oder als Reaktion auf eine callworker-Anforderung beendet wird. Die dekonstruktormethode ruft auch Close auf.

Diese Schritte werden im folgenden Beispiel veranschaulicht:


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



In ihrer abgeleiteten Klasse können Sie auch Element Funktionen definieren, die die Parameter an callworker überprüfen. Das folgende Beispiel zeigt eine typische Vorgehensweise:


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



Die- `CAMThread` Klasse stellt zwei kritische Abschnitte als öffentliche Element Variablen bereit. Verwenden `CAMThread::m_AccessLock` Sie, um den Zugriff auf den Thread durch andere Threads zu sperren. (Beispielsweise enthalten die Methoden Create und callworker diese Sperre, um Vorgänge für den Thread zu serialisieren.) Verwenden Sie " [**camthread:: m \_ workerlock**](camthread-m-workerlock.md) ", um Daten zu sperren, die von Threads gemeinsam genutzt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




