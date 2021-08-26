---
description: In diesem Thema wird beschrieben, wie Sie einen benutzerdefinierten Quellfilter für DirectShow schreiben.
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: Schreiben eines Quellfilters für DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79ea6821dc7d56f2628ce68e7320e5e76b2c1643978e68287d434b7a111cbbd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043240"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a>Schreiben eines Quellfilters für DirectShow

In diesem Thema wird beschrieben, wie Sie einen benutzerdefinierten Quellfilter für DirectShow schreiben.

> [!Note]  
> In diesem Thema werden nur Pushquellen beschrieben. Sie beschreibt keine Pullquellen, z. B. den Async Reader Filter oder Splitterfilter, die eine Verbindung mit Pullquellen herstellen. Informationen zum Unterschied zwischen *Push-* und *Pullquellen* finden Sie unter [Data Flow for Filter Developers](data-flow-for-filter-developers.md).

 

## <a name="the-directshow-streaming-model"></a>Das DirectShow-Streamingmodell

Wenn Sie einen Quellfilter schreiben, ist es wichtig zu verstehen, dass eine Pushquelle nicht mit einer Livequelle identisch ist. Eine Livequelle ruft Daten aus einer externen Quelle ab, z. B. einer Kamera oder einem Netzwerkdatenstrom. Im Allgemeinen kann eine Livequelle die eingehende Datenrate nicht steuern. Wenn die Downstreamfilter die Daten nicht schnell genug nutzen, muss die Quelle Stichproben löschen.

Eine Pushquelle muss jedoch keine Livequelle sein. Beispielsweise kann eine Pushquelle Daten aus einer lokalen Datei lesen. In diesem Fall bestimmen die Downstreamrendererfilter basierend auf der Referenzuhr und den Beispielzeitstempeln, wie schnell sie die Daten aus der Quelle nutzen. Der Quellfilter liefert so schnell wie möglich Stichproben, aber der tatsächliche Datenfluss wird durch die Renderer eingeschränkt. Die Mechanismen zum Gating des Datenflusses werden unter [Data Flow for Filter Developers (Daten Flow für Filterentwickler)](data-flow-for-filter-developers.md)beschrieben.

Jeder Ausgabepin im Quellfilter erstellt einen Thread, der als *Streamingthread* bezeichnet wird. Die Stecknadel liefert Beispiele für den Streamingthread. In der Regel erfolgt die gesamte Decodierung, Verarbeitung und das Rendering in diesem Thread, obwohl einige Downstreamfilter zusätzliche Threads erstellen können, um ihre Ausgabebeispiele in die Warteschlange zu stellen.

Der Streamingthread führt eine Schleife mit der folgenden Struktur aus:

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

Wenn keine Beispiele verfügbar sind, wird Schritt 1 blockiert, bis ein Beispiel verfügbar wird. Schritt 4 kann ebenfalls blockiert werden. Sie kann z. B. blockieren, während das Diagramm angehalten wird.

Die -Schleife wird so schnell wie möglich ausgeführt, ist jedoch durch die Anzahl der Rendererfilter beschränkt, die jedes Beispiel rendern. Wenn das Filterdiagramm über eine Referenzuhr verfügt, wird die Rate durch die Präsentationszeiten der Stichproben bestimmt. Wenn keine Referenzuhr vorhanden ist, verwendet der Renderer Stichproben so schnell wie möglich.

## <a name="using-csource-and-csourcestream"></a>Verwenden von CSource und CSourceStream

Die DirectShow-Basisklassen enthalten zwei Klassen, die Pushquellen unterstützen: [**CSource**](csource.md) und [**CSourceStream.**](csourcestream.md)

-   [**CSource**](csource.md) ist die Basisklasse für den Filter und implementiert die [**IBaseFilter-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)
-   [**CSourceStream**](csourcestream.md) ist die Basisklasse für die Ausgabepins und implementiert die [**IPin-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-ipin)

### <a name="output-pins"></a>Ausgabepins

Ein Quellfilter kann mehrere Ausgabepins aufweisen. Erstellen Sie in der Konstruktormethode Ihres Filters mindestens einen von [**CSourceStream**](csourcestream.md) abgeleiteten Pin (einen Pin pro Ausgabestream). Sie müssen keine Zeiger auf die Stecknadeln speichern. die Pins fügen sich automatisch dem Filter hinzu, wenn sie erstellt werden.

