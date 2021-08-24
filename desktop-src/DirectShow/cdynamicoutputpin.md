---
description: Die CDynamicOutputPin-Klasse implementiert einen Ausgabepin, der dynamische Verbindungswiederherstellungen und Formatänderungen unterstützt.
ms.assetid: d2488fba-a653-4b6e-b786-ce95f9e20daa
title: CDynamicOutputPin-Klasse (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e0b8903f83c372aa85bd1c41fb12ce9065798d79dc4dbd940df926a395f8bc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871800"
---
# <a name="cdynamicoutputpin-class"></a>CDynamicOutputPin-Klasse

Die `CDynamicOutputPin` -Klasse implementiert einen Ausgabepin, der dynamische Verbindungswiederherstellungen und Formatänderungen unterstützt.

Diese Klasse wird von der [**CBaseOutputPin-Klasse**](cbaseoutputpin.md) abgeleitet und implementiert die [**IPinFlowControl-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) Sie unterstützt mehrere Vorgänge, die für die dynamische Grapherstellung wichtig sind:

-   Dynamische wiederherzustellende Verbindung: Der Pin kann die Verbindung trennen und wiederherstellen, während der Filter noch aktiv ist (angehalten oder ausgeführt).
-   Dynamische Formatänderung: Der Pin kann einen neuen Medientyp aushandeln, während der Filter noch aktiv ist, ohne erneut eine Verbindung herzustellen.
-   Flow Steuerelement: Der besitzende Filter (oder eine Anwendung) kann den Datenfluss vom Pin blockieren, ohne den Filter zu beenden.

Weitere Informationen finden Sie unter [Dynamic Graph Building](dynamic-graph-building.md).

Die Stecknadel hat drei mögliche Zustände: blockiert, entsperrt und ausstehend. Im Status *Ausstehend* wartet die Stecknadel auf den Abschluss eines Vorgangs in einem anderen Thread, bevor der Pin in den blockierten Zustand wechselt. Während der Pin blockiert ist, kann der Filter keine Daten über den Pin übermitteln oder die Verbindung des Pins ändern.

Um zwischen mehreren Threads zu koordinieren, muss der besitzende Filter bestimmte Regeln befolgen. (Weitere Informationen zu Threads im Filterdiagramm finden Sie unter [Threads und kritische Abschnitte.)](threads-and-critical-sections.md) Zunächst muss der Streamingthread immer die [**CDynamicOutputPin::StartUsingOutputPin-Methode**](cdynamicoutputpin-startusingoutputpin.md) aufrufen, bevor eine der folgenden Methoden aufgerufen wird:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Anschließend muss die [**CDynamicOutputPin::StopUsingOutputPin-Methode**](cdynamicoutputpin-stopusingoutputpin.md) aufgerufen werden.

Zweitens darf der Anwendungsthread keine der Methoden in der vorherigen Liste aufrufen. Drittens darf der Streamingthread nicht die Klassenmethoden aufrufen, die den Pin blockieren oder entsperren. Diese Methoden sind: [**CDynamicOutputPin::Block,**](cdynamicoutputpin-block.md) [**CDynamicOutputPin::SynchronousBlockOutputPin,**](cdynamicoutputpin-synchronousblockoutputpin.md) [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)und [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md).

Diese Regeln stellen sicher, dass der Anwendungsthread den Pin nicht blockieren kann, während er vom Streamingthread verwendet wird (und umgekehrt). Nachdem der Streamingthread **StartUsingOutputPin** aufgerufen hat, wird der Pin erst blockiert, wenn der Streamingthread **StopUsingOutputPin aufruft.** Wenn der Pin dagegen blockiert ist, wartet **StartUsingOutputPin,** bis die Blockierung des Pins aufgehoben wurde.

Um zu vermeiden, dass Sie **StopUsingOutputPin** aufrufen, können Sie die [**CAutoUsingOutputPin-Klasse**](cautousingoutputpin-cautousingoutputpin.md) verwenden. **StopUsingOutputPin** wird automatisch aufruft, wenn es den Gültigkeitsbereich übergibt.

Wenn der besitzende Filter das Filterdiagramm (in der [**IBaseFilter::JoinFilterGraph-Methode)**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) joint oder verlässt, muss er die [**CDynamicOutputPin::SetConfigInfo-Methode**](cdynamicoutputpin-setconfiginfo.md) des Pins aufrufen.



| Geschützte Membervariablen                                                                      | Beschreibung                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md)                                 | Kritischer Abschnitt, der den Blockierungszustand schützt.                                                                            |
| [**m \_ hUnblockOutputPinEvent**](cdynamicoutputpin-m-hunblockoutputpinevent.md)                 | Ereignis, das signalisiert wird, wenn die Stecknadel nicht blockiert wird.                                                                           |
| [**m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)     | Ereignis, das signalisiert wird, wenn die Stecknadel erfolgreich blockiert wird oder der Benutzer einen ausstehenden Block abbricht.                                 |
| [**m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)                                         | Blockierungszustand.                                                                                                               |
| [**m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)                   | Der Bezeichner des Threads, der zuletzt die [**IPinFlowControl::Block-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) auf diesem Pin aufgerufen hat. |
| [**m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md) | Anzahl der Streamingthreads, die diesen Pin verwenden.                                                                                   |
| [**m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)                                         | Ereignis, das signalisiert wird, wenn der Filter beendet wird oder der Stecknadel Daten leert.                                                         |
| [**m \_ pGraphConfig**](cdynamicoutputpin-m-pgraphconfig.md)                                     | Zeiger auf die [**IGraphConfig-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) zum Ausführen dynamischer erneuter Verbindungsverknüpfungen.                           |
| [**m \_ bPinUsesReadOnlyAllocator**](cdynamicoutputpin-m-bpinusesreadonlyallocator.md)           | Flag, das angibt, ob Stichproben aus der Zuweisung des Pins schreibgeschützt sind.                                                   |
| Geschützte Methoden                                                                               | Beschreibung                                                                                                                   |
| [**SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)                | Blockiert die Stecknadel; gibt erst dann zurück, wenn die Stecknadel blockiert ist.                                                                     |
| [**AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)              | Blockiert die Stecknadel; gibt möglicherweise zurück, bevor die Stecknadel blockiert wird.                                                                       |
| [**UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)                                  | Entsperrt die Stecknadel.                                                                                                             |
| [**BlockOutputPin**](cdynamicoutputpin-blockoutputpin.md)                                      | Blockiert die Stecknadel.                                                                                                               |
| [**WaitEvent**](cdynamicoutputpin-waitevent.md)                                                | Wartet, bis das angegebene Ereignis signalisiert wird.                                                                                  |
| Öffentliche Methoden                                                                                  | Beschreibung                                                                                                                   |
| [**CDynamicOutputPin**](cdynamicoutputpin-cdynamicoutputpin.md)                                | Konstruktormethode.                                                                                                           |
| [**~CDynamicOutputPin**](cdynamicoutputpin--cdynamicoutputpin.md)                              | Destruktormethode.                                                                                                            |
| [**SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)                                        | Gibt den [**IGraphConfig-Zeiger**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) und das Beendigungsereignis an.                                                |
| [**DeliverBeginFlush**](cdynamicoutputpin-deliverbeginflush.md)                                | Fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu starten.                                                                  |
| [**DeliverEndFlush**](cdynamicoutputpin-deliverendflush.md)                                    | Fordert den verbundenen Eingabepin an, um einen Leerungsvorgang zu beenden.                                                                    |
| [**Inaktiv**](cdynamicoutputpin-inactive.md)                                                  | Benachrichtigt den Stecknadel, dass der Filter beendet wurde.                                                                                 |
| [**Aktiv**](cdynamicoutputpin-active.md)                                                      | Benachrichtigt den Pin, dass der Filter jetzt aktiv ist.                                                                               |
| [**CompleteConnect**](cdynamicoutputpin-completeconnect.md)                                    | Schließt eine Verbindung mit einem Eingabepin ab. Virtuellen.                                                                              |
| [**StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)                            | Ruft Zugriff auf die Stecknadel für einen Streamingvorgang ab. Virtuellen.                                                                 |
| [**StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)                              | Gibt den Zugriff auf den Pin nach einem Streamingvorgang frei. Virtuellen.                                                              |
| [**StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)        | Bestimmt, ob ein Thread einen Streamingvorgang für den Pin ausführt. Virtuellen.                                        |
| [**ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)                              | Ändert dynamisch den Medientyp für die Verbindung und übermittelt neue Segmentinformationen.                                  |
| [**ChangeMediaType**](cdynamicoutputpin-changemediatype.md)                                    | Ändert den Medientyp für die Verbindung dynamisch.                                                                        |
| [**DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)                                  | Führt eine dynamische wiederhergestellte Verbindung mit einem neuen Medientyp aus.                                                                        |
| IPin-Methoden                                                                                    | Beschreibung                                                                                                                   |
| [**Trennen**](cdynamicoutputpin-disconnect.md)                                              | Unterbricht die aktuelle Pinverbindung.                                                                                            |
| IPinFlowControl-Methoden                                                                         | Beschreibung                                                                                                                   |
| [**Block**](cdynamicoutputpin-block.md)                                                        | Blockiert oder entsperrt den Datenfluss vom Pin.                                                                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




