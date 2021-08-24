---
description: Die COutputQueue-Klasse implementiert eine Warteschlange zum Übermitteln von Medienbeispielen.
ms.assetid: da35bdac-fdc2-4b38-8253-547a19213cce
title: COutputQueue-Klasse (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8911c7261af0bf2e140a551b0146b7764cd541368898e6d3905f5dee2eaa4c53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813435"
---
# <a name="coutputqueue-class"></a>COutputQueue-Klasse

![coutputqueue](images/oput01.png)

Die `COutputQueue` -Klasse implementiert eine Warteschlange zum Übermitteln von Medienbeispielen.

Diese Klasse ermöglicht einem Ausgabepin das asynchrone Übermitteln von Beispielen. Beispiele werden in einer Warteschlange platziert, und ein Arbeitsthread übermittelt sie an den Eingabepin. Die Warteschlange kann auch Steuernachrichten enthalten, die auf ein neues Segment, eine Benachrichtigung zum Ende des Streams oder einen Leerungsvorgang hinweisen.

Um diese Klasse zu verwenden, erstellen Sie ein **COutputQueue-Objekt** für jeden Ausgabepin im Filter. Geben Sie in der Konstruktormethode den Eingabepin an, der mit diesem Ausgabepin verbunden ist. Mit dieser Klasse ruft der Ausgabepin methoden nicht direkt auf dem Eingabepin auf. Stattdessen werden die entsprechenden Methoden in wie `COutputQueue` in der folgenden Tabelle dargestellt.



| Pin-Methode                                                            | COutputQueue-Methode                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)                           | [**BeginFlush**](coutputqueue-beginflush.md)           |
| [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)                               | [**EndFlush**](coutputqueue-endflush.md)               |
| [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)                         | [**Eos**](coutputqueue-eos.md)                         |
| [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)                           | [**NewSegment**](coutputqueue-newsegment.md)           |
| [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)                 | [**Erhalten**](coutputqueue-receive.md)                 |
| [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) | [**ReceiveMultiple**](coutputqueue-receivemultiple.md) |



 

Optional können Sie das -Objekt so konfigurieren, `COutputQueue` dass Stichproben synchron ohne Arbeitsthread übermittelt werden. Das -Objekt kann auch zur Laufzeit basierend auf den Merkmalen des Eingabepins entscheiden, ob ein Arbeitsthread verwendet werden soll. Weitere Informationen finden Sie unter [**COutputQueue::COutputQueue**](coutputqueue-coutputqueue.md).



