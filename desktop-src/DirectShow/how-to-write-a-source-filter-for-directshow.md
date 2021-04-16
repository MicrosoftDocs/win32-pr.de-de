---
description: In diesem Thema wird beschrieben, wie ein benutzerdefinierter Quell Filter für DirectShow geschrieben wird.
ms.assetid: 032f7624-2237-41cd-844a-18ed4a2e420d
title: Schreiben eines Quell Filters für DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87af99595a43c86be0e2f4ecaa51768a211e9674
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522520"
---
# <a name="how-to-write-a-source-filter-for-directshow"></a>Schreiben eines Quell Filters für DirectShow

In diesem Thema wird beschrieben, wie ein benutzerdefinierter Quell Filter für DirectShow geschrieben wird.

> [!Note]  
> In diesem Thema werden nur pushquellen beschrieben. Es werden keine pullquellen, z. b. der Async-Reader-Filter, oder Splitter Filter beschrieben, die eine Verbindung mit Pull-Quellen herstellen. Informationen zu den Unterschieden zwischen *Push* -und *Pull* -Quellen finden Sie unter [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md).

 

## <a name="the-directshow-streaming-model"></a>Das DirectShow-Streamingmodell

Wenn Sie einen Quell Filter schreiben, ist es wichtig zu verstehen, dass eine pushquelle nicht dasselbe wie eine Live Quelle ist. Eine Live Quelle ruft Daten aus einer externen Quelle, z. b. einer Kamera oder einem Netzwerkstream, ab. Im Allgemeinen kann eine Live Quelle die eingehende Daten Rate nicht steuern. Wenn die downstreamfilter die Daten nicht schnell genug verarbeiten, muss die Quelle Beispiele ablegen.

Eine pushquelle muss jedoch keine Live Quelle sein. Beispielsweise kann eine pushquelle Daten aus einer lokalen Datei lesen. In diesem Fall bestimmen die nachgeschalteten rendererfilter, wie schnell die Daten aus der Quelle genutzt werden, basierend auf der Referenzuhr und den Beispiel Zeitstempeln. Der Quell Filter liefert Stichproben so schnell wie möglich, aber der tatsächliche Datenfluss wird durch die Renderer eingeschränkt. Die Mechanismen zum Durchlaufen des Datenflusses werden im [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md)beschrieben.

Jede Ausgabe-PIN im Quell Filter erstellt einen Thread, der als *streamingthread* bezeichnet wird. Die PIN liefert Beispiele für den streamingthread. In der Regel erfolgen alle Decodierungs-, Verarbeitungs-und Rendering-Vorgänge in diesem Thread, obwohl einige downstreamfilter zusätzliche Threads erstellen können, um Ihre Ausgabe Beispiele in die Warteschlange zu stellen

Der streamingthread führt eine-Schleife mit der folgenden Struktur aus:

``` syntax
until (stopped)
  1. Get a media sample from the allocator.
  2. Fill the sample with data.
  3. Time stamp the sample. 
  4. Deliver the sample downstream.
```

Wenn keine Beispiele verfügbar sind, blockiert Schritt 1, bis eine Stichprobe verfügbar wird. Schritt 4 kann auch blockieren. Beispielsweise kann dies blockiert werden, während das Diagramm angehalten wird.

Die-Schleife wird so schnell wie möglich ausgeführt, aber Sie ist darauf beschränkt, wie schnell der rendererfilter die einzelnen Beispiele rendert. Wenn das Filter Diagramm eine Referenzuhr aufweist, wird die Rate durch die Präsentations Zeiten der Stichproben bestimmt. Wenn keine Referenzuhr vorhanden ist, verarbeitet der Renderer die Stichproben so schnell wie möglich.

## <a name="using-csource-and-csourcestream"></a>Verwenden von CSource und csourcestream

Die DirectShow-Basisklassen enthalten zwei Klassen, die pushquellen unterstützen: [**CSource**](csource.md) und [**csourcestream**](csourcestream.md).

-   [**CSource**](csource.md) ist die Basisklasse für den Filter und implementiert die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle.
-   [**Csourcestream**](csourcestream.md) ist die Basisklasse für die Ausgabe Pins und implementiert die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle.

### <a name="output-pins"></a>Ausgabe Pins

Ein Quell Filter kann über mehr als eine Ausgabepin verfügen. Erstellen Sie in der Konstruktormethode Ihres Filters mindestens eine PIN, die von [**csourcestream**](csourcestream.md) (eine PIN pro Ausgabestream) abgeleitet ist. Sie müssen keine Zeiger auf die Pins speichern. die Pins werden automatisch dem Filter hinzugefügt, wenn Sie erstellt werden.

