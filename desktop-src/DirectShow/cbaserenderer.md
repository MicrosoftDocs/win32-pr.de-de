---
description: Die cbaserenderer-Klasse ist eine Basisklasse zum Implementieren von rendererfiltern.
ms.assetid: 8d39d3bd-6162-402e-a4b3-0f35d3e29b96
title: Cbaserderderer-Klasse (renbase. h)
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
ms.openlocfilehash: e30bae52cf5a7eba642354d002173291cb7d38b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356404"
---
# <a name="cbaserenderer-class"></a>Cbaserderderer-Klasse

![cbaserenderer-Klassenhierarchie](images/rbase02.png)

Die- `CBaseRenderer` Klasse ist eine Basisklasse zum Implementieren von rendererfiltern. Sie unterstützt eine Eingabe-PIN, die von der [**crendererinputpin**](crendererinputpin.md) -Klasse implementiert wird. Um diese Klasse zu verwenden, deklarieren Sie eine abgeleitete Klasse, die erbt `CBaseRenderer` . Die abgeleitete Klasse muss mindestens die folgenden Methoden implementieren, die in der Basisklasse als rein virtuell deklariert werden:

-   [**Cbaserderderer:: checkmediatype**](cbaserenderer-checkmediatype.md): akzeptiert oder lehnt vorgeschlagene Medientypen ab. Der Filter ruft diese Methode während des PIN-Verbindungs Vorgangs auf.
-   [**Cbaserenderer::D orendersample**](cbaserenderer-dorendersample.md): rendert ein Beispiel. Der Filter ruft diese Methode für jedes bei der Ausführung empfangene Beispiel auf.

Die-Basisklasse verarbeitet Zustandsänderungen und Synchronisierungs Probleme. Außerdem werden Beispiele für das Rendering geplant, obwohl keine Qualitäts Steuerungsmaßnahmen implementiert werden. Die-Basisklasse deklariert auch mehrere "Handler"-Methoden. Dabei handelt es sich um Methoden, die der Filter an bestimmten Punkten im streamingprozess aufruft. Sie führen in der Basisklasse keine Aktionen aus, aber die abgeleitete Klasse kann Sie überschreiben. In der folgenden Tabelle werden Sie unter der Überschrift Public Methods: Handlers aufgeführt.

Der [**cbaserderderer:: onreceivefirstsample**](cbaserenderer-onreceivefirstsample.md) -Handler verdient besondere Erwähnung. Der Filter ruft diese Methode auf, wenn Sie eine Stichprobe empfängt, während der Filter angehalten wird. Dies kann vorkommen, wenn der Graph von "angehalten" zu "angehalten" wechselt oder wenn das Diagramm während des angehaltenen angezeigt wird. Videorenderer verwenden in der Regel das Beispiel, um einen noch immer Frame anzuzeigen. Wenn der Filter von "angehalten" in "wird ausgeführt" wechselt, sendet er dasselbe Beispiel an die [**cbaserenderer::D orendersample**](cbaserenderer-dorendersample.md) -Methode, wie das erste Beispiel im Stream.

Die `CBaseRenderer` -Klasse macht die Schnittstellen **imediaseeking** und **imediaposition** über das [**crendererpospassthru**](crendererpospassthru.md) -Objekt verfügbar. Alle Suchanforderungen werden an den nächsten Filter Upstream weitergeleitet.

## <a name="scheduling"></a>Scheduling

Wenn der upstreamfilter die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode der Eingabe-PIN aufruft, um ein Beispiel zu übermitteln, übergibt die PIN diesen Aufruf an die [**cbaserenderer:: Receive**](cbaserenderer-receive.md) -Methode des Filters. Der Filter löscht entweder das Beispiel, rendert es sofort oder plant es für das Rendering.

Wenn das Beispiel keine Zeitstempel aufweist oder wenn keine Referenzuhr verfügbar ist, rendert der Filter das Beispiel sofort. Andernfalls ruft der Filter die [**cbaserenderer:: denddrawsamplenow**](cbaserenderer-shoulddrawsamplenow.md) -Methode auf, um zu bestimmen, was zu tun ist. Standardmäßig wird das Beispiel basierend auf den Zeitstempeln geplant. Die abgeleitete Klasse kann " **schulddrawsamplenow** " zur Unterstützung der Qualitätskontrolle überschreiben.