| Geschützte Membervariablen                                   | Beschreibung                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**m \_ pPin**](coutputqueue-m-ppin.md)                       | Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins.                                               |
| [**m \_ pInputPin**](coutputqueue-m-pinputpin.md)             | Zeiger auf die [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) des Eingabepins.                               |
| [**m \_ bBatchExact**](coutputqueue-m-bbatchexact.md)         | Flag, das angibt, ob das Objekt Stichproben in genauen Batches übermittelt.                                |
| [**m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)           | Batchgröße.                                                                                              |
| [**\_m-Liste**](coutputqueue-m-list.md)                       | Medienbeispielwarteschlange.                                                                                      |
| [**m \_ hSem**](coutputqueue-m-hsem.md)                       | Handle für ein Semaphor, das vom Thread verwendet wird, um auf Stichproben zu warten.                                           |
| [**m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) | Das Ereignis, das signalisiert, wenn ein Leerungsvorgang abgeschlossen ist.                                                  |
| [**m \_ hThread**](coutputqueue-m-hthread.md)                 | Handle für den Arbeitsthread.                                                                             |
| [**m \_ ppSamples**](coutputqueue-m-ppsamples.md)             | Array von Beispielen der Größe [**COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).               |
| [**m \_ nBatched**](coutputqueue-m-nbatched.md)               | Anzahl von Stichproben, die derzeit in Batches verarbeitet werden und auf die Verarbeitung warten.                                             |
| [**m \_ lWaiting**](coutputqueue-m-lwaiting.md)               | Flag mit einem Wert ungleich 0 (null), wenn der Thread auf ein Beispiel wartet.                                   |
| [**m \_ bFlushing**](coutputqueue-m-bflushing.md)             | Flag, das angibt, ob das Objekt einen Leerungsvorgang ausführt.                                  |
| [**m \_ bTerminate**](coutputqueue-m-bterminate.md)           | Flag, das angibt, ob der Thread beendet werden soll.                                                 |
| [**m \_ bSendAnyway**](coutputqueue-m-bsendanyway.md)         | Flag zum Überschreiben der Batchverarbeitung.                                                                       |
| [**m \_ std**](coutputqueue-m-hr.md)                           | **HRESULT-Wert,** der angibt, ob das Objekt Stichproben akzeptiert.                                 |
| [**m \_ hEventPop**](coutputqueue-m-heventpop.md)             | Ereignis, das signalisiert wird, wenn das Objekt ein Beispiel aus der Warteschlange entfernt.                              |
| Geschützte Methoden                                            | Beschreibung                                                                                              |
| [**InitialThreadProc**](coutputqueue-initialthreadproc.md)  | Ruft die [**COutputQueue::ThreadProc-Methode**](coutputqueue-threadproc.md) auf, wenn der Thread erstellt wird. |
| [**ThreadProc**](coutputqueue-threadproc.md)                | Ruft Beispiele aus der Warteschlange ab und übermittelt sie an den Eingabepin.                                     |
| [**IsQueued**](coutputqueue-isqueued.md)                    | Bestimmt, ob das Objekt einen Arbeitsthread zum Übermitteln von Beispielen verwendet.                               |
| [**QueueSample**](coutputqueue-queuesample.md)              | Reiht ein Medienbeispiel oder eine Steuernachricht in die Warteschlange ein.                                                                |
| [**IsSpecialSample**](coutputqueue-isspecialsample.md)      | Bestimmt, ob daten in der Warteschlange eine Steuernachricht sind.                                                     |
| [**FreeSamples**](coutputqueue-freesamples.md)              | Gibt alle ausstehenden Beispiele frei.                                                                               |
| [**NotifyThread**](coutputqueue-notifythread.md)            | Benachrichtigt den Thread, dass die Warteschlange Daten enthält.                                                        |
| Öffentliche Methoden                                               | Beschreibung                                                                                              |
| [**COutputQueue**](coutputqueue-coutputqueue.md)            | Konstruktormethode.                                                                                      |
| [**~COutputQueue**](coutputqueue--coutputqueue.md)          | Destruktormethode.                                                                                       |
| [**BeginFlush**](coutputqueue-beginflush.md)                | Startet einen Leerungsvorgang.                                                                                |
| [**EndFlush**](coutputqueue-endflush.md)                    | Beendet einen Leerungsvorgang.                                                                                  |
| [**Eos**](coutputqueue-eos.md)                              | Übermittelt einen End-of-Stream-Aufruf an den Eingabepin.                                                         |
| [**SendAnyway**](coutputqueue-sendanyway.md)                | Übermittelt alle ausstehenden Beispiele.                                                                            |
| [**NewSegment**](coutputqueue-newsegment.md)                | Übermittelt ein neues Segment an den Eingabepin.                                                                 |
| [**Erhalten**](coutputqueue-receive.md)                      | Übermittelt ein Medienbeispiel an den Eingabepin.                                                                |
| [**ReceiveMultiple**](coutputqueue-receivemultiple.md)      | Übermittelt einen Batch von Medienbeispielen an den Eingabepin.                                                      |
| [**Zurücksetzen**](coutputqueue-reset.md)                          | Setzt das Objekt zurück, damit es mehr Daten empfangen kann.                                                      |
| [**IsIdle**](coutputqueue-isidle.md)                        | Bestimmt, ob das Objekt auf Daten wartet.                                                       |
| [**SetPopEvent**](coutputqueue-setpopevent.md)              | Gibt ein Ereignis an, das signalisiert wird, wenn das -Objekt ein Beispiel aus der Warteschlange entfernt.                 |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