### <a name="output-formats"></a>Ausgabeformate

Der Ausgabepin verarbeitet die Formataushandlung mit den folgenden [**CSourceStream-Methoden:**](csourcestream.md)



| Methode                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetMediaType**](csourcestream-getmediatype.md)     | Ruft einen Medientyp vom Ausgabepin ab. <br/> Der Pin muss mindestens einen Medientyp vorschlagen, da der Downstreamfilter möglicherweise keine Typen vorschlägt. In den meisten Fällen ist der Downstreamfilter ein Decoder oder renderer, je nachdem, ob der Quellfilter komprimierte oder nicht komprimierte Daten übermittelt. Ein Rendererfilter erfordert in der Regel einen vollständigen Medientyp, der alle Formatinformationen enthält, die zum Rendern des Streams erforderlich sind. Bei einem Decoder hängt die Menge der erforderlichen Informationen im Medientyp stark vom Codierungsformat ab.<br/> |
| [**CheckMediaType**](csourcestream-checkmediatype.md) | Überprüft, ob der Ausgabepin einen bestimmten Medientyp akzeptiert. Das Überschreiben dieser Methode ist optional, je nachdem, wie Sie [**GetMediaType**](csourcestream-getmediatype.md)implementieren.                                                                                                                                                                                                                                                                                                                                                                                                         |



 

Die [**GetMediaType-Methode**](csourcestream-getmediatype.md) ist überladen:

-   [**GetMediaType**](csourcestream-getmediatype.md) (1) verwendet einen einzelnen Parameter, einen Zeiger auf ein [**CMediaType-Objekt.**](cmediatype.md)
-   [**GetMediaType**](csourcestream-getmediatype2.md) (2) verwendet eine Indexvariable und einen Zeiger auf ein [**CMediaType-Objekt.**](cmediatype.md)

Wenn der Ausgabepin des Quellfilters genau ein Medienformat unterstützt, sollten Sie (1) überschreiben, um das [**CMediaType-Objekt**](cmediatype.md) mit diesem Format zu initialisieren. Belassen Sie die Standardimplementierungen von (2) und die Standardimplementierungen von [**CheckMediaType.**](csourcestream-checkmediatype.md)

Wenn der Pin mehrere Formate unterstützt, überschreiben Sie (2). Initialisieren Sie das [**CMediaType-Objekt**](cmediatype.md) entsprechend dem Wert der Indexvariablen. Die Stecknadel sollte die Formate als sortierte Liste zurückgeben. In diesem Fall müssen Sie auch [**CheckMediaType**](csourcestream-checkmediatype.md) überschreiben, um den Medientyp anhand Ihrer Formatliste zu überprüfen.

Beachten Sie bei nicht komprimierten Videoformaten, dass der Downstreamfilter Formate mit verschiedenen Schrittwerten vorschlagen kann. Ihr Filter sollte jeden gültigen Schrittwert akzeptieren. Weitere Informationen finden Sie unter [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader).

Sie müssen auch die rein virtuelle [**CBaseOutputPin::D ecideBufferSize-Methode**](cbaseoutputpin-decidebuffersize.md) überschreiben. Verwenden Sie diese Methode, um die Größe der Beispielpuffer festzulegen.

### <a name="streaming"></a>Streaming

Die [**CSourceStream-Klasse**](csourcestream.md) erstellt den Streamingthread für den Pin. Die Threadprozedur wird in der [**CSourceStream::D oBufferProcessingLoop-Methode**](csourcestream-dobufferprocessingloop.md) implementiert. Diese Methode ruft die rein virtuelle [**CSourceStream::FillBuffer-Methode**](csourcestream-fillbuffer.md) auf, die die abgeleitete Klasse überschreiben muss. Bei dieser Methode füllt der Stecknadel den Puffer mit Daten. Wenn Ihr Filter beispielsweise unkomprimierte Videos übermittelt, zeichnen Sie die Videoframes an dieser Stelle.

Die Basisklasse startet und beendet die Threadschleife automatisch zu den richtigen Zeiten, wenn der Filter angehalten oder beendet wird. In diesem Fall ruft die [**CSourceStream-Klasse**](csourcestream.md) einige Methoden auf, um ihre abgeleitete Klasse zu benachrichtigen:

-   [**CSourceStream::OnThreadCreate**](csourcestream-onthreadcreate.md)
-   [**CSourceStream::OnThreadDestroy**](csourcestream-onthreaddestroy.md)
-   [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md)

