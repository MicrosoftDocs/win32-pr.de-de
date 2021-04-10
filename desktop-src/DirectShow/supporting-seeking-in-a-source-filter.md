---
description: In diesem Thema wird beschrieben, wie Suchvorgänge in einem Microsoft DirectShow-Quell Filter implementiert werden. Es verwendet das Kugel Filter Beispiel als Ausgangspunkt und beschreibt den zusätzlichen Code, der erforderlich ist, um die Suche in diesem Filter zu unterstützen.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Unterstützen der Suche in einem Quell Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ac4bbb63410adf9cb4e8d69064679143b84d67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868520"
---
# <a name="supporting-seeking-in-a-source-filter"></a>Unterstützen der Suche in einem Quell Filter

In diesem Thema wird beschrieben, wie Suchvorgänge in einem Microsoft DirectShow-Quell Filter implementiert werden. Es verwendet das [Kugel Filter](ball-filter-sample.md) Beispiel als Ausgangspunkt und beschreibt den zusätzlichen Code, der erforderlich ist, um die Suche in diesem Filter zu unterstützen.

Das [Kugel Filter](ball-filter-sample.md) Beispiel ist ein Quell Filter, der einen animierten Sprung-Ball erstellt. In diesem Artikel wird beschrieben, wie Sie diesem Filter Suchfunktionen hinzufügen. Nachdem Sie diese Funktionalität hinzugefügt haben, können Sie den Filter in GraphEdit Rendering und die Kugel steuern, indem Sie den Schieberegler GraphEdit ziehen.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht über das Suchen in DirectShow](#overview-of-seeking-in-directshow)
-   [Kurze Übersicht über den Kugel Filter](#quick-overview-of-the-ball-filter)
-   [Ändern des Kugel Filters für Suchvorgänge](#modifying-the-ball-filter-for-seeking)
-   [Einschränkungen der csourceseeking-Klasse](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a>Übersicht über das Suchen in DirectShow

Eine Anwendung sucht das Filter Diagramm, indem eine [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Methode für den Filter Graph-Manager aufgerufen wird. Der Filter Graph-Manager verteilt dann den Aufruf an jeden Renderer im Diagramm. Jeder Renderer sendet den upstreambefehl über die Ausgabe-PIN des nächsten upstreamfilters. Der-Befehl durchläuft den Upstream, bis er einen Filter erreicht, der den Seek-Befehl ausführen kann, in der Regel einen Quell Filter oder einen Parserfilter. Im allgemeinen verarbeitet der Filter, der die Zeitstempel durchführt, auch das suchen.

Ein Filter antwortet wie folgt auf einen Suchbefehl:

1.  Der Filter leert das Diagramm. Dadurch werden alle veralteten Daten aus dem Diagramm gelöscht, was die Reaktionsfähigkeit verbessert. Andernfalls werden Stichproben, die vor dem Seek-Befehl gepuffert wurden, möglicherweise zugestellt.
2.  Mit dem Filter wird [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) aufgerufen, um Downstream-Filter über die neue Endzeit, die Startzeit und die Wiedergabe Rate zu informieren.
3.  Der Filter legt dann das Diskontinuität-Flag für das erste Beispiel nach dem Seek-Befehl fest.

Zeitstempel beginnen mit 0 (null) nach jedem Seek-Befehl (einschließlich Raten Änderungen).

## <a name="quick-overview-of-the-ball-filter"></a>Kurze Übersicht über den Kugel Filter

Der Kugel Filter ist eine Push-Quelle. Dies bedeutet, dass ein Arbeits Thread verwendet wird, um Abtastungen im Gegensatz zu einer pullquelle bereitzustellen, die passiv darauf wartet, dass ein downstreamfilter Beispiele anfordert. Der Kugel Filter wird aus der [**CSource**](csource.md) -Klasse erstellt, und die Ausgabe-PIN wird aus der [**csourcestream**](csourcestream.md) -Klasse erstellt. Die **csourcestream** -Klasse erstellt den Arbeits Thread, der den Datenfluss steuert. Dieser Thread tritt in eine Schleife ein, die Beispiele aus der Zuweisung abruft, Sie mit Daten füllt und diese nach unten übermittelt.

Der größte Teil der Aktion in [**csourcestream**](csourcestream.md) erfolgt in der [**csourcestream:: FillBuffer**](csourcestream-fillbuffer.md) -Methode, die von der abgeleiteten Klasse implementiert wird. Das Argument für diese Methode ist ein Zeiger auf das Beispiel, das übermittelt werden soll. Die-Implementierung von **FillBuffer** des Kugel Filters Ruft die Adresse des Beispiel Puffers ab und zeichnet durch Festlegen einzelner Pixelwerte direkt in den Puffer. (Das Zeichnen erfolgt durch eine Hilfsklasse, cball, sodass Sie die Details zu Bittiefen, Paletten usw. ignorieren können.)

## <a name="modifying-the-ball-filter-for-seeking"></a>Ändern des Kugel Filters für Suchvorgänge

Um den Kugel Filter suchbar zu machen, verwenden Sie die [**csourceseeking**](csourceseeking.md) -Klasse, die für die Implementierung von suchen in Filtern mit einem Ausgabepin konzipiert ist. Fügen Sie die **csourceseeking** -Klasse der Vererbungs Liste für die cballstream-Klasse hinzu:


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



Außerdem müssen Sie einen Initialisierer für [**csourceseeking**](csourceseeking.md) zum cballstream-Konstruktor hinzufügen:


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



Diese Anweisung ruft den Basiskonstruktor für [**csourceseeking**](csourceseeking.md)auf. Bei den Parametern handelt es sich um einen Namen, einen Zeiger auf den besitzenden PIN, einen **HRESULT** -Wert und die Adresse eines kritischen Abschnitts Objekts. Der Name wird nur zum Debuggen verwendet, und das [**Name**](name.md) -Makro wird in Einzelhandels Builds in eine leere Zeichenfolge kompiliert. Die PIN erbt direkt **csourceseeking**, sodass der zweite Parameter ein Zeiger auf sich selbst ist, der in einen [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Zeiger umgewandelt wird. Der **HRESULT** -Wert wird in der aktuellen Version der Basisklassen ignoriert. die Kompatibilität mit früheren Versionen bleibt bestehen. Der kritische Abschnitt schützt freigegebene Daten, z. b. die aktuelle Startzeit, Endzeit und Wiedergabe Rate.

Fügen Sie die folgende Anweisung im [**csourceseeking**](csourceseeking.md) -Konstruktor hinzu:


```C++
m_rtStop = 60 * UNITS;
```



Die *m \_ rtstoppt* -Variable gibt die Endzeit an. Standardmäßig ist der Wert \_ I64 \_ Max/2, der ungefähr 14.600 Jahre beträgt. Die vorherige Anweisung legt den Wert auf einen konservativeren Wert von 60 Sekunden fest.

Zwei zusätzliche Element Variablen müssen cballstream hinzugefügt werden:


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



Nach jedem Seek-Befehl muss der Filter das Diskontinuität-Flag für das nächste Beispiel durch Aufrufen von [**imediasample:: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity)festlegen. Diese wird von der *m \_ bdiscontinuity* -Variablen nachverfolgt. Die *m \_ rtballposition* -Variable gibt die Position der Kugel innerhalb des Video Rahmens an. Der ursprüngliche Ball Filter berechnet die Position von der streamzeit, aber die streamzeit wird nach jedem Seek-Befehl auf Null zurückgesetzt. In einem durchsuchbaren Datenstrom ist die absolute Position unabhängig von der streamzeit.

### <a name="queryinterface"></a>QueryInterface

Die [**csourceseeking**](csourceseeking.md) -Klasse implementiert die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle. Überschreiben Sie die [**nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) -Methode, um diese Schnittstelle für Clients verfügbar zu machen:


```C++
STDMETHODIMP CBallStream::NonDelegatingQueryInterface
    (REFIID riid, void **ppv)
{
    if( riid == IID_IMediaSeeking ) 
    {
        return CSourceSeeking::NonDelegatingQueryInterface( riid, ppv );
    }
    return CSourceStream::NonDelegatingQueryInterface(riid, ppv);
}
```



Die Methode wird aufgrund der Art und Weise, wie die DirectShow-Basisklassen Component Object Model (com)-Aggregation unterstützen, als "nondelegating" bezeichnet. Weitere Informationen finden Sie im Thema "Gewusst wie: Implementieren von IUnknown" im DirectShow SDK.

### <a name="seeking-methods"></a>Suchmethoden

Die [**csourceseeking**](csourceseeking.md) -Klasse verwaltet mehrere Element Variablen im Zusammenhang mit der Suche.



| Variable          | BESCHREIBUNG   | Standardwert  |
|-------------------|---------------|----------------|
| *m \_ rtstart*      | Startzeit    | Zero           |
| *m \_ rtstopps*       | Endzeit     | \_I64 \_ Max/2 |
| *m \_ drateseeking* | Wiedergabe Rate | 1.0            |



 

Die [**csourceseeking**](csourceseeking.md) -Implementierung von [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) aktualisiert die Start-und Endzeiten und ruft dann zwei rein virtuelle Methoden für die abgeleitete Klasse [**csourceseeking:: changestart**](csourceseeking-changestart.md) und [**csourceseeking:: changestoppt**](csourceseeking-changestop.md)auf. Die Implementierung von [**imediaseeking:: ctrate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) ist ähnlich: die Wiedergabe Rate wird aktualisiert, und anschließend wird die reine virtuelle Methode [**csourceseeking:: changerate**](csourceseeking-changerate.md)aufgerufen. In jeder dieser virtuellen Methoden muss die PIN folgende Aktionen ausführen:

1.  Aufrufen von [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) , um mit dem leeren von Daten zu beginnen.
2.  Stoppt den streamingthread.
3.  Nennen Sie [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
4.  Starten Sie den streamingthread neu.
5.  Nennen Sie [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).
6.  Legen Sie das Diskontinuität-Flag für das nächste Beispiel fest.

Die Reihenfolge dieser Schritte ist entscheidend, da der streamingthread blockiert werden kann, während er darauf wartet, ein Beispiel bereitzustellen oder ein neues Beispiel zu erhalten. Die [**beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode stellt sicher, dass der Streaminginhalt nicht blockiert wird und daher in Schritt 2 keinen Deadlock findet. Der [**endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Befehl informiert die downstreamfilter, dass neue Beispiele erwartet werden, sodass Sie nicht abgelehnt werden, wenn der Thread in Schritt 4 erneut gestartet wird.

Die folgende private Methode führt die Schritte 1 bis 4 aus:


```C++
void CBallStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        // Shut down the thread and stop pushing data.
        Stop();
        DeliverEndFlush();
        // Restart the thread and start pushing data again.
        Pause();
    }
}
```



Wenn der streamingthread erneut gestartet wird, ruft er die [**csourcestream:: onthreadstartplay**](csourcestream-onthreadstartplay.md) -Methode auf. Überschreiben Sie diese Methode, um die Schritte 5 und 6 auszuführen:


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



Legen Sie in der [**changestart**](csourceseeking-changestart.md) -Methode die streamzeit auf 0 (null) und die Position der Kugel auf die neue Startzeit fest. Dann cballstream:: updatefromseek aufrufen:


```C++
HRESULT CBallStream::ChangeStart( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_rtSampleTime = 0;
        m_rtBallPosition = m_rtStart;
    }
    UpdateFromSeek();
    return S_OK;
}
```



In der [**changeend**](csourceseeking-changestop.md) -Methode wird cballstream:: updatefromseek aufgerufen, wenn die neue Endzeit kleiner als die aktuelle Position ist. Andernfalls ist die Endzeit noch in der Zukunft, sodass es nicht erforderlich ist, das Diagramm zu leeren.


```C++
HRESULT CBallStream::ChangeStop( )
{
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        if (m_rtBallPosition < m_rtStop)
        {
            return S_OK;
        }
    }

    // We're already past the new stop time. Flush the graph.
    UpdateFromSeek();
    return S_OK;
}
```



Bei Raten Änderungen legt die [**csourceseeking:: setRate**](csourceseeking-setrate.md) -Methode *m \_ drateseeking* auf den neuen Satz fest (verwerfen des alten Werts), bevor [**changerate**](csourceseeking-changerate.md)aufgerufen wird. Wenn der Aufrufer eine ungültige Rate gab – z. b. kleiner als 0 (null) – ist es zu spät, wenn der **changerate** aufgerufen wird. Eine Lösung besteht darin, **die-Aktivität** zu überschreiben und auf gültige Raten zu prüfen:


```C++
HRESULT CBallStream::SetRate(double dRate)
{
    if (dRate <= 1.0)
    {
        return E_INVALIDARG;
    }
    {
        CAutoLock lock(CSourceSeeking::m_pLock);
        m_dRateSeeking = dRate;
    }
    UpdateFromSeek();
    return S_OK;
}
// Now ChangeRate won't ever be called, but it's pure virtual, so it needs
// a dummy implementation.
HRESULT CBallStream::ChangeRate() { return S_OK; }
```



### <a name="drawing-in-the-buffer"></a>Zeichnen im Puffer

Dies ist die geänderte Version von [**csourcestream:: FillBuffer**](csourcestream-fillbuffer.md), der Routine, die die Kugel in jedem Frame zeichnet:


```C++
HRESULT CBallStream::FillBuffer(IMediaSample *pMediaSample)
{
    BYTE *pData;
    long lDataLen;
    pMediaSample->GetPointer(&pData);
    lDataLen = pMediaSample->GetSize();
    {
        CAutoLock cAutoLockShared(&m_cSharedState);
        if (m_rtBallPosition >= m_rtStop) 
        {
            // End of the stream.
            return S_FALSE;
        }
        // Draw the ball in its current position.
        ZeroMemory( pData, lDataLen );
        m_Ball->MoveBall(m_rtBallPosition);
        m_Ball->PlotBall(pData, m_BallPixel, m_iPixelSize);
        
        // The sample times are modified by the current rate.
        REFERENCE_TIME rtStart, rtStop;
        rtStart = static_cast<REFERENCE_TIME>(
                      m_rtSampleTime / m_dRateSeeking);
        rtStop  = rtStart + static_cast<int>(
                      m_iRepeatTime / m_dRateSeeking);
        pMediaSample->SetTime(&rtStart, &rtStop);

        // Increment for the next loop.
        m_rtSampleTime += m_iRepeatTime;
        m_rtBallPosition += m_iRepeatTime;
    }
    pMediaSample->SetSyncPoint(TRUE);
    if (m_bDiscontinuity) 
    {
        pMediaSample->SetDiscontinuity(TRUE);
        m_bDiscontinuity = FALSE;
    }
    return NOERROR;
}
```



Die wichtigsten Unterschiede zwischen dieser Version und der ursprünglichen Version sind die folgenden:

-   Wie bereits erwähnt, wird die *m \_ rtballposition* -Variable verwendet, um die Position der Kugel anstelle der streamzeit festzulegen.
-   Nach dem halten des kritischen Abschnitts prüft die Methode, ob die aktuelle Position die Endzeit überschreitet. Wenn dies der Fall ist, wird **S \_ false** zurückgegeben. Dadurch wird der Basisklasse signalisiert, das Senden von Daten zu beenden und eine Streamende Benachrichtigung bereitzustellen.
-   Die Zeitstempel werden durch die aktuelle Rate dividiert.
-   Wenn *m \_ bdiscontinuity* auf **true** festgelegt ist, legt die-Methode das Diskontinuität-Flag für das Beispiel fest.

Es gibt noch einen weiteren kleinen Unterschied. Da die ursprüngliche Version darauf basiert, dass genau ein Puffer vorhanden ist, füllt Sie den gesamten Puffer einmal mit Nullen auf, sobald das Streaming beginnt. Danach wird der Ball nur noch von seiner vorherigen Position gelöscht. Diese Optimierung zeigt jedoch einen geringfügigen Fehler im Ball Filter. Wenn die [**cbaseoutputpin::D ecidezuordcator**](cbaseoutputpin-decideallocator.md) -Methode [**IMemInputPin:: notifyzuweisung**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)aufruft, wird das schreibgeschützte Flag auf **false** festgelegt. Folglich kann der Downstream-Filter in den Puffer schreiben. Eine Lösung besteht darin, **dezidezuordcator** zu überschreiben, sodass das Flag für schreibgeschützten Zugriff auf **true** festgelegt wird. Der Einfachheit halber entfernt die neue Version die Optimierung einfach ganz. Stattdessen füllt diese Version den Puffer jedes Mal mit Nullen auf.

### <a name="miscellaneous-changes"></a>Sonstige Änderungen

In der neuen Version werden diese beiden Zeilen aus dem cball-Konstruktor entfernt:


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



Der ursprüngliche Kugel Filter verwendet diese Werte, um der Anfangs Ball Position etwas Zufälligkeit hinzuzufügen. Für unsere Zwecke soll die Kugel deterministisch sein. Außerdem wurden einige [**Variablen von den**](creftime.md) Objekten in [**Verweis \_ Zeit**](reference-time.md) Variablen geändert. (Die Klasse "- **Zeit** " ist ein schlanker Wrapper für einen **Verweis \_ Zeitwert** .) Schließlich wurde die Implementierung von [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) leicht geändert. Weitere Informationen finden Sie im Quellcode.

## <a name="limitations-of-the-csourceseeking-class"></a>Einschränkungen der csourceseeking-Klasse

Die [**csourceseeking**](csourceseeking.md) -Klasse ist aufgrund von Problemen mit der Kreuz-Pin-Kommunikation nicht für Filter mit mehreren Ausgabe Pins gedacht. Stellen Sie sich z. b. einen Parserfilter vor, der einen überlappenden audiovideostream empfängt, den Stream in seine Audio-und Videokomponenten unterteilt und Video aus einer Ausgabe-PIN und aus einer anderen Audiodatei übermittelt. Beide Ausgabe Pins empfangen jeden Seek-Befehl, aber der Filter sollte nur einmal pro Seek-Befehl suchen. Die Lösung besteht darin, einen der Pins zum Steuern der Suche und zum Ignorieren von Seek-Befehlen festzulegen, die von der anderen Pin empfangen werden.

Nach dem Seek-Befehl sollten jedoch beide Pins Daten leeren. Um das Problem weiter zu erschweren, geschieht der Seek-Befehl im Anwendungs Thread, nicht im streamingthread. Daher müssen Sie sicherstellen, dass keine PIN blockiert ist und darauf wartet, dass ein [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Befehl zurückgegeben wird, oder es kann zu einem Deadlock führen. Weitere Informationen zur Thread sicheren Leerung in Pins finden Sie unter [Threads und kritische Abschnitte](threads-and-critical-sections.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von Quell Filtern](writing-source-filters.md)
</dt> </dl>

 

 