### <a name="output-formats"></a>Ausgabeformate

Die Ausgabe-PIN verarbeitet die formataushandlung mit den folgenden [**csourcestream**](csourcestream.md) -Methoden:



| Methode                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getmediatype**](csourcestream-getmediatype.md)     | Ruft einen Medientyp aus der Ausgabe-PIN ab. <br/> Die PIN muss mindestens einen Medientyp vorschlagen, da der Downstream-Filter möglicherweise keine Typen vorschlägt. In den meisten Fällen ist der Downstream-Filter ein Decoder oder ein Renderer, je nachdem, ob der Quell Filter komprimierte oder nicht komprimierte Daten bereitstellt. Ein rendererfilter erfordert in der Regel einen vollständigen Medientyp, der alle zum Rendern des Streams erforderlichen Formatierungsinformationen enthält. Bei einem Decoder hängt die Menge der Informationen, die im Medientyp erforderlich ist, stark vom Codierungsformat ab.<br/> |
| [**Checkmediatype**](csourcestream-checkmediatype.md) | Überprüft, ob die Ausgabepin einen bestimmten Medientyp akzeptiert. Das Überschreiben dieser Methode ist optional, je nachdem, wie Sie " [**getmediatype**](csourcestream-getmediatype.md)" implementieren.                                                                                                                                                                                                                                                                                                                                                                                                         |



 

Die [**getmediatype**](csourcestream-getmediatype.md) -Methode ist überladen:

-   [**Getmediatype**](csourcestream-getmediatype.md) (1) übernimmt einen einzelnen Parameter, einen Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt.
-   [**Getmediatype**](csourcestream-getmediatype2.md) (2) nimmt eine Index Variable und einen Zeiger auf ein [**cmediatype**](cmediatype.md) -Objekt an.

Wenn die Ausgabe-PIN des Quell Filters genau ein Medienformat unterstützt, sollten Sie (1) überschreiben, um das [**cmediatype**](cmediatype.md) -Objekt mit diesem Format zu initialisieren. Belassen Sie die Standard Implementierung von (2), und belassen Sie auch die Standard Implementierung von [**checkmediatype**](csourcestream-checkmediatype.md).

Wenn die PIN mehr als ein Format unterstützt, überschreiben Sie (2). Initialisieren Sie das [**cmediatype**](cmediatype.md) -Objekt gemäß dem Wert der Index Variable. Die PIN sollte die Formate als geordnete Liste zurückgeben. In diesem Fall müssen Sie auch den [**checkmediatype**](csourcestream-checkmediatype.md) außer Kraft setzen, um den Medientyp mit der Liste der Formate zu überprüfen.

Beachten Sie, dass der Downstream-Filter für nicht komprimierte Videoformate Formate mit verschiedenen Stride-Werten vorschlagen kann. Der Filter sollte jeden gültigen Stride-Wert akzeptieren. Weitere Informationen finden Sie unter [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader).

Sie müssen auch die pure-Virtual [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) -Methode überschreiben. Verwenden Sie diese Methode, um die Größe der Beispiel Puffer festzulegen.

### <a name="streaming"></a>Streaming

Die [**csourcestream**](csourcestream.md) -Klasse erstellt den streamingthread für die PIN. Die Thread Prozedur wird in der [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) -Methode implementiert. Diese Methode ruft die pure-Virtual [**csourcestream:: FillBuffer**](csourcestream-fillbuffer.md) -Methode auf, die von der abgeleiteten Klasse überschrieben werden muss. Bei dieser Methode füllt der PIN den Puffer mit Daten. Wenn Ihr Filter beispielsweise unkomprimierte Videos bereitstellt, können Sie die Video Frames zeichnen.

Die-Basisklasse startet und beendet automatisch die Thread Schleife, wenn der Filter anhält oder angehalten wird. In diesem Fall ruft die [**csourcestream**](csourcestream.md) -Klasse einige Methoden auf, um die abgeleitete Klasse zu benachrichtigen:

-   [**Csourcestream:: onthreadcreate**](csourcestream-onthreadcreate.md)
-   [**Csourcestream:: onthreaddestroy**](csourcestream-onthreaddestroy.md)
-   [**Csourcestream:: onthreadstartplay**](csourcestream-onthreadstartplay.md)

Sie können diese Methoden überschreiben, wenn Sie eine spezielle Behandlung hinzufügen müssen. Andernfalls geben die Standard Implementierungen einfach **S \_ OK** zurück.

