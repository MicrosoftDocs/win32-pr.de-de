---
description: Die cpospassthru-Klasse verarbeitet Such Befehle für Transformations Filter, indem Sie vom Upstream an den nächsten Filter übergeben werden.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: Cpospassthru-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372077"
---
# <a name="cpospassthru-class"></a><span data-ttu-id="df0e8-103">Cpospassthru-Klasse</span><span class="sxs-lookup"><span data-stu-id="df0e8-103">CPosPassThru class</span></span>

![cpospassthru-Basisklassen Hierarchie](images/cutil14.png)

<span data-ttu-id="df0e8-105">Die- `CPosPassThru` Klasse verarbeitet Such Befehle für Transformations Filter, indem Sie vom Upstream an den nächsten Filter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="df0e8-105">The `CPosPassThru` class handles seek commands for transform filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="df0e8-106">Wenn eine Anwendung das Filter Diagramm sucht, übergibt der Filter Diagramm-Manager den rendererfiltern den Suchbefehl.</span><span class="sxs-lookup"><span data-stu-id="df0e8-106">When an application seeks the filter graph, the Filter Graph Manager gives the seek command to the renderer filters.</span></span> <span data-ttu-id="df0e8-107">Der Befehl wird über die Ausgabepin jedes Filters Upstream übergeben, bis ein Filter erreicht wird, der den Befehl ausführen kann (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="df0e8-107">The command is passed upstream, through each filter's output pin, until it reaches a filter that can execute the command (if any).</span></span> <span data-ttu-id="df0e8-108">Weitere Informationen finden Sie unter [Suchen](seeking.md).</span><span class="sxs-lookup"><span data-stu-id="df0e8-108">For details, see [Seeking](seeking.md).</span></span> <span data-ttu-id="df0e8-109">Die- `CPosPassThru` Klasse übergibt alle Suchbefehle an die Ausgabepin im upstreamfilter, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="df0e8-109">The `CPosPassThru` class passes all seek commands to the output pin on the upstream filter, as shown in the following diagram.</span></span>

![die cpospassthru-Klasse sendet Seek-Befehle Upstream.](images/cpospassthru.png)

<span data-ttu-id="df0e8-111">Obwohl diese Klasse in der Basisklassen Bibliothek bereitgestellt wird, stellt DirectShow auch dieselbe Klasse in Quartz.dll bereit.</span><span class="sxs-lookup"><span data-stu-id="df0e8-111">Although this class is provided in the base class library, DirectShow also provides the same class in Quartz.dll.</span></span> <span data-ttu-id="df0e8-112">Wenn Sie die Quartz.dll-Version verwenden, kann die Codegröße in Ihrem Filter einigermaßen reduziert werden, da die-Klasse zur Laufzeit aus der DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="df0e8-112">Using the Quartz.dll version can reduce the code size in your filter somewhat, because the class is loaded at run-time from the DLL.</span></span> <span data-ttu-id="df0e8-113">Um diese Version zu verwenden, müssen Sie [**die Funktion "**](createpospassthru.md) -Funktion" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df0e8-113">To use that version, call the [**CreatePosPassThru**](createpospassthru.md) function.</span></span>

<span data-ttu-id="df0e8-114">Delegieren Sie in der **nondelegatingqueryinterface** -Methode der Ausgabe-PIN immer dann an das **cpospassthru** -Objekt, wenn die angeforderte Schnittstelle [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) oder [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition)ist, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="df0e8-114">In your output pin's **NonDelegatingQueryInterface** method, delegate to the **CPosPassThru** object whenever the requested interface is [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) or [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), as shown in the following code:</span></span>


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



<span data-ttu-id="df0e8-115">Sofern nicht angegeben, rufen alle [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) -und [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Methoden in dieser Klasse die entsprechende Methode für die verbundene PIN auf und geben das Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="df0e8-115">Except where noted, all [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods in this class call the corresponding method on the connected pin and return the result.</span></span>



| <span data-ttu-id="df0e8-116">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="df0e8-116">Public Methods</span></span>                                                    | <span data-ttu-id="df0e8-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df0e8-117">Description</span></span>                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="df0e8-118">**Cpospassthru**</span><span class="sxs-lookup"><span data-stu-id="df0e8-118">**CPosPassThru**</span></span>](cpospassthru-cpospassthru.md)                 | <span data-ttu-id="df0e8-119">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="df0e8-119">Constructor method.</span></span>                                                                                 |
| [<span data-ttu-id="df0e8-120">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="df0e8-120">**ForceRefresh**</span></span>](cpospassthru-forcerefresh.md)                 | <span data-ttu-id="df0e8-121">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="df0e8-121">Obsolete.</span></span>                                                                                           |
| [<span data-ttu-id="df0e8-122">**Getmediatime**</span><span class="sxs-lookup"><span data-stu-id="df0e8-122">**GetMediaTime**</span></span>](cpospassthru-getmediatime.md)                 | <span data-ttu-id="df0e8-123">Ruft die Zeitstempel im aktuellen Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-123">Retrieves the time stamps on the current sample.</span></span> <span data-ttu-id="df0e8-124">Virtu.</span><span class="sxs-lookup"><span data-stu-id="df0e8-124">Virtual.</span></span>                                           |
| <span data-ttu-id="df0e8-125">Imediaposition-Methoden</span><span class="sxs-lookup"><span data-stu-id="df0e8-125">IMediaPosition Methods</span></span>                                            | <span data-ttu-id="df0e8-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df0e8-126">Description</span></span>                                                                                         |
| [<span data-ttu-id="df0e8-127">**\_Dauer erhalten**</span><span class="sxs-lookup"><span data-stu-id="df0e8-127">**get\_Duration**</span></span>](cpospassthru-get-duration.md)                | <span data-ttu-id="df0e8-128">Ruft die Dauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-128">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="df0e8-129">**\_CurrentPosition platzieren**</span><span class="sxs-lookup"><span data-stu-id="df0e8-129">**put\_CurrentPosition**</span></span>](cpospassthru-put-currentposition.md)  | <span data-ttu-id="df0e8-130">Legt die aktuelle Position relativ zur Gesamtdauer des Streams fest.</span><span class="sxs-lookup"><span data-stu-id="df0e8-130">Sets the current position, relative to the total duration of the stream.</span></span>                            |
| [<span data-ttu-id="df0e8-131">**\_Stopp Zeit erhalten**</span><span class="sxs-lookup"><span data-stu-id="df0e8-131">**get\_StopTime**</span></span>](cpospassthru-get-stoptime.md)                | <span data-ttu-id="df0e8-132">Ruft den Zeitpunkt ab, zu dem die Wiedergabe in Relation zur Dauer des Streams beendet wird.</span><span class="sxs-lookup"><span data-stu-id="df0e8-132">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="df0e8-133">**\_Stopp Zeit einfügen**</span><span class="sxs-lookup"><span data-stu-id="df0e8-133">**put\_StopTime**</span></span>](cpospassthru-put-stoptime.md)                | <span data-ttu-id="df0e8-134">Legt die Uhrzeit fest, zu der die Wiedergabe in Relation zur Dauer des Streams beendet wird.</span><span class="sxs-lookup"><span data-stu-id="df0e8-134">Sets the time at which the playback will stop, relative to the duration of the stream.</span></span>              |
| [<span data-ttu-id="df0e8-135">**\_vorab Zeit**</span><span class="sxs-lookup"><span data-stu-id="df0e8-135">**get\_PrerollTime**</span></span>](cpospassthru-get-prerolltime.md)          | <span data-ttu-id="df0e8-136">Ruft die Datenmenge ab, die vor der Startposition in die Warteschlange eingereiht wird.</span><span class="sxs-lookup"><span data-stu-id="df0e8-136">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="df0e8-137">**\_vorab Zeit festlegen**</span><span class="sxs-lookup"><span data-stu-id="df0e8-137">**put\_PrerollTime**</span></span>](cpospassthru-put-prerolltime.md)          | <span data-ttu-id="df0e8-138">Legt die Menge der Daten fest, die vor der Startposition in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="df0e8-138">Sets the amount of data that will be queued before the start position.</span></span>                              |
| [<span data-ttu-id="df0e8-139">**get- \_ Rate**</span><span class="sxs-lookup"><span data-stu-id="df0e8-139">**get\_Rate**</span></span>](cpospassthru-get-rate.md)                        | <span data-ttu-id="df0e8-140">Ruft die Wiedergabe Rate ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-140">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="df0e8-141">**Put- \_ Rate**</span><span class="sxs-lookup"><span data-stu-id="df0e8-141">**put\_Rate**</span></span>](cpospassthru-put-rate.md)                        | <span data-ttu-id="df0e8-142">Legt die Wiedergabe Rate fest.</span><span class="sxs-lookup"><span data-stu-id="df0e8-142">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="df0e8-143">**\_CurrentPosition erhalten**</span><span class="sxs-lookup"><span data-stu-id="df0e8-143">**get\_CurrentPosition**</span></span>](cpospassthru-get-currentposition.md)  | <span data-ttu-id="df0e8-144">Ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-144">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="df0e8-145">**Canseekforward**</span><span class="sxs-lookup"><span data-stu-id="df0e8-145">**CanSeekForward**</span></span>](cpospassthru-canseekforward.md)             | <span data-ttu-id="df0e8-146">Bestimmt, ob der Stream rückwärts Seeding durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="df0e8-146">Determines whether the stream can be seeked backward.</span></span>                                               |
| [<span data-ttu-id="df0e8-147">**Canseekabwärts**</span><span class="sxs-lookup"><span data-stu-id="df0e8-147">**CanSeekBackward**</span></span>](cpospassthru-canseekbackward.md)           | <span data-ttu-id="df0e8-148">Bestimmt, ob für den Datenstrom ein Seeding durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="df0e8-148">Determines whether the stream can be seeked forward.</span></span>                                                |
| <span data-ttu-id="df0e8-149">Imediaseeking-Methoden</span><span class="sxs-lookup"><span data-stu-id="df0e8-149">IMediaSeeking Methods</span></span>                                             | <span data-ttu-id="df0e8-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df0e8-150">Description</span></span>                                                                                         |
| [<span data-ttu-id="df0e8-151">**Prüffunktionen**</span><span class="sxs-lookup"><span data-stu-id="df0e8-151">**CheckCapabilities**</span></span>](cpospassthru-checkcapabilities.md)       | <span data-ttu-id="df0e8-152">Fragt ab, ob ein Stream Suchfunktionen angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="df0e8-152">Queries whether a stream has specified seeking capabilities.</span></span>                                        |
| [<span data-ttu-id="df0e8-153">**Converttimeformat**</span><span class="sxs-lookup"><span data-stu-id="df0e8-153">**ConvertTimeFormat**</span></span>](cpospassthru-converttimeformat.md)       | <span data-ttu-id="df0e8-154">Konvertiert von einem Zeitformat in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="df0e8-154">Converts from one time format to another.</span></span>                                                           |
| [<span data-ttu-id="df0e8-155">**Getavailable**</span><span class="sxs-lookup"><span data-stu-id="df0e8-155">**GetAvailable**</span></span>](cpospassthru-getavailable.md)                 | <span data-ttu-id="df0e8-156">Ruft den Zeitraum ab, in dem die Suche effizient ist.</span><span class="sxs-lookup"><span data-stu-id="df0e8-156">Retrieves the range of times in which seeking is efficient.</span></span>                                         |
| [<span data-ttu-id="df0e8-157">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="df0e8-157">**GetCapabilities**</span></span>](cpospassthru-getcapabilities.md)           | <span data-ttu-id="df0e8-158">Ruft alle Suchfunktionen des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-158">Retrieves all the seeking capabilities of the stream.</span></span>                                               |
| [<span data-ttu-id="df0e8-159">**Navigatorobjekt**</span><span class="sxs-lookup"><span data-stu-id="df0e8-159">**GetCurrentPosition**</span></span>](cpospassthru-getcurrentposition.md)     | <span data-ttu-id="df0e8-160">Ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-160">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="df0e8-161">**Getduration**</span><span class="sxs-lookup"><span data-stu-id="df0e8-161">**GetDuration**</span></span>](cpospassthru-getduration.md)                   | <span data-ttu-id="df0e8-162">Ruft die Dauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-162">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="df0e8-163">**Getpositions**</span><span class="sxs-lookup"><span data-stu-id="df0e8-163">**GetPositions**</span></span>](cpospassthru-getpositions.md)                 | <span data-ttu-id="df0e8-164">Ruft die aktuelle Position und die Position des Stopps relativ zur Gesamtdauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-164">Retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> |
| [<span data-ttu-id="df0e8-165">**Getpreroll**</span><span class="sxs-lookup"><span data-stu-id="df0e8-165">**GetPreroll**</span></span>](cpospassthru-getpreroll.md)                     | <span data-ttu-id="df0e8-166">Ruft die Datenmenge ab, die vor der Startposition in die Warteschlange eingereiht wird.</span><span class="sxs-lookup"><span data-stu-id="df0e8-166">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="df0e8-167">**Getrate**</span><span class="sxs-lookup"><span data-stu-id="df0e8-167">**GetRate**</span></span>](cpospassthru-getrate.md)                           | <span data-ttu-id="df0e8-168">Ruft die Wiedergabe Rate ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-168">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="df0e8-169">**Getstopposition**</span><span class="sxs-lookup"><span data-stu-id="df0e8-169">**GetStopPosition**</span></span>](cpospassthru-getstopposition.md)           | <span data-ttu-id="df0e8-170">Ruft den Zeitpunkt ab, zu dem die Wiedergabe in Relation zur Dauer des Streams beendet wird.</span><span class="sxs-lookup"><span data-stu-id="df0e8-170">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="df0e8-171">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="df0e8-171">**GetTimeFormat**</span></span>](cpospassthru-gettimeformat.md)               | <span data-ttu-id="df0e8-172">Ruft das aktuelle Zeitformat ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-172">Retrieves the current time format.</span></span>                                                                  |
| [<span data-ttu-id="df0e8-173">**Isformatsupported**</span><span class="sxs-lookup"><span data-stu-id="df0e8-173">**IsFormatSupported**</span></span>](cpospassthru-isformatsupported.md)       | <span data-ttu-id="df0e8-174">Bestimmt, ob ein angegebenes Zeitformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="df0e8-174">Determines whether a specified time format is supported.</span></span>                                            |
| [<span data-ttu-id="df0e8-175">**Isusingtimeformat**</span><span class="sxs-lookup"><span data-stu-id="df0e8-175">**IsUsingTimeFormat**</span></span>](cpospassthru-isusingtimeformat.md)       | <span data-ttu-id="df0e8-176">Bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.</span><span class="sxs-lookup"><span data-stu-id="df0e8-176">Determines whether a specified time format is the format currently in use.</span></span>                          |
| [<span data-ttu-id="df0e8-177">**Querypreferredformat**</span><span class="sxs-lookup"><span data-stu-id="df0e8-177">**QueryPreferredFormat**</span></span>](cpospassthru-querypreferredformat.md) | <span data-ttu-id="df0e8-178">Ruft das bevorzugte Zeitformat für den Stream ab.</span><span class="sxs-lookup"><span data-stu-id="df0e8-178">Retrieves the preferred time format for the stream.</span></span>                                                 |
| [<span data-ttu-id="df0e8-179">**Setpositions**</span><span class="sxs-lookup"><span data-stu-id="df0e8-179">**SetPositions**</span></span>](cpospassthru-setpositions.md)                 | <span data-ttu-id="df0e8-180">Legt die aktuelle Position und die Position des Stopps fest.</span><span class="sxs-lookup"><span data-stu-id="df0e8-180">Sets the current position and the stop position.</span></span>                                                    |
| [<span data-ttu-id="df0e8-181">**-Aktivität**</span><span class="sxs-lookup"><span data-stu-id="df0e8-181">**SetRate**</span></span>](cpospassthru-setrate.md)                           | <span data-ttu-id="df0e8-182">Legt die Wiedergabe Rate fest.</span><span class="sxs-lookup"><span data-stu-id="df0e8-182">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="df0e8-183">**Settimeformat**</span><span class="sxs-lookup"><span data-stu-id="df0e8-183">**SetTimeFormat**</span></span>](cpospassthru-settimeformat.md)               | <span data-ttu-id="df0e8-184">Legt das Zeitformat fest.</span><span class="sxs-lookup"><span data-stu-id="df0e8-184">Sets the time format.</span></span>                                                                               |
| <span data-ttu-id="df0e8-185">Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="df0e8-185">Helper Functions</span></span>                                                  | <span data-ttu-id="df0e8-186">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df0e8-186">Description</span></span>                                                                                         |
| [<span data-ttu-id="df0e8-187">**"Kreatepospassthru"**</span><span class="sxs-lookup"><span data-stu-id="df0e8-187">**CreatePosPassThru**</span></span>](createpospassthru.md)                    | <span data-ttu-id="df0e8-188">Erstellt ein- `CPosPassThru` oder [**crendererpospassthru**](crendererpospassthru.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="df0e8-188">Creates a `CPosPassThru` or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="df0e8-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df0e8-189">Requirements</span></span>



| <span data-ttu-id="df0e8-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df0e8-190">Requirement</span></span> | <span data-ttu-id="df0e8-191">Wert</span><span class="sxs-lookup"><span data-stu-id="df0e8-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df0e8-192">Header</span><span class="sxs-lookup"><span data-stu-id="df0e8-192">Header</span></span><br/>  | <dl> <span data-ttu-id="df0e8-193"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df0e8-193"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df0e8-194">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df0e8-194">Library</span></span><br/> | <dl> <span data-ttu-id="df0e8-195">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="df0e8-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




