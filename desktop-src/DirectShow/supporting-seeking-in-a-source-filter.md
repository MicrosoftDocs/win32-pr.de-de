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
# <a name="supporting-seeking-in-a-source-filter"></a><span data-ttu-id="db38b-104">Unterstützen der Suche in einem Quell Filter</span><span class="sxs-lookup"><span data-stu-id="db38b-104">Supporting Seeking in a Source Filter</span></span>

<span data-ttu-id="db38b-105">In diesem Thema wird beschrieben, wie Suchvorgänge in einem Microsoft DirectShow-Quell Filter implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="db38b-105">This topic describes how to implement seeking in a Microsoft DirectShow source filter.</span></span> <span data-ttu-id="db38b-106">Es verwendet das [Kugel Filter](ball-filter-sample.md) Beispiel als Ausgangspunkt und beschreibt den zusätzlichen Code, der erforderlich ist, um die Suche in diesem Filter zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="db38b-106">It uses the [Ball Filter](ball-filter-sample.md) sample as the starting point and describes the additional code needed to support seeking in this filter.</span></span>

<span data-ttu-id="db38b-107">Das [Kugel Filter](ball-filter-sample.md) Beispiel ist ein Quell Filter, der einen animierten Sprung-Ball erstellt.</span><span class="sxs-lookup"><span data-stu-id="db38b-107">The [Ball Filter](ball-filter-sample.md) sample is a source filter that creates an animated bouncing ball.</span></span> <span data-ttu-id="db38b-108">In diesem Artikel wird beschrieben, wie Sie diesem Filter Suchfunktionen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="db38b-108">This article describes how to add seeking functionality to this filter.</span></span> <span data-ttu-id="db38b-109">Nachdem Sie diese Funktionalität hinzugefügt haben, können Sie den Filter in GraphEdit Rendering und die Kugel steuern, indem Sie den Schieberegler GraphEdit ziehen.</span><span class="sxs-lookup"><span data-stu-id="db38b-109">Once you have added this functionality, you can render the filter in GraphEdit and control the ball by dragging the GraphEdit slider.</span></span>

