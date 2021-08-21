---
description: In diesem Thema wird beschrieben, wie Suchabfragen in einem Microsoft DirectShow-Quellfilter implementiert werden. Es verwendet das Beispiel "Ballfilter" als Ausgangspunkt und beschreibt den zusätzlichen Code, der zur Unterstützung der Suche in diesem Filter erforderlich ist.
ms.assetid: a2b4be09-2fd6-4aac-8ad6-c3d62377c1f2
title: Unterstützen von Suchabfragen in einem Quellfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92c52ff4bde3ea75b156e5521af9825b0902df38f0d0c6bc23cc7be99c37a55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072354"
---
# <a name="supporting-seeking-in-a-source-filter"></a>Unterstützen von Suchabfragen in einem Quellfilter

In diesem Thema wird beschrieben, wie Suchabfragen in einem Microsoft DirectShow-Quellfilter implementiert werden. Es verwendet das [Beispiel "Ballfilter"](ball-filter-sample.md) als Ausgangspunkt und beschreibt den zusätzlichen Code, der zur Unterstützung der Suche in diesem Filter erforderlich ist.

Das [Beispiel "Ballfilter"](ball-filter-sample.md) ist ein Quellfilter, der eine animierte Hüpfkugel erstellt. In diesem Artikel wird beschrieben, wie Sie diesem Filter Suchfunktionen hinzufügen. Nachdem Sie diese Funktion hinzugefügt haben, können Sie den Filter in GraphEdit rendern und die Kugel steuern, indem Sie den GraphEdit-Schieberegler ziehen.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht über Sucher in DirectShow](#overview-of-seeking-in-directshow)
-   [Kurze Übersicht über den Kugelfilter](#quick-overview-of-the-ball-filter)
-   [Ändern des Ballfilters für Die Suche](#modifying-the-ball-filter-for-seeking)
-   [Einschränkungen der CSourceSeeking-Klasse](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a>Übersicht über Sucher in DirectShow

Eine Anwendung sucht den Filtergraphen, indem sie eine [**IMediaSeeking-Methode**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) im Filter Graph Manager aufruft. Der Filter Graph Manager verteilt dann den Aufruf an jeden Renderer im Diagramm. Jeder Renderer sendet den Aufruf upstream über den Ausgabepin des nächsten Upstreamfilters. Der Aufruf wird vorgeschaltet, bis er einen Filter erreicht, der den Suchbefehl ausführen kann, in der Regel ein Quellfilter oder ein Parserfilter. Im Allgemeinen verarbeitet der Filter, der aus den Zeitstempeln stammt, auch Suchabfragen.

Ein Filter antwortet wie folgt auf einen Suchbefehl:

1.  Der Filter leert das Diagramm. Dadurch werden veraltete Daten aus dem Diagramm gelöscht, wodurch die Reaktionsfähigkeit verbessert wird. Andernfalls können Beispiele, die vor dem Suchbefehl gepuffert wurden, übermittelt werden.
2.  Der Filter ruft [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) auf, um Downstreamfilter über die neue Beendigungszeit, Startzeit und Wiedergaberate zu informieren.
3.  Der Filter legt dann das Diskontinuitätsflag für das erste Beispiel nach dem Seek-Befehl fest.

Zeitstempel beginnen nach jedem Suchbefehl (einschließlich Ratenänderungen) bei 0 (null).

## <a name="quick-overview-of-the-ball-filter"></a>Kurze Übersicht über den Kugelfilter

Der Ball-Filter ist eine Pushquelle, d. h., er verwendet einen Arbeitsthread, um Stichproben nachgeschaltet zu übermitteln, im Gegensatz zu einer Pullquelle, die passiv auf einen Downstreamfilter wartet, um Stichproben anzufordern. Der Ball-Filter wird aus der [**CSource-Klasse**](csource.md) erstellt, und sein Ausgabepin wird aus der [**CSourceStream-Klasse**](csourcestream.md) erstellt. Die **CSourceStream-Klasse** erstellt den Arbeitsthread, der den Datenfluss steuert. Dieser Thread wechselt in eine Schleife, die Stichproben aus der Zuweisung erhält, sie mit Daten auffüllt und sie nachgeschaltet übermittelt.

Der Großteil der Aktion in [**CSourceStream**](csourcestream.md) erfolgt in der [**CSourceStream::FillBuffer-Methode,**](csourcestream-fillbuffer.md) die von der abgeleiteten Klasse implementiert wird. Das Argument für diese Methode ist ein Zeiger auf das zu liefernde Beispiel. Die Implementierung von **FillBuffer** durch den Ball-Filter ruft die Adresse des Beispielpuffers ab und zeichnet direkt in den Puffer, indem einzelne Pixelwerte festgelegt werden. (Die Zeichnung wird von der Hilfsklasse CBall durchgeführt, sodass Sie die Details zu Bittiefe, Paletten usw. ignorieren können.)

## <a name="modifying-the-ball-filter-for-seeking"></a>Ändern des Ballfilters für Die Suche

Um den Ball-Filter suchbar zu machen, verwenden Sie die [**CSourceSeeking-Klasse,**](csourceseeking.md) die für die Implementierung von Suchabfragen in Filtern mit einem Ausgabepin konzipiert ist. Fügen Sie die **CSourceSeeking-Klasse** der Vererbungsliste für die CBallStream-Klasse hinzu:


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



Außerdem müssen Sie dem CBallStream-Konstruktor einen Initialisierer für [**CSourceSeeking**](csourceseeking.md) hinzufügen:


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



Diese Anweisung ruft den Basiskonstruktor für [**CSourceSeeking**](csourceseeking.md)auf. Die Parameter sind ein Name, ein Zeiger auf den besitzenden Pin, ein **HRESULT-Wert** und die Adresse eines kritischen Abschnittsobjekts. Der Name wird nur zum Debuggen verwendet, und das [**NAME-Makro**](name.md) wird in Verkaufsbuilds in eine leere Zeichenfolge kompiliert. Der Pin erbt **direkt CSourceSeeking,** sodass der zweite Parameter ein Zeiger auf sich selbst ist und in einen [**IPin-Zeiger**](/windows/desktop/api/Strmif/nn-strmif-ipin) umgestellt wird. Der **HRESULT-Wert** wird in der aktuellen Version der Basisklassen ignoriert. sie bleibt aus Kompatibilitätsgründen mit früheren Versionen bestehen. Der kritische Abschnitt schützt freigegebene Daten, z. B. die aktuelle Startzeit, Beendigungszeit und Wiedergaberate.

Fügen Sie im [**CSourceSeeking-Konstruktor**](csourceseeking.md) die folgende Anweisung hinzu:


```C++
m_rtStop = 60 * UNITS;
```



Die *Variable m \_ rtStop* gibt die Beendigungszeit an. Standardmäßig ist der Wert \_ I64 \_ MAX/2, also ungefähr 14.600 Jahre. Die vorherige Anweisung legt sie auf einen konservativeren Wert von 60 Sekunden fest.

CBallStream müssen zwei zusätzliche Membervariablen hinzugefügt werden:


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



Nach jedem Suchbefehl muss der Filter das Diskontinuitätsflag im nächsten Beispiel festlegen, indem [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity)aufgerufen wird. Die *m \_ bDiscontinuity-Variable* verfolgt dies nach. Die Variable *m \_ rtBallPosition* gibt die Position der Kugel innerhalb des Videoframes an. Der ursprüngliche Ball-Filter berechnet die Position aus der Streamzeit, aber die Streamzeit wird nach jedem Suchbefehl auf 0 (null) zurückgesetzt. In einem suchbaren Stream ist die absolute Position unabhängig von der Streamzeit.

### <a name="queryinterface"></a>QueryInterface

Die [**CSourceSeeking-Klasse**](csourceseeking.md) implementiert die [**IMediaSeeking-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) Um diese Schnittstelle für Clients verfügbar zu machen, überschreiben Sie die [**NonDelegatingQueryInterface-Methode:**](cunknown-nondelegatingqueryinterface.md)


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



Die -Methode wird als "NonDelegating" bezeichnet, da die DirectShow-Basisklassen Component Object Model (COM)-Aggregation unterstützen. Weitere Informationen finden Sie im DirectShow SDK im Thema "Implementieren von IUnknown".

### <a name="seeking-methods"></a>Suchen nach Methoden

Die [**CSourceSeeking-Klasse**](csourceseeking.md) verwaltet mehrere Membervariablen im Zusammenhang mit der Suche.



| Variable          | BESCHREIBUNG   | Standardwert  |
|-------------------|---------------|----------------|
| *m \_ rtStart*      | Startzeit    | Null           |
| *m \_ rtStop*       | Endzeit     | \_I64 \_ MAX/2 |
| *m \_ dRateSeeking* | Wiedergaberate | 1.0            |



 

Die [**CSourceSeeking-Implementierung**](csourceseeking.md) von [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) aktualisiert die Start- und Beendigungszeiten und ruft dann zwei rein virtuelle Methoden für die abgeleitete Klasse auf: [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) und [**CSourceSeeking::ChangeStop.**](csourceseeking-changestop.md) Die Implementierung von [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) ist ähnlich: Sie aktualisiert die Wiedergaberate und ruft dann die reine virtuelle Methode [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md)auf. In jeder dieser virtuellen Methoden muss der Pin folgende Schritte ausführen:

1.  Rufen Sie [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) auf, um mit dem Leeren von Daten zu beginnen.
2.  Halten Sie den Streamingthread an.
3.  Rufen Sie [**IPin::EndFlush auf.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)
4.  Starten Sie den Streamingthread neu.
5.  Rufen Sie [**IPin::NewSegment auf.**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
6.  Legen Sie das Diskontinuitätsflag für das nächste Beispiel fest.

Die Reihenfolge dieser Schritte ist entscheidend, da der Streamingthread blockieren kann, während er auf die Bereitstellung eines Beispiels oder das Abrufen eines neuen Beispiels wartet. Mit der [**BeginFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) wird sichergestellt, dass der Streamingthread nicht blockiert wird und daher in Schritt 2 kein Deadlock entsteht. Der [**EndFlush-Aufruf**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) informiert die Downstreamfilter, dass sie neue Stichproben erwarten, sodass sie sie nicht ablehnen, wenn der Thread in Schritt 4 erneut gestartet wird.

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



Wenn der Streamingthread erneut gestartet wird, ruft er die [**CSourceStream::OnThreadStartPlay-Methode auf.**](csourcestream-onthreadstartplay.md) Überschreiben Sie diese Methode, um die Schritte 5 und 6 auszuführen:


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



Legen Sie in der [**ChangeStart-Methode**](csourceseeking-changestart.md) die Streamzeit auf 0 (null) und die Position der Kugel auf die neue Startzeit fest. Rufen Sie dann CBallStream::UpdateFromSeek auf:


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



Rufen Sie in der [**ChangeStop-Methode**](csourceseeking-changestop.md) CBallStream::UpdateFromSeek auf, wenn die neue Beendigungszeit kleiner als die aktuelle Position ist. Andernfalls liegt die Beendigungszeit noch in der Zukunft, sodass das Diagramm nicht geleert werden muss.


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



Bei Ratenänderungen legt die [**CSourceSeeking::SetRate-Methode**](csourceseeking-setrate.md) *m \_ dRateSeeking* auf die neue Rate fest (verwirft den alten Wert), bevor [**ChangeRate aufruft.**](csourceseeking-changerate.md) Wenn der Aufrufer leider eine ungültige Rate (z. B. kleiner als 0 ) gegeben hat, ist dies zu spät, wenn **ChangeRate** aufgerufen wird. Eine Lösung besteht darin, **SetRate** außer Kraft zu setzen und auf gültige Raten zu prüfen:


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

Hier ist die geänderte Version von [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md), der Routine, die die Kugel auf jedem Frame zeichnet:


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



Die hauptunterschiede zwischen dieser Version und dem Original sind die folgenden:

-   Wie bereits erwähnt, wird die *m \_ rtBallPosition-Variable* verwendet, um die Position der Kugel und nicht die Streamzeit zu festlegen.
-   Nach dem Halten des kritischen Abschnitts überprüft die Methode, ob die aktuelle Position die Stoppzeit überschreitet. Wenn dies der Wert ist, wird **S \_ FALSE** zurückgegeben. Dies signalisiert der Basisklasse, das Senden von Daten zu beenden und eine Benachrichtigung zum Streamende zu senden.
-   Die Zeitstempel werden durch die aktuelle Rate dividiert.
-   Wenn *m \_ bDiscontinuity* **true ist,** legt die Methode das Diskontinuitätsflag für das Beispiel fest.

Es gibt einen weiteren geringfügigen Unterschied. Da die ursprüngliche Version genau einen Puffer verwendet, füllt sie den gesamten Puffer einmal mit Nullen, wenn das Streaming beginnt. Danach löscht er einfach die Kugel aus ihrer vorherigen Position. Diese Optimierung zeigt jedoch einen geringfügigen Fehler im Filter "Ball" an. Wenn die [**CBaseOutputPin::D ecideAllocator-Methode**](cbaseoutputpin-decideallocator.md) [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)aufruft, wird das schreibgeschützte Flag auf **FALSE festgelegt.** Daher kann der Downstreamfilter in den Puffer schreiben. Eine Lösung besteht in der Außerkraftsetzung **von DecideAllocator,** sodass das schreibgeschützte Flag auf **TRUE legt.** Der Einfachheit halber entfernt die neue Version die Optimierung jedoch ganz. Stattdessen füllt diese Version den Puffer jedes Mal mit Nullen auf.

### <a name="miscellaneous-changes"></a>Sonstige Änderungen

In der neuen Version werden diese beiden Zeilen aus dem CBall-Konstruktor entfernt:


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



Der ursprüngliche Ball-Filter verwendet diese Werte, um der Ursprünglichen Ballposition eine gewisse Zufälligkeit hinzuzufügen. Für unsere Zwecke möchten wir, dass die Kugel deterministisch ist. Außerdem wurden einige Variablen von [**CRefTime-Objekten**](creftime.md) in [**REFERENCE \_ TIME-Variablen**](reference-time.md) geändert. (Die **CRefTime-Klasse** ist ein schlanker Wrapper für einen **REFERENCE \_ TIME-Wert.)** Schließlich wurde die Implementierung von [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) geringfügig geändert. Weitere Informationen finden Sie im Quellcode.

## <a name="limitations-of-the-csourceseeking-class"></a>Einschränkungen der CSourceSeeking-Klasse

Die [**CSourceSeeking-Klasse**](csourceseeking.md) ist aufgrund von Problemen mit der übergreifenden Kommunikation nicht für Filter mit mehreren Ausgabepins gedacht. Stellen Sie sich beispielsweise einen Parserfilter vor, der einen überlappten Audio-Videostream empfängt, den Stream in seine Audio- und Videokomponenten aufteilt und Videos von einem Ausgabepin und Audiodaten von einem anderen liefert. Beide Ausgabepins empfangen jeden Suchbefehl, der Filter sollte jedoch nur einmal pro Suchbefehl suchen. Die Lösung besteht im Festlegen eines der Pins zum Steuern der Such- und Ignorieren von Suchbefehlen, die vom anderen Pin empfangen werden.

Nach dem Suchbefehl sollten jedoch beide Pins Daten leeren. Um dies noch komplizierter zu machen, erfolgt der Suchbefehl im Anwendungsthread, nicht im Streamingthread. Daher müssen Sie sicherstellen, dass keines der Pins blockiert ist und darauf warten, dass ein [**IMemInputPin::Receive-Aufruf**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) zurückerwartet wird, oder dass dies zu einem Deadlock führen kann. Weitere Informationen zum threadsicheren Leeren in Stecknadeln finden Sie unter [Threads und kritische Abschnitte](threads-and-critical-sections.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben von Quellfiltern](writing-source-filters.md)
</dt> </dl>

 

 



