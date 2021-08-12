---
description: Die KLASSE CABThread ist eine abstrakte Klasse zum Verwalten von Arbeitsthreads.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: CABThread-Klasse (Wxutil.h)
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
ms.openlocfilehash: ca7182ecc16cd873732b2d39d2659f42017f9e01c1308642af4b8cac7ff2a682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662113"
---
# <a name="camthread-class"></a>WEBCAMThread-Klasse

Die `CAMThread` -Klasse ist eine abstrakte Klasse zum Verwalten von Arbeitsthreads.



| Geschützte Membervariablen                                 | BESCHREIBUNG                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [**m \_ hThread**](camthread-m-hthread.md)                  | Handle für den Thread.                                                        |
| Öffentliche Membervariablen                                    | BESCHREIBUNG                                                                  |
| [**m \_ AccessLock**](camthread-m-accesslock.md)            | Kritischer Abschnitt, der verhindert, dass andere Threads auf den Thread zugreifen. |
| [**m \_ WorkerLock**](camthread-m-workerlock.md)            | Kritischer Abschnitt zum Sperren von Daten, die von Threads gemeinsam genutzt werden.                       |
| Öffentliche Methoden                                             | BESCHREIBUNG                                                                  |
| [**WEBCAMThread**](camthread-camthread.md)                   | Konstruktormethode.                                                          |
| [**~ WEBCAMThread**](camthread--camthread.md)                | Destruktormethode. Virtuellen.                                                  |
| [**InitialThreadProc**](camthread-initialthreadproc.md)   | Ruft die ThreadProc-Methode auf, wenn der Thread erstellt wird.                      |
| [**Erstellen**](camthread-create.md)                         | Erstellt den Thread.                                                          |
| [**CallWorker**](camthread-callworker.md)                 | Signalisiert dem Thread eine Anforderung.                                           |
| [**Schließen**](camthread-close.md)                           | Wartet, bis der Thread beendet wird, und gibt dann seine Ressourcen frei.                   |
| [**ThreadExists**](camthread-threadexists.md)             | Fragt ab, ob der Thread vorhanden ist.                                           |
| [**GetRequest**](camthread-getrequest.md)                 | Wartet auf die nächste Anforderung.                                                  |
| [**CheckRequest**](camthread-checkrequest.md)             | Überprüft, ob eine Anforderung vorhanden ist, ohne dass eine Blockierung erfolgt.                              |
| [**Antwort**](camthread-reply.md)                           | Antwortet auf eine Anforderung.                                                        |
| [**GetRequestHandle**](camthread-getrequesthandle.md)     | Ruft ein Handle für das Ereignis ab, das von der CallWorker-Methode signalisiert wird.           |
| [**GetRequestParam**](camthread-getrequestparam.md)       | Ruft die neueste Anforderung ab.                                                |
| [**CoInitializeHelper**](camthread-coinitializehelper.md) | Ruft CoInitializeEx am Anfang des Threads auf.                             |
| Reine virtuelle Methoden                                       | BESCHREIBUNG                                                                  |
| [**ThreadProc**](camthread-threadproc.md)                 | Threadprozedur.                                                            |



 

## <a name="remarks"></a>Hinweise

Diese Klasse stellt Methoden zum Erstellen eines Arbeitsthreads, zum Übergeben von Anforderungen an den Thread und zum Warten auf das Beenden des Threads bereit. Gehen Sie wie folgt vor, um diese Klasse zu verwenden:

-   Leiten Sie eine Klasse von `CAMThread` ab, und überschreiben Sie die reine virtuelle Methode [**MSIThread::ThreadProc**](camthread-threadproc.md). Diese Methode ist die Threadprozedur, die am Anfang des Threads aufgerufen wird.
-   Erstellen Sie in Ihrer Anwendung eine Instanz der abgeleiteten Klasse. Beim Erstellen des -Objekts wird der Thread nicht erstellt. Um den Thread zu erstellen, rufen Sie die [**METHODE TARThread::Create**](camthread-create.md) auf.
-   Um Anforderungen an den Thread zu senden, rufen Sie die [**METHODE TARThread::CallWorker**](camthread-callworker.md) auf. Diese Methode verwendet einen DWORD-Parameter, dessen Bedeutung von Ihrer -Klasse definiert wird. Die -Methode wird blockiert, bis der Thread antwortet (siehe unten).
-   Reagieren Sie in Ihrer Threadprozedur auf Anforderungen, indem Sie entweder [**"TARThread::GetRequest"**](camthread-getrequest.md) oder [**"WEBCAMThread::CheckRequest"**](camthread-checkrequest.md)aufrufen. Die GetRequest-Methode wird blockiert, bis ein anderer Thread CallWorker aufruft. Die CheckRequest-Methode ist nicht blockierend, wodurch der Thread bei asynchroner Arbeit auf neue Anforderungen überprüfen kann.
-   Wenn der Thread eine Anforderung empfängt, rufen Sie [**MITTHREAD::Reply**](camthread-reply.md) auf, um die Blockierung des aufrufenden Threads aufzuheben. Die Reply-Methode verwendet einen DWORD-Parameter, der als Rückgabewert für CallWorker an den aufrufenden Thread übergeben wird.

Wenn Sie mit dem Thread fertig sind, rufen Sie die [**METHODE TARThread::Close**](camthread-close.md) auf. Diese Methode wartet, bis der Thread beendet wird, und schließt dann das Threadhandle. Ihre ThreadProc-Nachricht muss garantiert beendet werden, entweder eigenständig oder als Antwort auf eine CallWorker-Anforderung. Die Destruktormethode ruft auch Close auf.

Im folgenden Beispiel werden diese Schritte veranschaulicht:


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



In ihrer abgeleiteten Klasse können Sie auch Memberfunktionen definieren, die die Parameter auf CallWorker überprüfen. Das folgende Beispiel zeigt eine typische Vorgehensweise:


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



Die `CAMThread` -Klasse stellt zwei kritische Abschnitte als öffentliche Membervariablen bereit. Verwenden Sie `CAMThread::m_AccessLock` , um den Thread daran zu hindern, von anderen Threads darauf zuzugreifen. (Beispielsweise halten die Create- und CallWorker-Methoden diese Sperre bei, um Vorgänge für den Thread zu serialisieren.) Verwenden Sie [**DEN \_ WORKERLOCK-Code VON THREADSThread::m,**](camthread-m-workerlock.md) um Daten zu sperren, die von Threads gemeinsam genutzt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




