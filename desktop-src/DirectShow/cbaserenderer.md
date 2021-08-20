---
description: Die CBaseRenderer-Klasse ist eine Basisklasse zum Implementieren von Rendererfiltern.
ms.assetid: 8d39d3bd-6162-402e-a4b3-0f35d3e29b96
title: CBaseRenderer-Klasse (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81e529493bfd892607748423bb1bab9016eb232aaeb3ed22287fa2c1c1917687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954804"
---
# <a name="cbaserenderer-class"></a>CBaseRenderer-Klasse

![cbaserenderer-Klassenhierarchie](images/rbase02.png)

Die `CBaseRenderer` -Klasse ist eine Basisklasse zum Implementieren von Rendererfiltern. Es unterstützt einen Eingabepin, der von der [**CRendererInputPin-Klasse**](crendererinputpin.md) implementiert wird. Um diese Klasse zu verwenden, deklarieren Sie eine abgeleitete Klasse, die `CBaseRenderer` erbt. Die abgeleitete Klasse muss mindestens die folgenden Methoden implementieren, die in der Basisklasse als rein virtuell deklariert sind:

-   [**CBaseRenderer::CheckMediaType:**](cbaserenderer-checkmediatype.md)Akzeptiert vorgeschlagene Medientypen oder lehnt sie ab. Der Filter ruft diese Methode während des Pinverbindungsprozesses auf.
-   [**CBaseRenderer::D oRenderSample:**](cbaserenderer-dorendersample.md)Rendert ein Beispiel. Der Filter ruft diese Methode für jedes Beispiel auf, das während der Ausführung empfangen wird.

Die Basisklasse behandelt Zustandsänderungen und Synchronisierungsprobleme. Außerdem werden Beispiele für das Rendering geplant, obwohl keine Qualitätskontrollmaßnahmen implementiert werden. Die Basisklasse deklariert auch mehrere Handlermethoden. Dies sind Methoden, die der Filter an bestimmten Punkten im Streamingprozess aufruft. Sie tun nichts in der Basisklasse, aber die abgeleitete Klasse kann sie überschreiben. In der folgenden Tabelle sind sie unter der Überschrift Öffentliche Methoden: Handler aufgeführt.

Der [**CBaseRenderer::OnReceiveFirstSample-Handler**](cbaserenderer-onreceivefirstsample.md) ist eine besondere Erwähnung. Der Filter ruft diese Methode auf, wenn er ein Beispiel empfängt, während der Filter angehalten wird. Dies kann auftreten, wenn das Diagramm von angehalten in angehalten wechselt oder wenn das Diagramm während der Pause gesucht wird. Videorenderer verwenden das Beispiel in der Regel, um einen Stillframe anzuzeigen. Wenn der Filter von angehalten in ausgeführt wechselt, sendet er das gleiche Beispiel an die [**CBaseRenderer::D oRenderSample-Methode,**](cbaserenderer-dorendersample.md) wie das erste Beispiel im Stream.

Die `CBaseRenderer` -Klasse macht die **Schnittstellen IMediaSeeking** und **IMediaPosition** über das [**CRendererPosPassThru-Objekt**](crendererpospassthru.md) verfügbar. Er übergibt alle Suchanforderungen an den nächsten Filter upstream.

## <a name="scheduling"></a>Scheduling

Wenn der Upstreamfilter die [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) des Eingabepins aufruft, um ein Beispiel zu übermitteln, übergibt der Pin diesen Aufruf an die [**CBaseRenderer::Receive-Methode**](cbaserenderer-receive.md) des Filters. Der Filter löscht entweder das Beispiel, rendert es sofort oder plant es für das Rendering.

Wenn das Beispiel über keine Zeitstempel verfügt oder keine Referenzuhr verfügbar ist, rendert der Filter das Beispiel sofort. Andernfalls ruft der Filter die [**CBaseRenderer::ShouldDrawSampleNow-Methode**](cbaserenderer-shoulddrawsamplenow.md) auf, um zu bestimmen, was zu tun ist. Standardmäßig wird das Beispiel basierend auf den Zeitstempeln geplant. Die abgeleitete Klasse kann **ShouldDrawSampleNow** überschreiben, um die Qualitätskontrolle zu unterstützen.

Um ein Beispiel zu planen, ruft der Filter die [**IReferenceClock::AdviseTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) auf, die eine Empfehlungsanforderung erstellt. Die [**Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) wird dann bis zum geplanten Zeitpunkt oder bis zur Änderung des Filterzustands blockiert. Die Blockierung verhindert, dass der Upstreamfilter mehr Stichproben liefert, bis das aktuelle Beispiel gerendert wird.

Wenn der Upstreamfilter die [**IPin::EndOfStream-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) aufruft, um das Ende des Streams zu signalisieren, sendet der Filter ein [**EC \_ COMPLETE-Ereignis**](ec-complete.md) an den Filtergraph-Manager. Der Filter wartet vor dem Senden des Ereignisses auf die Beendigungszeit des aktuellen Beispiels.



| Geschützte Membervariablen                                                   | Beschreibung                                                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bAbort**](cbaserenderer-m-babort.md)                                  | Flag, das angibt, ob das Rendering beendet und weitere Beispiele abgelehnt werden sollen.                                                               |
| [**m \_ bEOS**](cbaserenderer-m-beos.md)                                      | Flag, das angibt, ob das Ende des Streams erreicht wurde.                                                                                  |
| [**m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md)                    | Flag, das angibt, ob der Filter das EC \_ COMPLETE-Ereignis gesendet hat.                                                               |
| [**m \_ bInReceive**](cbaserenderer-m-binreceive.md)                          | Flag, das angibt, ob der Filter einen **Empfangsaufruf** verarbeitet.                                                                |
| [**m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md)                  | Flag, das Neumalereignisse aktiviert oder deaktiviert.                                                                                           |
| [**m \_ bStreaming**](cbaserenderer-m-bstreaming.md)                          | Flag, das angibt, ob der Filter Daten streamt.                                                                               |
| [**m \_ dwAdvise**](cbaserenderer-m-dwadvise.md)                              | Bezeichner des Timerereignisses, das das Rendering plant.                                                                                 |
| [**m \_ EndOfStreamTimer**](cbaserenderer-m-endofstreamtimer.md)              | Timerereignisbezeichner zum Planen von EC \_ COMPLETE-Benachrichtigungen.                                                                      |
| [**m \_ evComplete**](cbaserenderer-m-evcomplete.md)                          | Das Ereignis, das signalisiert wird, wenn ein Zustandsübergang abgeschlossen ist.                                                                             |
| [**m \_ InterfaceLock**](cbaserenderer-m-interfacelock.md)                    | Filterzustandssperre.                                                                                                                      |
| [**m \_ ObjectCreationLock**](cbaserenderer-m-objectcreationlock.md)          | Sperren Sie , um die Erstellung von Objekten innerhalb des Filters zu schützen.                                                                              |
| [**m \_ pInputPin**](cbaserenderer-m-pinputpin.md)                            | Zeiger auf den Eingabepin des Filters.                                                                                                      |
| [**m \_ pMediaSample**](cbaserenderer-m-pmediasample.md)                      | Zeiger auf das aktuelle Medienbeispiel.                                                                                                    |
| [**m \_ pPosition**](cbaserenderer-m-pposition.md)                            | Hilfsobjekt zum Übergeben von Suchbefehlen upstream.                                                                                           |
| [**m \_ pQSink**](cbaserenderer-m-pqsink.md)                                  | Zeiger auf das Objekt, das Qualitätskontrollnachrichten empfängt.                                                                           |
| [**m \_ RendererLock**](cbaserenderer-m-rendererlock.md)                      | Streamingsperre.                                                                                                                         |
| [**m \_ RenderEvent**](cbaserenderer-m-renderevent.md)                        | Ereignis, das zum Planen des Renderings verwendet wird.                                                                                                       |
| [**m \_ SignalTime**](cbaserenderer-m-signaltime.md)                          | Beendigungszeit für das aktuelle Beispiel.                                                                                                        |
| [**m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md)                      | Ereignis, das zum Freigeben des Streamingthreads verwendet wird.                                                                                             |
| Öffentliche Methoden                                                               | Beschreibung                                                                                                                             |
| [**CancelNotification**](cbaserenderer-cancelnotification.md)               | Bricht das Zeitgeberereignis ab, das das Rendering plant. Virtuellen.                                                                              |
| [**CBaseRenderer**](cbaserenderer-cbaserenderer.md)                         | Konstruktormethode.                                                                                                                     |
| [**~CBaseRenderer**](cbaserenderer--cbaserenderer.md)                       | Destruktormethode.                                                                                                                      |
| [**GetMediaPositionInterface**](cbaserenderer-getmediapositioninterface.md) | Ruft die [**Schnittstellenzeiger IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) und [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) des Filters ab. Virtuellen. |
| [**GetPin**](cbaserenderer-getpin.md)                                       | Ruft eine Stecknadel ab. Virtuellen.                                                                                                               |
| [**GetPinCount**](cbaserenderer-getpincount.md)                             | Ruft die Anzahl der Pins ab. Virtuellen.                                                                                                  |
| [**GetSampleTimes**](cbaserenderer-getsampletimes.md)                       | Ruft die Zeitstempel aus einem Beispiel ab. Virtuellen.                                                                                       |
| [**OnDisplayChange**](cbaserenderer-ondisplaychange.md)                     | Sendet ein [**EC \_ DISPLAY \_ CHANGED-Ereignis**](ec-display-changed.md) an den Filtergraph-Manager.                                          |
| [**PrepareReceive**](cbaserenderer-preparereceive.md)                       | Bereitet das Rendern eines Beispiels vor. Virtuellen.                                                                                                   |
| [**Erhalten**](cbaserenderer-receive.md)                                     | Empfängt das nächste Medienbeispiel im Stream. Virtuellen.                                                                                  |
| [**erbringen**](cbaserenderer-render.md)                                       | Rendert ein Beispiel. Virtuellen.                                                                                                              |
| [**ScheduleSample**](cbaserenderer-schedulesample.md)                       | Hier wird ein Beispiel für das Rendering geplant. Virtuellen.                                                                                              |
| [**SendNotifyWindow**](cbaserenderer-sendnotifywindow.md)                   | Benachrichtigt den Upstreamfilter des Videofensterhandpunkts.                                                                                |
| [**SendRepaint**](cbaserenderer-sendrepaint.md)                             | Sendet ein Repaint-Ereignis an den Filterdiagramm-Manager.                                                                                      |
| [**SetMediaType**](cbaserenderer-setmediatype.md)                           | Wird aufgerufen, wenn der Medientyp des Pins festgelegt ist. Virtuellen.                                                                                       |
| [**SignalTimerFired**](cbaserenderer-signaltimerfired.md)                   | Löschen des Timerbezeichners, der zum Planen des Renderings verwendet wird.                                                                                 |
| [**SourceThreadCanWait**](cbaserenderer-sourcethreadcanwait.md)             | Enthält oder gibt den Streamingthread frei. Virtuellen.                                                                                        |
| [**WaitForReceiveToComplete**](cbaserenderer-waitforreceivetocomplete.md)   | Wartet, bis die [**CBaseRenderer::Receive-Methode**](cbaserenderer-receive.md) abgeschlossen ist.                                               |
| [**WaitForRenderTime**](cbaserenderer-waitforrendertime.md)                 | Wartet auf die Präsentationszeit des aktuellen Beispiels. Virtuellen.                                                                              |
| Öffentliche Methoden: Accessormethoden                                             | Beschreibung                                                                                                                             |
| [**ClearPendingSample**](cbaserenderer-clearpendingsample.md)               | Gibt das aktuelle Beispiel frei. Virtuellen.                                                                                                   |
| [**GetCurrentSample**](cbaserenderer-getcurrentsample.md)                   | Ruft das aktuelle Beispiel ab. Virtuellen.                                                                                                  |
| [**GetRealState**](cbaserenderer-getrealstate.md)                           | Ruft den Filterstatus ab.                                                                                                             |
| [**GetRenderEvent**](cbaserenderer-getrenderevent.md)                       | Ruft das Ereignis ab, das das Rendering geplant.                                                                                           |
| [**HaveCurrentSample**](cbaserenderer-havecurrentsample.md)                 | Bestimmt, ob der Filter über ein Beispiel verfügt. Virtuellen.                                                                                    |
| [**IsEndOfStream**](cbaserenderer-isendofstream.md)                         | Fragt ab, ob die Benachrichtigung zum Ende des Streams empfangen wurde.                                                                            |
| [**IsEndOfStreamDelivered**](cbaserenderer-isendofstreamdelivered.md)       | Fragt ab, ob das \_ EC COMPLETE-Ereignis an den Filterdiagramm-Manager übermittelt wurde.                                                  |
| [**IsStreaming**](cbaserenderer-isstreaming.md)                             | Fragt ab, ob der Filter Streamingdaten ist.                                                                                           |
| [**SetAbortSignal**](cbaserenderer-setabortsignal.md)                       | Legt ein Flag fest, das angibt, ob das Rendering stoppt und weitere Beispiele abgelehnt werden.                                                       |
| [**SetRepaintStatus**](cbaserenderer-setrepaintstatus.md)                   | Aktiviert oder deaktiviert Neupaintereignisse.                                                                                                     |
| Öffentliche Methoden: State-Change Methoden                                         | Beschreibung                                                                                                                             |
| [**Aktiv**](cbaserenderer-active.md)                                       | Wird aufgerufen, wenn der Zustand in "Angehalten" oder "Wird ausgeführt" umgeschaltet wird. Virtuellen.                                                                        |
| [**BeginFlush**](cbaserenderer-beginflush.md)                               | Startet einen Leerungsvorgang. Virtuellen.                                                                                                      |
| [**BreakConnect**](cbaserenderer-breakconnect.md)                           | Gibt den Eingabepin von einer Verbindung frei. Virtuellen.                                                                                      |
| [**CheckReady**](cbaserenderer-checkready.md)                               | Fragt ab, ob ein Zustandsübergang abgeschlossen ist.                                                                                         |
| [**CompleteConnect**](cbaserenderer-completeconnect.md)                     | Schließt die Verbindung des Eingabepins mit einem anderen Pin ab. Virtuellen.                                                                           |
| [**CompleteStateChange**](cbaserenderer-completestatechange.md)             | Bestimmt, ob ein Übergang in den angehaltenen Zustand abgeschlossen ist. Virtuellen.                                                               |
| [**EndFlush**](cbaserenderer-endflush.md)                                   | Beendet einen Leerungsvorgang. Virtuellen.                                                                                                        |
| [**Inaktiv**](cbaserenderer-inactive.md)                                   | Wird aufgerufen, wenn der Zustand in Beendet wechselt. Virtuellen.                                                                                  |
| [**NotReady**](cbaserenderer-notready.md)                                   | Signalisiert, dass ein Zustandsübergang noch nicht abgeschlossen ist.                                                                                    |
| [**Bereit**](cbaserenderer-ready.md)                                         | Signalisiert, dass ein Zustandsübergang abgeschlossen ist.                                                                                            |
| [**StartStreaming**](cbaserenderer-startstreaming.md)                       | Initiiert das Streaming, wenn der Filter in den Ausführungszustand wechselt. Virtuellen.                                                               |
| [**StopStreaming**](cbaserenderer-stopstreaming.md)                         | Hält das Streaming an, wenn der Filter aus dem Ausführungszustand wechselt. Virtuellen.                                                             |
| Öffentliche Methoden: End-of-Stream-Methoden                                        | Beschreibung                                                                                                                             |
| [**EndOfStream**](cbaserenderer-endofstream.md)                             | Benachrichtigt den Filter, dass der Eingabepin eine Benachrichtigung zum Streamende empfangen hat. Virtuellen.                                                 |
| [**NotifyEndOfStream**](cbaserenderer-notifyendofstream.md)                 | Veröffentlicht ein [**EC \_ COMPLETE-Ereignis**](ec-complete.md) an den Filtergraph-Manager.                                                         |
| [**ResetEndOfStream**](cbaserenderer-resetendofstream.md)                   | Setzt die Flags für das Ende des Streams zurück.                                                                                                         |
| [**ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)         | Bricht den Timer ab, der EC \_ COMPLETE-Benachrichtigungen geplant. Virtuellen.                                                                   |
| [**SendEndOfStream**](cbaserenderer-sendendofstream.md)                     | Wenn das Ende des Streams erreicht wurde, wird von ein EC \_ COMPLETE-Ereignis für den Filterdiagramm-Manager geplant. Virtuellen.                                    |
| [**Timercallback**](cbaserenderer-timercallback.md)                         | Rückrufmethode für das End-of-Stream-Timerereignis.                                                                                      |
| Öffentliche Methoden: Handler                                                     | Beschreibung                                                                                                                             |
| [**OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)           | Wird aufgerufen, wenn der Filter ein Beispiel empfängt, während er angehalten wurde. Virtuellen.                                                                         |
| [**OnRenderEnd**](cbaserenderer-onrenderend.md)                             | Wird aufgerufen, nachdem ein Beispiel gerendert wurde. Virtuellen.                                                                                             |
| [**OnRenderStart**](cbaserenderer-onrenderstart.md)                         | Wird aufgerufen, wenn das Rendering gestartet wird. Virtuellen.                                                                                       |
| [**OnStartStreaming**](cbaserenderer-onstartstreaming.md)                   | Wird aufgerufen, wenn der Filter mit dem Streaming beginnt. Virtuellen.                                                                                       |
| [**OnStopStreaming**](cbaserenderer-onstopstreaming.md)                     | Wird aufgerufen, wenn der Filter das Streaming beendet. Virtuellen.                                                                                        |
| [**OnWaitEnd**](cbaserenderer-onwaitend.md)                                 | Wird aufgerufen, wenn der Filter fertig ist und auf die Präsentationszeit eines Beispiels gewartet wird. Virtuellen.                                                       |
| [**OnWaitStart**](cbaserenderer-onwaitstart.md)                             | Wird aufgerufen, wenn der Filter beginnt, auf die Präsentationszeit eines Beispiels zu warten. Virtuellen.                                                        |
| [**PrepareRender**](cbaserenderer-preparerender.md)                         | Wird aufgerufen, bevor der Filter ein Beispiel rendert. Virtuellen.                                                                                     |
| [**ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)             | Bestimmt, wie ein Beispiel für das Rendering geplant ist. Virtuellen.                                                                            |
| Rein virtuelle Methoden                                                         | Beschreibung                                                                                                                             |
| [**CheckMediaType**](cbaserenderer-checkmediatype.md)                       | Bestimmt, ob der Filter einen bestimmten Medientyp akzeptiert.                                                                                 |
| [**DoRenderSample**](cbaserenderer-dorendersample.md)                       | Rendert ein Beispiel.                                                                                                                       |
| IMediaFilter-Methoden                                                         | Beschreibung                                                                                                                             |
| [**GetState**](cbaserenderer-getstate.md)                                   | Ruft den Zustand des Filters ab (wird ausgeführt, beendet oder angehalten).                                                                             |
| [**Anhalten**](cbaserenderer-pause.md)                                         | Hält den Filter an.                                                                                                                      |
| [**Ausführung**](cbaserenderer-run.md)                                             | Führt den Filter aus.                                                                                                                        |
| [**Stoppen**](cbaserenderer-stop.md)                                           | Beendet den Filter.                                                                                                                       |
| IBaseFilter-Methoden                                                          | Beschreibung                                                                                                                             |
| [**FindPin**](cbaserenderer-findpin.md)                                     | Ruft den Pin mit dem angegebenen Bezeichner ab.                                                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