Sie können diese Methoden überschreiben, wenn Sie eine spezielle Behandlung hinzufügen müssen. Andernfalls geben die Standardimplementierungen einfach **S \_ OK** zurück.

## <a name="seeking"></a>Suchen

Wenn Sie über einen Quellfilter mit einem Ausgabepin verfügen, können Sie die [**CSourceSeeking-Klasse**](csourceseeking.md) als Ausgangspunkt für die Implementierung von Suchabfragen verwenden. Erben Sie Ihre Pin-Klasse sowohl von [**CSourceStream**](csourcestream.md) als **auch von CSourceSeeking.**

> [!Note]  
> [**CSourceSeeking**](csourceseeking.md) wird für filter mit mehr als einem Ausgabepin nicht empfohlen. Das Hauptproblem besteht darin, dass nur ein Pin auf Suchanforderungen reagieren sollte. Dies erfordert in der Regel die Kommunikation zwischen den Pins und dem Filter.

 

Die [**CSourceSeeking-Klasse**](csourceseeking.md) verwaltet die Wiedergaberate, Startzeit, Beendigungszeit und Dauer. Ihre abgeleitete Klasse sollte die anfängliche Beendigungszeit und -dauer festlegen. Wenn sich einer dieser Werte ändert, wird die [**Methode CSourceSeeking::ChangeRate,**](csourceseeking-changerate.md) [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)oder [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md) nach Bedarf aufgerufen. Die Methoden sind alle rein virtuelle Methoden. Die abgeleitete Pin-Klasse überschreibt diese Methoden, um Folgendes zu tun:

1.  Rufen Sie [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) auf dem Downstreampin auf. Dies führt dazu, dass Downstreamfilter Stichproben freigeben, die sie enthalten, und neue Stichproben ablehnen.
2.  Rufen Sie [**CSourceStream::Stop**](csourcestream-stop.md) auf, um den Streamingthread zu beenden. Der Quellfilter unterbricht die Erstellung neuer Daten.
3.  Rufen Sie [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) auf dem Downstreampin auf. Dies signalisiert den Downstreamfiltern, dass sie neue Daten akzeptieren.
4.  Rufen Sie [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) mit den neuen Start- und Stoppzeiten und der Rate auf.
5.  Legen Sie die Diskontinuitätseigenschaft für das nächste Beispiel fest.

Weitere Informationen finden Sie unter [Unterstützen von Suchabfragen in einem Quellfilter.](supporting-seeking-in-a-source-filter.md)

Wenn Ihr Filter Suchabfragen unterstützt, ist die Streamposition jetzt unabhängig von der Präsentationszeit. Nach einer Suche werden Zeitstempel auf 0 (null) zurückgesetzt. Die allgemeine Formel für Zeitstempel lautet:

-   Beispielstartzeit = verstrichene Zeit/Wiedergaberate
-   Endzeit der Stichprobe = Startzeit der Stichprobe + (Zeit pro Frame/Wiedergaberate)

dabei ist die *verstrichene Zeit* die Zeit, die seit der Ausführung des Filters oder seit dem letzten Suchbefehl verstrichen ist.

### <a name="time-formats-for-seeking"></a>Zeitformate für Suche

Standardmäßig liegen seek-Befehle in Einheiten von 100 Nanosekunden vor. Ihr Quellfilter kann zusätzliche Zeitformate unterstützen, z. B. die Suche nach Framenummer. Jedes Mal, wenn das Format durch eine GUID identifiziert wird; weitere Informationen finden Sie unter [**Zeitformat-GUIDs.**](time-format-guids.md)

Um zusätzliche Zeitformate zu unterstützen, müssen Sie die folgenden Methoden auf dem Ausgabepin implementieren:

-   [**IMediaSeeking::ConvertTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Wenn die Anwendung ein neues Zeitformat festlegt, werden alle Positionsparameter in den [**IMediaSeeking-Methoden**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) als neues Zeitformat interpretiert. Wenn das Zeitformat beispielsweise Frames ist, muss die [**IMediaSeeking::GetDuration-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) die Dauer in Frames zurückgeben.

In der Praxis unterstützen einige DirectShow-Filter zusätzliche Zeitformate, und daher nutzen nur wenige DirectShow-Anwendungen diese Funktion.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von Quellfiltern](writing-source-filters.md)
</dt> </dl>

 

 