<span data-ttu-id="db38b-110">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="db38b-110">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="db38b-111">Übersicht über das Suchen in DirectShow</span><span class="sxs-lookup"><span data-stu-id="db38b-111">Overview of Seeking in DirectShow</span></span>](#overview-of-seeking-in-directshow)
-   [<span data-ttu-id="db38b-112">Kurze Übersicht über den Kugel Filter</span><span class="sxs-lookup"><span data-stu-id="db38b-112">Quick Overview of the Ball Filter</span></span>](#quick-overview-of-the-ball-filter)
-   [<span data-ttu-id="db38b-113">Ändern des Kugel Filters für Suchvorgänge</span><span class="sxs-lookup"><span data-stu-id="db38b-113">Modifying the Ball Filter for Seeking</span></span>](#modifying-the-ball-filter-for-seeking)
-   [<span data-ttu-id="db38b-114">Einschränkungen der csourceseeking-Klasse</span><span class="sxs-lookup"><span data-stu-id="db38b-114">Limitations of the CSourceSeeking Class</span></span>](#limitations-of-the-csourceseeking-class)

## <a name="overview-of-seeking-in-directshow"></a><span data-ttu-id="db38b-115">Übersicht über das Suchen in DirectShow</span><span class="sxs-lookup"><span data-stu-id="db38b-115">Overview of Seeking in DirectShow</span></span>

<span data-ttu-id="db38b-116">Eine Anwendung sucht das Filter Diagramm, indem eine [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Methode für den Filter Graph-Manager aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="db38b-116">An application seeks the filter graph by calling an [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) method on the Filter Graph Manager.</span></span> <span data-ttu-id="db38b-117">Der Filter Graph-Manager verteilt dann den Aufruf an jeden Renderer im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="db38b-117">The Filter Graph Manager then distributes the call to every renderer in the graph.</span></span> <span data-ttu-id="db38b-118">Jeder Renderer sendet den upstreambefehl über die Ausgabe-PIN des nächsten upstreamfilters.</span><span class="sxs-lookup"><span data-stu-id="db38b-118">Each renderer sends the call upstream, through the output pin of the next upstream filter.</span></span> <span data-ttu-id="db38b-119">Der-Befehl durchläuft den Upstream, bis er einen Filter erreicht, der den Seek-Befehl ausführen kann, in der Regel einen Quell Filter oder einen Parserfilter.</span><span class="sxs-lookup"><span data-stu-id="db38b-119">The call travels upstream until it reaches a filter that can execute the seek command, typically a source filter or a parser filter.</span></span> <span data-ttu-id="db38b-120">Im allgemeinen verarbeitet der Filter, der die Zeitstempel durchführt, auch das suchen.</span><span class="sxs-lookup"><span data-stu-id="db38b-120">In general, the filter that originates the time stamps also handles seeking.</span></span>

<span data-ttu-id="db38b-121">Ein Filter antwortet wie folgt auf einen Suchbefehl:</span><span class="sxs-lookup"><span data-stu-id="db38b-121">A filter responds to a seek command as follows:</span></span>

1.  <span data-ttu-id="db38b-122">Der Filter leert das Diagramm.</span><span class="sxs-lookup"><span data-stu-id="db38b-122">The filter flushes the graph.</span></span> <span data-ttu-id="db38b-123">Dadurch werden alle veralteten Daten aus dem Diagramm gelöscht, was die Reaktionsfähigkeit verbessert.</span><span class="sxs-lookup"><span data-stu-id="db38b-123">This clears any stale data from graph, which improves responsiveness.</span></span> <span data-ttu-id="db38b-124">Andernfalls werden Stichproben, die vor dem Seek-Befehl gepuffert wurden, möglicherweise zugestellt.</span><span class="sxs-lookup"><span data-stu-id="db38b-124">Otherwise, samples that were buffered prior to the seek command might get delivered.</span></span>
2.  <span data-ttu-id="db38b-125">Mit dem Filter wird [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) aufgerufen, um Downstream-Filter über die neue Endzeit, die Startzeit und die Wiedergabe Rate zu informieren.</span><span class="sxs-lookup"><span data-stu-id="db38b-125">The filter calls [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) to inform downstream filters of the new stop time, start time, and playback rate.</span></span>
3.  <span data-ttu-id="db38b-126">Der Filter legt dann das Diskontinuität-Flag für das erste Beispiel nach dem Seek-Befehl fest.</span><span class="sxs-lookup"><span data-stu-id="db38b-126">The filter then sets the discontinuity flag on the first sample after the seek command.</span></span>

<span data-ttu-id="db38b-127">Zeitstempel beginnen mit 0 (null) nach jedem Seek-Befehl (einschließlich Raten Änderungen).</span><span class="sxs-lookup"><span data-stu-id="db38b-127">Time stamps start from zero after any seek command (including rate changes).</span></span>

## <a name="quick-overview-of-the-ball-filter"></a><span data-ttu-id="db38b-128">Kurze Übersicht über den Kugel Filter</span><span class="sxs-lookup"><span data-stu-id="db38b-128">Quick Overview of the Ball Filter</span></span>

<span data-ttu-id="db38b-129">Der Kugel Filter ist eine Push-Quelle. Dies bedeutet, dass ein Arbeits Thread verwendet wird, um Abtastungen im Gegensatz zu einer pullquelle bereitzustellen, die passiv darauf wartet, dass ein downstreamfilter Beispiele anfordert.</span><span class="sxs-lookup"><span data-stu-id="db38b-129">The Ball filter is a push source, which means that it uses a worker thread to deliver samples downstream, as opposed to a pull source, which passively waits for a downstream filter to request samples.</span></span> <span data-ttu-id="db38b-130">Der Kugel Filter wird aus der [**CSource**](csource.md) -Klasse erstellt, und die Ausgabe-PIN wird aus der [**csourcestream**](csourcestream.md) -Klasse erstellt.</span><span class="sxs-lookup"><span data-stu-id="db38b-130">The Ball filter is built from the [**CSource**](csource.md) class, and its output pin is built from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="db38b-131">Die **csourcestream** -Klasse erstellt den Arbeits Thread, der den Datenfluss steuert.</span><span class="sxs-lookup"><span data-stu-id="db38b-131">The **CSourceStream** class creates the worker thread that drives the flow of data.</span></span> <span data-ttu-id="db38b-132">Dieser Thread tritt in eine Schleife ein, die Beispiele aus der Zuweisung abruft, Sie mit Daten füllt und diese nach unten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="db38b-132">This thread enters a loop that gets samples from the allocator, fills them with data, and delivers them downstream.</span></span>

<span data-ttu-id="db38b-133">Der größte Teil der Aktion in [**csourcestream**](csourcestream.md) erfolgt in der [**csourcestream:: FillBuffer**](csourcestream-fillbuffer.md) -Methode, die von der abgeleiteten Klasse implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="db38b-133">Most of the action in [**CSourceStream**](csourcestream.md) happens in the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which the derived class implements.</span></span> <span data-ttu-id="db38b-134">Das Argument für diese Methode ist ein Zeiger auf das Beispiel, das übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="db38b-134">The argument to this method is a pointer to the sample to be delivered.</span></span> <span data-ttu-id="db38b-135">Die-Implementierung von **FillBuffer** des Kugel Filters Ruft die Adresse des Beispiel Puffers ab und zeichnet durch Festlegen einzelner Pixelwerte direkt in den Puffer.</span><span class="sxs-lookup"><span data-stu-id="db38b-135">The Ball filter's implementation of **FillBuffer** retrieves the address of the sample buffer and draws directly to the buffer by setting individual pixel values.</span></span> <span data-ttu-id="db38b-136">(Das Zeichnen erfolgt durch eine Hilfsklasse, cball, sodass Sie die Details zu Bittiefen, Paletten usw. ignorieren können.)</span><span class="sxs-lookup"><span data-stu-id="db38b-136">(The drawing is done by a helper class, CBall, so you can ignore the details regarding bit depths, palettes, and so forth.)</span></span>

## <a name="modifying-the-ball-filter-for-seeking"></a><span data-ttu-id="db38b-137">Ändern des Kugel Filters für Suchvorgänge</span><span class="sxs-lookup"><span data-stu-id="db38b-137">Modifying the Ball Filter for Seeking</span></span>

<span data-ttu-id="db38b-138">Um den Kugel Filter suchbar zu machen, verwenden Sie die [**csourceseeking**](csourceseeking.md) -Klasse, die für die Implementierung von suchen in Filtern mit einem Ausgabepin konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="db38b-138">To make the Ball filter seekable, use the [**CSourceSeeking**](csourceseeking.md) class, which is designed for implementing seeking in filters with one output pin.</span></span> <span data-ttu-id="db38b-139">Fügen Sie die **csourceseeking** -Klasse der Vererbungs Liste für die cballstream-Klasse hinzu:</span><span class="sxs-lookup"><span data-stu-id="db38b-139">Add the **CSourceSeeking** class to the inheritance list for the CBallStream class:</span></span>


```C++
class CBallStream :  // Defines the output pin.
    public CSourceStream, public CSourceSeeking
```



<span data-ttu-id="db38b-140">Außerdem müssen Sie einen Initialisierer für [**csourceseeking**](csourceseeking.md) zum cballstream-Konstruktor hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="db38b-140">Also, you will need to add an initializer for [**CSourceSeeking**](csourceseeking.md) to the CBallStream constructor:</span></span>


```C++
    CSourceSeeking(NAME("SeekBall"), (IPin*)this, phr, &m_cSharedState),
```



<span data-ttu-id="db38b-141">Diese Anweisung ruft den Basiskonstruktor für [**csourceseeking**](csourceseeking.md)auf.</span><span class="sxs-lookup"><span data-stu-id="db38b-141">This statement calls the base constructor for [**CSourceSeeking**](csourceseeking.md).</span></span> <span data-ttu-id="db38b-142">Bei den Parametern handelt es sich um einen Namen, einen Zeiger auf den besitzenden PIN, einen **HRESULT** -Wert und die Adresse eines kritischen Abschnitts Objekts.</span><span class="sxs-lookup"><span data-stu-id="db38b-142">The parameters are a name, a pointer to the owning pin, an **HRESULT** value, and the address of a critical section object.</span></span> <span data-ttu-id="db38b-143">Der Name wird nur zum Debuggen verwendet, und das [**Name**](name.md) -Makro wird in Einzelhandels Builds in eine leere Zeichenfolge kompiliert.</span><span class="sxs-lookup"><span data-stu-id="db38b-143">The name is used only for debugging, and the [**NAME**](name.md) macro compiles to an empty string in retail builds.</span></span> <span data-ttu-id="db38b-144">Die PIN erbt direkt **csourceseeking**, sodass der zweite Parameter ein Zeiger auf sich selbst ist, der in einen [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Zeiger umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="db38b-144">The pin directly inherits **CSourceSeeking**, so the second parameter is a pointer to itself, cast to an [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointer.</span></span> <span data-ttu-id="db38b-145">Der **HRESULT** -Wert wird in der aktuellen Version der Basisklassen ignoriert. die Kompatibilität mit früheren Versionen bleibt bestehen.</span><span class="sxs-lookup"><span data-stu-id="db38b-145">The **HRESULT** value is ignored in the current version of the base classes; it remains for compatibility with previous versions.</span></span> <span data-ttu-id="db38b-146">Der kritische Abschnitt schützt freigegebene Daten, z. b. die aktuelle Startzeit, Endzeit und Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="db38b-146">The critical section protects shared data, such as the current start time, stop time, and playback rate.</span></span>

<span data-ttu-id="db38b-147">Fügen Sie die folgende Anweisung im [**csourceseeking**](csourceseeking.md) -Konstruktor hinzu:</span><span class="sxs-lookup"><span data-stu-id="db38b-147">Add the following statement inside the [**CSourceSeeking**](csourceseeking.md) constructor:</span></span>


```C++
m_rtStop = 60 * UNITS;
```



<span data-ttu-id="db38b-148">Die *m \_ rtstoppt* -Variable gibt die Endzeit an.</span><span class="sxs-lookup"><span data-stu-id="db38b-148">The *m\_rtStop* variable specifies the stop time.</span></span> <span data-ttu-id="db38b-149">Standardmäßig ist der Wert \_ I64 \_ Max/2, der ungefähr 14.600 Jahre beträgt.</span><span class="sxs-lookup"><span data-stu-id="db38b-149">By default, the value is \_I64\_MAX / 2, which is approximately 14,600 years.</span></span> <span data-ttu-id="db38b-150">Die vorherige Anweisung legt den Wert auf einen konservativeren Wert von 60 Sekunden fest.</span><span class="sxs-lookup"><span data-stu-id="db38b-150">The previous statement sets it to a more conservative 60 seconds.</span></span>

<span data-ttu-id="db38b-151">Zwei zusätzliche Element Variablen müssen cballstream hinzugefügt werden:</span><span class="sxs-lookup"><span data-stu-id="db38b-151">Two additional member variables must be added to CBallStream:</span></span>


```C++
BOOL            m_bDiscontinuity; // If true, set the discontinuity flag.
REFERENCE_TIME  m_rtBallPosition; // Position of the ball. 
```



<span data-ttu-id="db38b-152">Nach jedem Seek-Befehl muss der Filter das Diskontinuität-Flag für das nächste Beispiel durch Aufrufen von [**imediasample:: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity)festlegen.</span><span class="sxs-lookup"><span data-stu-id="db38b-152">After every seek command, the filter must set the discontinuity flag on the next sample by calling [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity).</span></span> <span data-ttu-id="db38b-153">Diese wird von der *m \_ bdiscontinuity* -Variablen nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="db38b-153">The *m\_bDiscontinuity* variable will keep track of this.</span></span> <span data-ttu-id="db38b-154">Die *m \_ rtballposition* -Variable gibt die Position der Kugel innerhalb des Video Rahmens an.</span><span class="sxs-lookup"><span data-stu-id="db38b-154">The *m\_rtBallPosition* variable will specify the position of the ball within the video frame.</span></span> <span data-ttu-id="db38b-155">Der ursprüngliche Ball Filter berechnet die Position von der streamzeit, aber die streamzeit wird nach jedem Seek-Befehl auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="db38b-155">The original Ball filter calculates the position from the stream time, but the stream time resets to zero after each seek command.</span></span> <span data-ttu-id="db38b-156">In einem durchsuchbaren Datenstrom ist die absolute Position unabhängig von der streamzeit.</span><span class="sxs-lookup"><span data-stu-id="db38b-156">In a seekable stream, the absolute position is independent of the stream time.</span></span>

### <a name="queryinterface"></a><span data-ttu-id="db38b-157">QueryInterface</span><span class="sxs-lookup"><span data-stu-id="db38b-157">QueryInterface</span></span>

<span data-ttu-id="db38b-158">Die [**csourceseeking**](csourceseeking.md) -Klasse implementiert die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="db38b-158">The [**CSourceSeeking**](csourceseeking.md) class implements the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="db38b-159">Überschreiben Sie die [**nondelegatingqueryinterface**](cunknown-nondelegatingqueryinterface.md) -Methode, um diese Schnittstelle für Clients verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="db38b-159">To expose this interface to clients, override the [**NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) method:</span></span>


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



<span data-ttu-id="db38b-160">Die Methode wird aufgrund der Art und Weise, wie die DirectShow-Basisklassen Component Object Model (com)-Aggregation unterstützen, als "nondelegating" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="db38b-160">The method is called "NonDelegating" because of the way the DirectShow base classes support Component Object Model (COM) aggregation.</span></span> <span data-ttu-id="db38b-161">Weitere Informationen finden Sie im Thema "Gewusst wie: Implementieren von IUnknown" im DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="db38b-161">For more information, see the "How to Implement IUnknown" topic in the DirectShow SDK.</span></span>

### <a name="seeking-methods"></a><span data-ttu-id="db38b-162">Suchmethoden</span><span class="sxs-lookup"><span data-stu-id="db38b-162">Seeking Methods</span></span>

<span data-ttu-id="db38b-163">Die [**csourceseeking**](csourceseeking.md) -Klasse verwaltet mehrere Element Variablen im Zusammenhang mit der Suche.</span><span class="sxs-lookup"><span data-stu-id="db38b-163">The [**CSourceSeeking**](csourceseeking.md) class maintains several member variables relating to seeking.</span></span>



| <span data-ttu-id="db38b-164">Variable</span><span class="sxs-lookup"><span data-stu-id="db38b-164">Variable</span></span>          | <span data-ttu-id="db38b-165">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db38b-165">Description</span></span>   | <span data-ttu-id="db38b-166">Standardwert</span><span class="sxs-lookup"><span data-stu-id="db38b-166">Default Value</span></span>  |
|-------------------|---------------|----------------|
| <span data-ttu-id="db38b-167">*m \_ rtstart*</span><span class="sxs-lookup"><span data-stu-id="db38b-167">*m\_rtStart*</span></span>      | <span data-ttu-id="db38b-168">Startzeit</span><span class="sxs-lookup"><span data-stu-id="db38b-168">Start time</span></span>    | <span data-ttu-id="db38b-169">Zero</span><span class="sxs-lookup"><span data-stu-id="db38b-169">Zero</span></span>           |
| <span data-ttu-id="db38b-170">*m \_ rtstopps*</span><span class="sxs-lookup"><span data-stu-id="db38b-170">*m\_rtStop*</span></span>       | <span data-ttu-id="db38b-171">Endzeit</span><span class="sxs-lookup"><span data-stu-id="db38b-171">Stop time</span></span>     | <span data-ttu-id="db38b-172">\_I64 \_ Max/2</span><span class="sxs-lookup"><span data-stu-id="db38b-172">\_I64\_MAX / 2</span></span> |
| <span data-ttu-id="db38b-173">*m \_ drateseeking*</span><span class="sxs-lookup"><span data-stu-id="db38b-173">*m\_dRateSeeking*</span></span> | <span data-ttu-id="db38b-174">Wiedergabe Rate</span><span class="sxs-lookup"><span data-stu-id="db38b-174">Playback rate</span></span> | <span data-ttu-id="db38b-175">1.0</span><span class="sxs-lookup"><span data-stu-id="db38b-175">1.0</span></span>            |



 

<span data-ttu-id="db38b-176">Die [**csourceseeking**](csourceseeking.md) -Implementierung von [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) aktualisiert die Start-und Endzeiten und ruft dann zwei rein virtuelle Methoden für die abgeleitete Klasse [**csourceseeking:: changestart**](csourceseeking-changestart.md) und [**csourceseeking:: changestoppt**](csourceseeking-changestop.md)auf.</span><span class="sxs-lookup"><span data-stu-id="db38b-176">The [**CSourceSeeking**](csourceseeking.md) implementation of [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) updates the start and stop times, and then calls two pure virtual methods on the derived class, [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md) and [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md).</span></span> <span data-ttu-id="db38b-177">Die Implementierung von [**imediaseeking:: ctrate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) ist ähnlich: die Wiedergabe Rate wird aktualisiert, und anschließend wird die reine virtuelle Methode [**csourceseeking:: changerate**](csourceseeking-changerate.md)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="db38b-177">The implementation of [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) is similar: It updates the playback rate and then calls the pure virtual method [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="db38b-178">In jeder dieser virtuellen Methoden muss die PIN folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="db38b-178">In each of these virtual methods, the pin must do the following:</span></span>

1.  <span data-ttu-id="db38b-179">Aufrufen von [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) , um mit dem leeren von Daten zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="db38b-179">Call [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) to start flushing data.</span></span>
2.  <span data-ttu-id="db38b-180">Stoppt den streamingthread.</span><span class="sxs-lookup"><span data-stu-id="db38b-180">Halt the streaming thread.</span></span>
3.  <span data-ttu-id="db38b-181">Nennen Sie [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span><span class="sxs-lookup"><span data-stu-id="db38b-181">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>
4.  <span data-ttu-id="db38b-182">Starten Sie den streamingthread neu.</span><span class="sxs-lookup"><span data-stu-id="db38b-182">Restart the streaming thread.</span></span>
5.  <span data-ttu-id="db38b-183">Nennen Sie [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span><span class="sxs-lookup"><span data-stu-id="db38b-183">Call [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).</span></span>
6.  <span data-ttu-id="db38b-184">Legen Sie das Diskontinuität-Flag für das nächste Beispiel fest.</span><span class="sxs-lookup"><span data-stu-id="db38b-184">Set the discontinuity flag on the next sample.</span></span>

<span data-ttu-id="db38b-185">Die Reihenfolge dieser Schritte ist entscheidend, da der streamingthread blockiert werden kann, während er darauf wartet, ein Beispiel bereitzustellen oder ein neues Beispiel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="db38b-185">The order of these steps is crucial, because the streaming thread can block while it waits to deliver a sample or get a new sample.</span></span> <span data-ttu-id="db38b-186">Die [**beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode stellt sicher, dass der Streaminginhalt nicht blockiert wird und daher in Schritt 2 keinen Deadlock findet.</span><span class="sxs-lookup"><span data-stu-id="db38b-186">The [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method ensures that the streaming thread is not blocked and therefore will not deadlock in step 2.</span></span> <span data-ttu-id="db38b-187">Der [**endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Befehl informiert die downstreamfilter, dass neue Beispiele erwartet werden, sodass Sie nicht abgelehnt werden, wenn der Thread in Schritt 4 erneut gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="db38b-187">The [**EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) call informs the downstream filters to expect new samples, so they do not reject them when the thread starts again in step 4.</span></span>

<span data-ttu-id="db38b-188">Die folgende private Methode führt die Schritte 1 bis 4 aus:</span><span class="sxs-lookup"><span data-stu-id="db38b-188">The following private method performs steps 1 through 4:</span></span>


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



<span data-ttu-id="db38b-189">Wenn der streamingthread erneut gestartet wird, ruft er die [**csourcestream:: onthreadstartplay**](csourcestream-onthreadstartplay.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="db38b-189">When the streaming thread starts again, it calls the [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method.</span></span> <span data-ttu-id="db38b-190">Überschreiben Sie diese Methode, um die Schritte 5 und 6 auszuführen:</span><span class="sxs-lookup"><span data-stu-id="db38b-190">Override this method to perform steps 5 and 6:</span></span>


```C++
HRESULT CBallStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



<span data-ttu-id="db38b-191">Legen Sie in der [**changestart**](csourceseeking-changestart.md) -Methode die streamzeit auf 0 (null) und die Position der Kugel auf die neue Startzeit fest.</span><span class="sxs-lookup"><span data-stu-id="db38b-191">In the [**ChangeStart**](csourceseeking-changestart.md) method, set the stream time to zero and the position of the ball to the new start time.</span></span> <span data-ttu-id="db38b-192">Dann cballstream:: updatefromseek aufrufen:</span><span class="sxs-lookup"><span data-stu-id="db38b-192">Then call CBallStream::UpdateFromSeek:</span></span>


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



<span data-ttu-id="db38b-193">In der [**changeend**](csourceseeking-changestop.md) -Methode wird cballstream:: updatefromseek aufgerufen, wenn die neue Endzeit kleiner als die aktuelle Position ist.</span><span class="sxs-lookup"><span data-stu-id="db38b-193">In the [**ChangeStop**](csourceseeking-changestop.md) method, call CBallStream::UpdateFromSeek if the new stop time is less than the current position.</span></span> <span data-ttu-id="db38b-194">Andernfalls ist die Endzeit noch in der Zukunft, sodass es nicht erforderlich ist, das Diagramm zu leeren.</span><span class="sxs-lookup"><span data-stu-id="db38b-194">Otherwise, the stop time is still in the future, so there's no need to flush the graph.</span></span>


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



<span data-ttu-id="db38b-195">Bei Raten Änderungen legt die [**csourceseeking:: setRate**](csourceseeking-setrate.md) -Methode *m \_ drateseeking* auf den neuen Satz fest (verwerfen des alten Werts), bevor [**changerate**](csourceseeking-changerate.md)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="db38b-195">For rate changes, the [**CSourceSeeking::SetRate**](csourceseeking-setrate.md) method sets *m\_dRateSeeking* to the new rate (discarding the old value) before it calls [**ChangeRate**](csourceseeking-changerate.md).</span></span> <span data-ttu-id="db38b-196">Wenn der Aufrufer eine ungültige Rate gab – z. b. kleiner als 0 (null) – ist es zu spät, wenn der **changerate** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="db38b-196">Unfortunately, if the caller gave an invalid rate—for example, less than zero—it's too late by the time **ChangeRate** is called.</span></span> <span data-ttu-id="db38b-197">Eine Lösung besteht darin, **die-Aktivität** zu überschreiben und auf gültige Raten zu prüfen:</span><span class="sxs-lookup"><span data-stu-id="db38b-197">One solution is to override **SetRate** and check for valid rates:</span></span>


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



### <a name="drawing-in-the-buffer"></a><span data-ttu-id="db38b-198">Zeichnen im Puffer</span><span class="sxs-lookup"><span data-stu-id="db38b-198">Drawing in the Buffer</span></span>

<span data-ttu-id="db38b-199">Dies ist die geänderte Version von [**csourcestream:: FillBuffer**](csourcestream-fillbuffer.md), der Routine, die die Kugel in jedem Frame zeichnet:</span><span class="sxs-lookup"><span data-stu-id="db38b-199">Here is the modified version of [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md), the routine that draws the ball on each frame:</span></span>


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



<span data-ttu-id="db38b-200">Die wichtigsten Unterschiede zwischen dieser Version und der ursprünglichen Version sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="db38b-200">The major differences between this version and the original are the following:</span></span>

-   <span data-ttu-id="db38b-201">Wie bereits erwähnt, wird die *m \_ rtballposition* -Variable verwendet, um die Position der Kugel anstelle der streamzeit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="db38b-201">As mentioned earlier, the *m\_rtBallPosition* variable is used to set the position of the ball, rather than the stream time.</span></span>
-   <span data-ttu-id="db38b-202">Nach dem halten des kritischen Abschnitts prüft die Methode, ob die aktuelle Position die Endzeit überschreitet.</span><span class="sxs-lookup"><span data-stu-id="db38b-202">After holding the critical section, the method checks whether the current position exceeds the stop time.</span></span> <span data-ttu-id="db38b-203">Wenn dies der Fall ist, wird **S \_ false** zurückgegeben. Dadurch wird der Basisklasse signalisiert, das Senden von Daten zu beenden und eine Streamende Benachrichtigung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="db38b-203">If so, it returns **S\_FALSE**, which signals the base class to stop sending data and deliver an end-of-stream notification.</span></span>
-   <span data-ttu-id="db38b-204">Die Zeitstempel werden durch die aktuelle Rate dividiert.</span><span class="sxs-lookup"><span data-stu-id="db38b-204">The time stamps are divided by the current rate.</span></span>
-   <span data-ttu-id="db38b-205">Wenn *m \_ bdiscontinuity* auf **true** festgelegt ist, legt die-Methode das Diskontinuität-Flag für das Beispiel fest.</span><span class="sxs-lookup"><span data-stu-id="db38b-205">If *m\_bDiscontinuity* is **TRUE**, the method sets the discontinuity flag on the sample.</span></span>

<span data-ttu-id="db38b-206">Es gibt noch einen weiteren kleinen Unterschied.</span><span class="sxs-lookup"><span data-stu-id="db38b-206">There is another minor difference.</span></span> <span data-ttu-id="db38b-207">Da die ursprüngliche Version darauf basiert, dass genau ein Puffer vorhanden ist, füllt Sie den gesamten Puffer einmal mit Nullen auf, sobald das Streaming beginnt.</span><span class="sxs-lookup"><span data-stu-id="db38b-207">Because the original version relies on having exactly one buffer, it fills the entire buffer with zeroes once, when streaming begins.</span></span> <span data-ttu-id="db38b-208">Danach wird der Ball nur noch von seiner vorherigen Position gelöscht.</span><span class="sxs-lookup"><span data-stu-id="db38b-208">After that, it just erases the ball from its previous position.</span></span> <span data-ttu-id="db38b-209">Diese Optimierung zeigt jedoch einen geringfügigen Fehler im Ball Filter.</span><span class="sxs-lookup"><span data-stu-id="db38b-209">However, this optimization reveals a slight bug in the Ball filter.</span></span> <span data-ttu-id="db38b-210">Wenn die [**cbaseoutputpin::D ecidezuordcator**](cbaseoutputpin-decideallocator.md) -Methode [**IMemInputPin:: notifyzuweisung**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)aufruft, wird das schreibgeschützte Flag auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="db38b-210">When the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator), it sets the read-only flag to **FALSE**.</span></span> <span data-ttu-id="db38b-211">Folglich kann der Downstream-Filter in den Puffer schreiben.</span><span class="sxs-lookup"><span data-stu-id="db38b-211">As a result, the downstream filter is free to write on the buffer.</span></span> <span data-ttu-id="db38b-212">Eine Lösung besteht darin, **dezidezuordcator** zu überschreiben, sodass das Flag für schreibgeschützten Zugriff auf **true** festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="db38b-212">One solution is to override **DecideAllocator** so that it sets the read-only flag to **TRUE**.</span></span> <span data-ttu-id="db38b-213">Der Einfachheit halber entfernt die neue Version die Optimierung einfach ganz.</span><span class="sxs-lookup"><span data-stu-id="db38b-213">For simplicity, however, the new version simply removes the optimization altogether.</span></span> <span data-ttu-id="db38b-214">Stattdessen füllt diese Version den Puffer jedes Mal mit Nullen auf.</span><span class="sxs-lookup"><span data-stu-id="db38b-214">Instead, this version fills the buffer with zeroes each time.</span></span>

### <a name="miscellaneous-changes"></a><span data-ttu-id="db38b-215">Sonstige Änderungen</span><span class="sxs-lookup"><span data-stu-id="db38b-215">Miscellaneous Changes</span></span>

<span data-ttu-id="db38b-216">In der neuen Version werden diese beiden Zeilen aus dem cball-Konstruktor entfernt:</span><span class="sxs-lookup"><span data-stu-id="db38b-216">In the new version, these two lines are removed from the CBall constructor:</span></span>


```C++
    m_iRandX = rand();
    m_iRandY = rand();
```



<span data-ttu-id="db38b-217">Der ursprüngliche Kugel Filter verwendet diese Werte, um der Anfangs Ball Position etwas Zufälligkeit hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="db38b-217">The original Ball filter uses these values to add some randomness to the initial ball position.</span></span> <span data-ttu-id="db38b-218">Für unsere Zwecke soll die Kugel deterministisch sein.</span><span class="sxs-lookup"><span data-stu-id="db38b-218">For our purposes, we want the ball to be deterministic.</span></span> <span data-ttu-id="db38b-219">Außerdem wurden einige [**Variablen von den**](creftime.md) Objekten in [**Verweis \_ Zeit**](reference-time.md) Variablen geändert.</span><span class="sxs-lookup"><span data-stu-id="db38b-219">Also, some variables have been changed from [**CRefTime**](creftime.md) objects to [**REFERENCE\_TIME**](reference-time.md) variables.</span></span> <span data-ttu-id="db38b-220">(Die Klasse "- **Zeit** " ist ein schlanker Wrapper für einen **Verweis \_ Zeitwert** .) Schließlich wurde die Implementierung von [**iqualitycontrol:: notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) leicht geändert. Weitere Informationen finden Sie im Quellcode.</span><span class="sxs-lookup"><span data-stu-id="db38b-220">(The **CRefTime** class is a thin wrapper for a **REFERENCE\_TIME** value.) Lastly, the implementation of [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) has been modified slightly; you can refer to the source code for details.</span></span>

## <a name="limitations-of-the-csourceseeking-class"></a><span data-ttu-id="db38b-221">Einschränkungen der csourceseeking-Klasse</span><span class="sxs-lookup"><span data-stu-id="db38b-221">Limitations of the CSourceSeeking Class</span></span>

<span data-ttu-id="db38b-222">Die [**csourceseeking**](csourceseeking.md) -Klasse ist aufgrund von Problemen mit der Kreuz-Pin-Kommunikation nicht für Filter mit mehreren Ausgabe Pins gedacht.</span><span class="sxs-lookup"><span data-stu-id="db38b-222">The [**CSourceSeeking**](csourceseeking.md) class is not meant for filters with multiple output pins, because of issues with cross-pin communication.</span></span> <span data-ttu-id="db38b-223">Stellen Sie sich z. b. einen Parserfilter vor, der einen überlappenden audiovideostream empfängt, den Stream in seine Audio-und Videokomponenten unterteilt und Video aus einer Ausgabe-PIN und aus einer anderen Audiodatei übermittelt.</span><span class="sxs-lookup"><span data-stu-id="db38b-223">For example, imagine a parser filter that receives an interleaved audio-video stream, splits the stream into its audio and video components, and delivers video from one output pin and audio from another.</span></span> <span data-ttu-id="db38b-224">Beide Ausgabe Pins empfangen jeden Seek-Befehl, aber der Filter sollte nur einmal pro Seek-Befehl suchen.</span><span class="sxs-lookup"><span data-stu-id="db38b-224">Both output pins will receive every seek command, but the filter should seek only once per seek command.</span></span> <span data-ttu-id="db38b-225">Die Lösung besteht darin, einen der Pins zum Steuern der Suche und zum Ignorieren von Seek-Befehlen festzulegen, die von der anderen Pin empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="db38b-225">The solution is to designate one of the pins to control seeking and to ignore seek commands received by the other pin.</span></span>

<span data-ttu-id="db38b-226">Nach dem Seek-Befehl sollten jedoch beide Pins Daten leeren.</span><span class="sxs-lookup"><span data-stu-id="db38b-226">After the seek command, however, both pins should flush data.</span></span> <span data-ttu-id="db38b-227">Um das Problem weiter zu erschweren, geschieht der Seek-Befehl im Anwendungs Thread, nicht im streamingthread.</span><span class="sxs-lookup"><span data-stu-id="db38b-227">To complicate matters further, the seek command happens on the application thread, not the streaming thread.</span></span> <span data-ttu-id="db38b-228">Daher müssen Sie sicherstellen, dass keine PIN blockiert ist und darauf wartet, dass ein [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Befehl zurückgegeben wird, oder es kann zu einem Deadlock führen.</span><span class="sxs-lookup"><span data-stu-id="db38b-228">Therefore, you must make certain that neither pin is blocked and waiting for a [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call to return, or it might cause a deadlock.</span></span> <span data-ttu-id="db38b-229">Weitere Informationen zur Thread sicheren Leerung in Pins finden Sie unter [Threads und kritische Abschnitte](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="db38b-229">For more information about thread-safe flushing in pins, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="db38b-230">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db38b-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db38b-231">Schreiben von Quell Filtern</span><span class="sxs-lookup"><span data-stu-id="db38b-231">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 