Um ein Beispiel zu planen, ruft der Filter die [**IReferenceClock:: advisettime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) -Methode auf, die eine Request-Anforderung erstellt. Die [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode wird dann bis zum geplanten Zeitpunkt blockiert, oder bis der Status des Filters geändert wird. Die Blockierung verhindert, dass der upstreamfilter weitere Stichproben bereitstellt, bis das aktuelle Beispiel gerendert

Wenn der upstreamfilter die [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) -Methode aufruft, um das Ende des Streams zu signalisieren, sendet der Filter ein [**EC \_ Complete**](ec-complete.md) -Ereignis an den Filter Graph-Manager. Der Filter wartet auf die Endzeit des aktuellen Beispiels, bevor das Ereignis gesendet wird.



| Geschützte Member-Variablen                                                   | BESCHREIBUNG                                                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ babort**](cbaserenderer-m-babort.md)                                  | Flag, das angibt, ob das Rendering beendet und weitere Beispiele abgelehnt werden sollen.                                                               |
| [**Mio. \_ Betriebssysteme**](cbaserenderer-m-beos.md)                                      | Flag, das angibt, ob das Ende des Streams erreicht wurde.                                                                                  |
| [**m \_ BeOS übermittelt**](cbaserenderer-m-beosdelivered.md)                    | Flag, das angibt, ob der Filter das "EC Complete"-Ereignis gesendet hat \_ .                                                               |
| [**m- \_ binreceive**](cbaserenderer-m-binreceive.md)                          | Flag, das angibt, ob der Filter einen **Receive** -Befehl verarbeitet.                                                                |
| [**m \_ brepaintstatus**](cbaserenderer-m-brepaintstatus.md)                  | Flag, das Repaint-Ereignisse aktiviert oder deaktiviert.                                                                                           |
| [**m \_ bstreaming**](cbaserenderer-m-bstreaming.md)                          | Flag, das angibt, ob der Filterdaten Streamingdaten ist.                                                                               |
| [**m \_ DW-Empfehlung**](cbaserenderer-m-dwadvise.md)                              | Der Bezeichner des Zeit Geber Ereignisses, das das Rendering plant.                                                                                 |
| [**m \_ EndOf streamtimer**](cbaserenderer-m-endofstreamtimer.md)              | Timer-Ereignis Bezeichner für die Planung von "EC Complete"- \_ Benachrichtigungen.                                                                      |
| [**m. \_ evcomplete**](cbaserenderer-m-evcomplete.md)                          | Das Ereignis, das signalisiert wird, wenn ein Zustandsübergang beendet ist.                                                                             |
| [**m- \_ interfakelock**](cbaserenderer-m-interfacelock.md)                    | Filter-State-Sperre.                                                                                                                      |
| [**m \_ objectkreationlock**](cbaserenderer-m-objectcreationlock.md)          | Sperre zum Schutz der Erstellung von Objekten innerhalb des Filters.                                                                              |
| [**m \_ pinputpin**](cbaserenderer-m-pinputpin.md)                            | Zeiger auf die Eingabe-PIN des Filters.                                                                                                      |
| [**m \_ pmediasample**](cbaserenderer-m-pmediasample.md)                      | Zeiger auf das aktuelle Medien Beispiel.                                                                                                    |
| [**m \_ pposition**](cbaserenderer-m-pposition.md)                            | Hilfsobjekt, um Seek-Befehle zu übergeben.                                                                                           |
| [**m- \_ pqsink**](cbaserenderer-m-pqsink.md)                                  | Zeiger auf das-Objekt, das Qualitäts Steuerungs Meldungen empfängt.                                                                           |
| [**m \_ rendererlock**](cbaserenderer-m-rendererlock.md)                      | Streamingsperre.                                                                                                                         |
| [**m \_ renderevent**](cbaserenderer-m-renderevent.md)                        | Das Ereignis, mit dem das Rendering geplant wird.                                                                                                       |
| [**m \_ Signalzeit**](cbaserenderer-m-signaltime.md)                          | Endzeit für das aktuelle Beispiel.                                                                                                        |
| [**m \_ threadsignal**](cbaserenderer-m-threadsignal.md)                      | Ereignis, das verwendet wird, um den Streaminginhalte                                                                                             |
| Öffentliche Methoden                                                               | BESCHREIBUNG                                                                                                                             |
| [**Cancelnotification**](cbaserenderer-cancelnotification.md)               | Bricht das Timer-Ereignis ab, das das Rendering plant. Virtu.                                                                              |
| [**Cbaserererderer**](cbaserenderer-cbaserenderer.md)                         | Konstruktormethode.                                                                                                                     |
| [**~ Cbaserererderer**](cbaserenderer--cbaserenderer.md)                       | Dekonstruktormethode.                                                                                                                      |
| [**Getmediapositioninterface**](cbaserenderer-getmediapositioninterface.md) | Ruft die Schnittstellen Zeiger [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) und [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) des Filters ab. Virtu. |
| [**Getpin**](cbaserenderer-getpin.md)                                       | Ruft eine PIN ab. Virtu.                                                                                                               |
| [**Getpincount**](cbaserenderer-getpincount.md)                             | Ruft die Anzahl der Pins ab. Virtu.                                                                                                  |
| [**Getsampletimes**](cbaserenderer-getsampletimes.md)                       | Ruft die Zeitstempel aus einem Beispiel ab. Virtu.                                                                                       |
| [**Ondisplaychange**](cbaserenderer-ondisplaychange.md)                     | Sendet ein angezeigter [**EC- \_ Anzeige \_**](ec-display-changed.md) Ereignis an den Filter Diagramm-Manager.                                          |
| [**Preparereceive**](cbaserenderer-preparereceive.md)                       | Bereitet das Rendering eines Beispiels vor. Virtu.                                                                                                   |
| [**Medizinisch**](cbaserenderer-receive.md)                                     | Empfängt das nächste Medien Beispiel im Stream. Virtu.                                                                                  |
| [**Bieten**](cbaserenderer-render.md)                                       | Rendert ein Beispiel. Virtu.                                                                                                              |
| [**Schedulesample**](cbaserenderer-schedulesample.md)                       | Plant ein Beispiel für das Rendering. Virtu.                                                                                              |
| [**Sendnotifywindow**](cbaserenderer-sendnotifywindow.md)                   | Benachrichtigt den upstreamfilter über das Videofenster handle.                                                                                |
| [**Sendrepaint**](cbaserenderer-sendrepaint.md)                             | Sendet ein Repaint-Ereignis an den Filter Diagramm-Manager.                                                                                      |
| [**Setmediatype**](cbaserenderer-setmediatype.md)                           | Wird aufgerufen, wenn der Medientyp der PIN festgelegt wird. Virtu.                                                                                       |
| [**Signaltimerfired**](cbaserenderer-signaltimerfired.md)                   | Löscht den Zeit Geber Bezeichner, der zum Planen des Rendering verwendet wird                                                                                 |
| [**Sourcethreadcanwait**](cbaserenderer-sourcethreadcanwait.md)             | Hält den Streaminginhalt oder gibt diesen frei. Virtu.                                                                                        |
| [**Waitforreceivetocomplete**](cbaserenderer-waitforreceivetocomplete.md)   | Wartet, bis die [**cbaserdenderer:: Receive**](cbaserenderer-receive.md) -Methode beendet ist.                                               |
| [**Waitforrendertime**](cbaserenderer-waitforrendertime.md)                 | Wartet auf die Präsentationszeit des aktuellen Beispiels. Virtu.                                                                              |
| Öffentliche Methoden: Accessormethoden                                             | BESCHREIBUNG                                                                                                                             |
| [**Clearpdingsample**](cbaserenderer-clearpendingsample.md)               | Gibt das aktuelle Beispiel frei. Virtu.                                                                                                   |
| [**Getcurrentsample**](cbaserenderer-getcurrentsample.md)                   | Ruft das aktuelle Beispiel ab. Virtu.                                                                                                  |
| [**Getrealstate**](cbaserenderer-getrealstate.md)                           | Ruft den Filter Status ab.                                                                                                             |
| [**GetRenderEvent**](cbaserenderer-getrenderevent.md)                       | Ruft das Ereignis ab, das das Rendering plant.                                                                                           |
| [**Havecurrentsample**](cbaserenderer-havecurrentsample.md)                 | Bestimmt, ob der Filter über ein Beispiel verfügt. Virtu.                                                                                    |
| [**Isendof-Stream**](cbaserenderer-isendofstream.md)                         | Fragt ab, ob das Ende der Stream-Benachrichtigung empfangen wurde.                                                                            |
| [**Isendof streamzugestellt**](cbaserenderer-isendofstreamdelivered.md)       | Fragt ab, ob das EC \_ Complete-Ereignis an den Filter Graph-Manager übermittelt wurde.                                                  |
| [**Isstreaming**](cbaserenderer-isstreaming.md)                             | Fragt ab, ob der Filter Streamingdaten ist.                                                                                           |
| [**"Abtabortsignal"**](cbaserenderer-setabortsignal.md)                       | Legt ein Flag fest, das angibt, ob das Rendering beendet und weitere Beispiele abgelehnt werden sollen.                                                       |
| [**Status**](cbaserenderer-setrepaintstatus.md)                   | Aktiviert oder deaktiviert Repaint-Ereignisse.                                                                                                     |
| Öffentliche Methoden: State-Change Methoden                                         | BESCHREIBUNG                                                                                                                             |
| [**Aktiv**](cbaserenderer-active.md)                                       | Wird aufgerufen, wenn der Zustand zum Anhalten oder ausführen gewechselt wird. Virtu.                                                                        |
| [**Beginflush**](cbaserenderer-beginflush.md)                               | Startet einen Löschvorgang. Virtu.                                                                                                      |
| [**Breakconnect**](cbaserenderer-breakconnect.md)                           | Gibt die Eingabe-PIN von einer Verbindung frei. Virtu.                                                                                      |
| [**Prüfbereit**](cbaserenderer-checkready.md)                               | Fragt ab, ob ein Zustandsübergang beendet ist.                                                                                         |
| [**Completeconnect**](cbaserenderer-completeconnect.md)                     | Schließt die Verbindung der Eingabe-PIN mit einer anderen Pin ab. Virtu.                                                                           |
| [**Completestatechange**](cbaserenderer-completestatechange.md)             | Bestimmt, ob ein Übergang zum angehaltenen Zustand beendet ist. Virtu.                                                               |
| [**Endflush**](cbaserenderer-endflush.md)                                   | Beendet einen Löschvorgang. Virtu.                                                                                                        |
| [**Inaktiv**](cbaserenderer-inactive.md)                                   | Wird aufgerufen, wenn der Zustand in "beendet" versetzt wird. Virtu.                                                                                  |
| [**NotReady**](cbaserenderer-notready.md)                                   | Signalisiert, dass ein Zustandsübergang noch nicht beendet ist.                                                                                    |
| [**Bereit**](cbaserenderer-ready.md)                                         | Signalisiert, dass ein Zustandsübergang beendet ist.                                                                                            |
| [**Startstreaming**](cbaserenderer-startstreaming.md)                       | Initiiert das Streaming, wenn der Filter in den Zustand "wird ausgeführt" wechselt. Virtu.                                                               |
| [**Stopstreaming**](cbaserenderer-stopstreaming.md)                         | Stoppt das Streaming, wenn der Filter den Status "wird ausgeführt" verlässt. Virtu.                                                             |
| Öffentliche Methoden: End-of-Stream-Methoden                                        | BESCHREIBUNG                                                                                                                             |
| [**EndOfStream**](cbaserenderer-endofstream.md)                             | Benachrichtigt den Filter, dass die Eingabe-PIN eine Benachrichtigung über das Ende des Datenstroms erhalten hat. Virtu.                                                 |
| [**Notifyendof**](cbaserenderer-notifyendofstream.md)                 | Sendet ein Ereignis vom Typ " [**EC \_ Complete**](ec-complete.md) " an den Filter Graph-Manager.                                                         |
| [**Retsdof-Stream**](cbaserenderer-resetendofstream.md)                   | Setzt die Flags für das Ende des Streams zurück.                                                                                                         |
| [**Restitendof-Zeitgeber**](cbaserenderer-resetendofstreamtimer.md)         | Bricht den Timer ab, der die Ausführung von EC- \_ Benachrichtigungen plant. Virtu.                                                                   |
| [**Sendendof-Stream**](cbaserenderer-sendendofstream.md)                     | Wenn das Ende des Streams erreicht wurde, plant ein EC \_ Complete-Ereignis für den Filter Graph-Manager. Virtu.                                    |
| [**TimerCallback**](cbaserenderer-timercallback.md)                         | Rückruf Methode für das End-of-Stream-Timer-Ereignis.                                                                                      |
| Öffentliche Methoden: Handler                                                     | BESCHREIBUNG                                                                                                                             |
| [**Onreceivefirstsample**](cbaserenderer-onreceivefirstsample.md)           | Wird aufgerufen, wenn der Filter ein Beispiel empfängt, während er angehalten wurde. Virtu.                                                                         |
| [**Onrenderend**](cbaserenderer-onrenderend.md)                             | Wird aufgerufen, nachdem ein Beispiel gerendert wurde. Virtu.                                                                                             |
| [**Onrenderstart**](cbaserenderer-onrenderstart.md)                         | Wird aufgerufen, wenn das Rendering gerade gestartet wird. Virtu.                                                                                       |
| [**Onstartstreaming**](cbaserenderer-onstartstreaming.md)                   | Wird aufgerufen, wenn der Filter das Streaming startet. Virtu.                                                                                       |
| [**Onstopstreaming**](cbaserenderer-onstopstreaming.md)                     | Wird aufgerufen, wenn der Filter das Streaming stoppt. Virtu.                                                                                        |
| [**Onwaitend**](cbaserenderer-onwaitend.md)                                 | Wird aufgerufen, wenn der Filter auf die Präsentationszeit eines Beispiels wartet. Virtu.                                                       |
| [**Onwaitstart**](cbaserenderer-onwaitstart.md)                             | Wird aufgerufen, wenn der Filter beginnt, auf die Präsentationszeit eines Beispiels zu warten. Virtu.                                                        |
| [**Preparerender**](cbaserenderer-preparerender.md)                         | Wird aufgerufen, bevor der Filter ein Beispiel rendert. Virtu.                                                                                     |
| [**"Schulddrawsamplenow"**](cbaserenderer-shoulddrawsamplenow.md)             | Bestimmt, wie ein Beispiel für das Rendering geplant wird. Virtu.                                                                            |
| Reine virtuelle Methoden                                                         | BESCHREIBUNG                                                                                                                             |
| [**Checkmediatype**](cbaserenderer-checkmediatype.md)                       | Bestimmt, ob der Filter einen bestimmten Medientyp akzeptiert.                                                                                 |
| [**Dorendersample**](cbaserenderer-dorendersample.md)                       | Rendert ein Beispiel.                                                                                                                       |
| Imediafilter-Methoden                                                         | BESCHREIBUNG                                                                                                                             |
| [**GetState**](cbaserenderer-getstate.md)                                   | Ruft den Zustand des Filters ab (wird ausgeführt, beendet oder angehalten).                                                                             |
| [**Anhalten**](cbaserenderer-pause.md)                                         | Hält den Filter an.                                                                                                                      |
| [**Ausführen**](cbaserenderer-run.md)                                             | Führt den Filter aus.                                                                                                                        |
| [**Stop**](cbaserenderer-stop.md)                                           | Beendet den Filter.                                                                                                                       |
| Ibasefilter-Methoden                                                          | BESCHREIBUNG                                                                                                                             |
| [**Findpin**](cbaserenderer-findpin.md)                                     | Ruft die PIN mit dem angegebenen Bezeichner ab.                                                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