## <a name="seeking"></a>Diejenigen

Wenn Sie über einen Quell Filter mit einem Ausgabepin verfügen, können Sie die [**csourceseeking**](csourceseeking.md) -Klasse als Ausgangspunkt für die Implementierung der Suche verwenden. Erben Sie Ihre PIN-Klasse sowohl aus [**csourcestream**](csourcestream.md) als auch aus **csourceseeking**.

> [!Note]  
> [**Csourceseeking**](csourceseeking.md) wird nicht für einen Filter mit mehr als einer Ausgabe-PIN empfohlen. Das Hauptproblem besteht darin, dass nur eine PIN auf Suchanforderungen reagieren soll. Dies erfordert in der Regel die Kommunikation zwischen den Pins und dem Filter.

 

Die [**csourceseeking**](csourceseeking.md) -Klasse verwaltet die Wiedergabe Rate, die Startzeit, die Endzeit und die Dauer. Die abgeleitete Klasse sollte die anfängliche Endzeit und die Dauer festlegen. Wenn sich einer dieser Werte ändert, wird die [**csourceseeking:: changerate**](csourceseeking-changerate.md)-, [**csourceseeking:: changestart**](csourceseeking-changestart.md)-oder [**csourceseeking:: changestoppt**](csourceseeking-changestop.md) -Methode entsprechend aufgerufen. Bei den Methoden handelt es sich um reine virtuelle Methoden. Die abgeleitete Pin-Klasse überschreibt diese Methoden, um Folgendes durchzuführen:

1.  Aufrufen von [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) auf der Downstream-PIN. Dies bewirkt, dass Downstream-Filter Stichproben freigeben und neue Beispiele ablehnen.
2.  [**Csourcestream:: Beendigung**](csourcestream-stop.md) aufrufen, um den Streaminginhalt zu verhindern. Der Quell Filter hält die Erstellung neuer Daten an.
3.  Nennen Sie [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) für die downstreampin. Dies signalisiert den downstreamfiltern, neue Daten zu akzeptieren.
4.  Nennen Sie [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) mit den neuen Start-und Endzeit Zeiten und der Geschwindigkeit.
5.  Legen Sie die Diskontinuität-Eigenschaft für das nächste Beispiel fest.

Weitere Informationen finden Sie [unter unterstützen von Such Vorschauen in einem Quell Filter](supporting-seeking-in-a-source-filter.md).

Wenn der Filter Suchvorgänge unterstützt, ist die Streamposition jetzt unabhängig von der Präsentationszeit. Nach einer Suche werden Zeitstempel auf 0 (null) zurückgesetzt. Die allgemeine Formel für Zeitstempel lautet:

-   Beispiel Startzeit = verstrichene Zeit/Wiedergabe Rate
-   Beispiel Endzeit = Stichproben Startzeit + (Zeit pro Frame/Wiedergabe Rate)

die *verstrichene Zeit* ist die verstrichene Zeit seit Beginn der Ausführung des Filters oder seit dem letzten Seek-Befehl.

### <a name="time-formats-for-seeking"></a>Zeitformate für Suchvorgänge

Standardmäßig befinden sich Such Befehle in Einheiten von 100-Nanosekunden. Der Quell Filter kann zusätzliche Zeitformate unterstützen, z. b. die Suche nach Frame Nummer. Jedes Zeitformat wird durch eine GUID identifiziert. siehe [**Zeit Format-GUIDs**](time-format-guids.md).

Um zusätzliche Zeitformate zu unterstützen, müssen Sie die folgenden Methoden für die Ausgabepin implementieren:

-   [**Imediaseeking:: converttimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-converttimeformat)
-   [**Imediaseeking:: getTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [**Imediaseeking:: isformatsupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported)
-   [**Imediaseeking:: isusingtimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [**Imediaseeking:: querypreferredformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat)
-   [**Imediaseeking:: settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

Wenn die Anwendung ein neues Zeitformat festlegt, werden alle Positions Parameter in den [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Methoden im Hinblick auf das neue Zeitformat interpretiert. Wenn das Zeitformat z. b. Frames ist, muss die [**imediaseeking:: getduration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) -Methode die Dauer in Frames zurückgeben.

In der Praxis unterstützen nur wenige DirectShow-Filter zusätzliche Zeitformate. Folglich nutzen einige DirectShow-Anwendungen diese Funktion.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von Quell Filtern](writing-source-filters.md)
</dt> </dl>

 

 




