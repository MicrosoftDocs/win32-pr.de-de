---
description: Die csourceseeking-Klasse ist eine abstrakte Klasse für die Implementierung von suchen in Quell Filtern mit einem Ausgabepin.
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: Csourceseeking-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364748"
---
# <a name="csourceseeking-class"></a><span data-ttu-id="f2a61-103">Csourceseeking-Klasse</span><span class="sxs-lookup"><span data-stu-id="f2a61-103">CSourceSeeking class</span></span>

![csourceseeking-Klassenhierarchie](images/cutil15.png)

<span data-ttu-id="f2a61-105">Die **csourceseeking** -Klasse ist eine abstrakte Klasse für die Implementierung von suchen in Quell Filtern mit einem Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="f2a61-105">The **CSourceSeeking** class is an abstract class for implementing seeking in source filters with one output pin.</span></span>

<span data-ttu-id="f2a61-106">Diese Klasse unterstützt die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f2a61-106">This class supports the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="f2a61-107">Sie stellt Standard Implementierungen für alle **imediaseeking** -Methoden bereit.</span><span class="sxs-lookup"><span data-stu-id="f2a61-107">It provides default implementations for all of the **IMediaSeeking** methods.</span></span> <span data-ttu-id="f2a61-108">Geschützte Member-Variablen speichern die Startzeit, die Endzeit und die aktuelle Rate.</span><span class="sxs-lookup"><span data-stu-id="f2a61-108">Protected member variables store the start time, stop time, and current rate.</span></span> <span data-ttu-id="f2a61-109">Standardmäßig ist das von der-Klasse unterstützte Zeitformat **Zeit \_ Format \_ Medien \_ Zeit** (100-Nanosecond-Einheiten).</span><span class="sxs-lookup"><span data-stu-id="f2a61-109">By default, the only time format supported by the class is **TIME\_FORMAT\_MEDIA\_TIME** (100-nanosecond units).</span></span> <span data-ttu-id="f2a61-110">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f2a61-110">See Remarks for more information.</span></span>



| <span data-ttu-id="f2a61-111">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="f2a61-111">Protected Member Variables</span></span>                                          | <span data-ttu-id="f2a61-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2a61-112">Description</span></span>                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2a61-113">**m \_ rtduration**</span><span class="sxs-lookup"><span data-stu-id="f2a61-113">**m\_rtDuration**</span></span>](csourceseeking-m-rtduration.md)                | <span data-ttu-id="f2a61-114">Dauer des Streams.</span><span class="sxs-lookup"><span data-stu-id="f2a61-114">Duration of the stream.</span></span>                                                                     |
| [<span data-ttu-id="f2a61-115">**m \_ rtstart**</span><span class="sxs-lookup"><span data-stu-id="f2a61-115">**m\_rtStart**</span></span>](csourceseeking-m-rtstart.md)                      | <span data-ttu-id="f2a61-116">Startzeit.</span><span class="sxs-lookup"><span data-stu-id="f2a61-116">Start time.</span></span>                                                                                 |
| [<span data-ttu-id="f2a61-117">**m \_ rtstopps**</span><span class="sxs-lookup"><span data-stu-id="f2a61-117">**m\_rtStop**</span></span>](csourceseeking-m-rtstop.md)                        | <span data-ttu-id="f2a61-118">Endzeit.</span><span class="sxs-lookup"><span data-stu-id="f2a61-118">Stop time.</span></span>                                                                                  |
| [<span data-ttu-id="f2a61-119">**m \_ drateseeking**</span><span class="sxs-lookup"><span data-stu-id="f2a61-119">**m\_dRateSeeking**</span></span>](csourceseeking-m-drateseeking.md)            | <span data-ttu-id="f2a61-120">Wiedergabe Rate.</span><span class="sxs-lookup"><span data-stu-id="f2a61-120">Playback rate.</span></span>                                                                              |
| [<span data-ttu-id="f2a61-121">**m \_ dwseekingcaps**</span><span class="sxs-lookup"><span data-stu-id="f2a61-121">**m\_dwSeekingCaps**</span></span>](csourceseeking-m-dwseekingcaps.md)          | <span data-ttu-id="f2a61-122">Suchfunktionen.</span><span class="sxs-lookup"><span data-stu-id="f2a61-122">Seeking capabilities.</span></span>                                                                       |
| [<span data-ttu-id="f2a61-123">**m \_ Plock**</span><span class="sxs-lookup"><span data-stu-id="f2a61-123">**m\_pLock**</span></span>](csourceseeking-m-plock.md)                          | <span data-ttu-id="f2a61-124">Zeiger auf ein kritisches Abschnitts Objekt, das gesperrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2a61-124">Pointer to a critical section object for locking.</span></span>                                           |
| <span data-ttu-id="f2a61-125">Geschützte Methoden</span><span class="sxs-lookup"><span data-stu-id="f2a61-125">Protected Methods</span></span>                                                   | <span data-ttu-id="f2a61-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2a61-126">Description</span></span>                                                                                 |
| [<span data-ttu-id="f2a61-127">**Csourceseeking**</span><span class="sxs-lookup"><span data-stu-id="f2a61-127">**CSourceSeeking**</span></span>](csourceseeking-csourceseeking.md)             | <span data-ttu-id="f2a61-128">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f2a61-128">Constructor method.</span></span>                                                                         |
| <span data-ttu-id="f2a61-129">Reine virtuelle Methoden</span><span class="sxs-lookup"><span data-stu-id="f2a61-129">Pure Virtual Methods</span></span>                                                | <span data-ttu-id="f2a61-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2a61-130">Description</span></span>                                                                                 |
| [<span data-ttu-id="f2a61-131">**Changerate**</span><span class="sxs-lookup"><span data-stu-id="f2a61-131">**ChangeRate**</span></span>](csourceseeking-changerate.md)                     | <span data-ttu-id="f2a61-132">Wird aufgerufen, wenn sich die Wiedergabe Rate ändert.</span><span class="sxs-lookup"><span data-stu-id="f2a61-132">Called when the playback rate changes.</span></span>                                                      |
| [<span data-ttu-id="f2a61-133">**Ändern**</span><span class="sxs-lookup"><span data-stu-id="f2a61-133">**ChangeStart**</span></span>](csourceseeking-changestart.md)                   | <span data-ttu-id="f2a61-134">Wird aufgerufen, wenn die Startposition geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f2a61-134">Called when the start position changes.</span></span>                                                     |
| [<span data-ttu-id="f2a61-135">**Changestoppt**</span><span class="sxs-lookup"><span data-stu-id="f2a61-135">**ChangeStop**</span></span>](csourceseeking-changestop.md)                     | <span data-ttu-id="f2a61-136">Wird aufgerufen, wenn die Position des Stopps geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f2a61-136">Called when the stop position changes.</span></span>                                                      |
| <span data-ttu-id="f2a61-137">Imediaseeking-Methoden</span><span class="sxs-lookup"><span data-stu-id="f2a61-137">IMediaSeeking Methods</span></span>                                               | <span data-ttu-id="f2a61-138">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2a61-138">Description</span></span>                                                                                 |
| [<span data-ttu-id="f2a61-139">**Isformatsupported**</span><span class="sxs-lookup"><span data-stu-id="f2a61-139">**IsFormatSupported**</span></span>](csourceseeking-isformatsupported.md)       | <span data-ttu-id="f2a61-140">Bestimmt, ob ein angegebenes Zeitformat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f2a61-140">Determines whether a specified time format is supported.</span></span>                                    |
| [<span data-ttu-id="f2a61-141">**Querypreferredformat**</span><span class="sxs-lookup"><span data-stu-id="f2a61-141">**QueryPreferredFormat**</span></span>](csourceseeking-querypreferredformat.md) | <span data-ttu-id="f2a61-142">Ruft das bevorzugte Zeitformat des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="f2a61-142">Retrieves the object's preferred time format.</span></span>                                               |
| [<span data-ttu-id="f2a61-143">**Settimeformat**</span><span class="sxs-lookup"><span data-stu-id="f2a61-143">**SetTimeFormat**</span></span>](csourceseeking-settimeformat.md)               | <span data-ttu-id="f2a61-144">Legt das Zeitformat fest.</span><span class="sxs-lookup"><span data-stu-id="f2a61-144">Sets the time format.</span></span>                                                                       |
| [<span data-ttu-id="f2a61-145">**Isusingtimeformat**</span><span class="sxs-lookup"><span data-stu-id="f2a61-145">**IsUsingTimeFormat**</span></span>](csourceseeking-isusingtimeformat.md)       | <span data-ttu-id="f2a61-146">Bestimmt, ob ein angegebenes Zeitformat das derzeit verwendete Format ist.</span><span class="sxs-lookup"><span data-stu-id="f2a61-146">Determines whether a specified time format is the format currently in use.</span></span>                  |
| [<span data-ttu-id="f2a61-147">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f2a61-147">**GetTimeFormat**</span></span>](csourceseeking-gettimeformat.md)               | <span data-ttu-id="f2a61-148">Ruft das aktuelle Zeitformat ab.</span><span class="sxs-lookup"><span data-stu-id="f2a61-148">Retrieves the current time format.</span></span>                                                          |
| [<span data-ttu-id="f2a61-149">**Getduration**</span><span class="sxs-lookup"><span data-stu-id="f2a61-149">**GetDuration**</span></span>](csourceseeking-getduration.md)                   | <span data-ttu-id="f2a61-150">Ruft die Dauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="f2a61-150">Retrieves the duration of the stream.</span></span>                                                       |
| [<span data-ttu-id="f2a61-151">**Getstopposition**</span><span class="sxs-lookup"><span data-stu-id="f2a61-151">**GetStopPosition**</span></span>](csourceseeking-getstopposition.md)           | <span data-ttu-id="f2a61-152">Ruft den Zeitpunkt ab, zu dem die Wiedergabe in Relation zur Dauer des Streams beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2a61-152">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> |
| [<span data-ttu-id="f2a61-153">**Navigatorobjekt**</span><span class="sxs-lookup"><span data-stu-id="f2a61-153">**GetCurrentPosition**</span></span>](csourceseeking-getcurrentposition.md)     | <span data-ttu-id="f2a61-154">Ruft die aktuelle Position relativ zur Gesamtdauer des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="f2a61-154">Retrieves the current position, relative to the total duration of the stream.</span></span>               |
| [<span data-ttu-id="f2a61-155">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f2a61-155">**GetCapabilities**</span></span>](csourceseeking-getcapabilities.md)           | <span data-ttu-id="f2a61-156">Ruft alle Suchfunktionen des Streams ab.</span><span class="sxs-lookup"><span data-stu-id="f2a61-156">Retrieves all the seeking capabilities of the stream.</span></span>                                       |
| [<span data-ttu-id="f2a61-157">**Prüffunktionen**</span><span class="sxs-lookup"><span data-stu-id="f2a61-157">**CheckCapabilities**</span></span>](csourceseeking-checkcapabilities.md)       | <span data-ttu-id="f2a61-158">Fragt ab, ob der Stream Suchfunktionen angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f2a61-158">Queries whether the stream has specified seeking capabilities.</span></span>                              |
| [<span data-ttu-id="f2a61-159">**Converttimeformat**</span><span class="sxs-lookup"><span data-stu-id="f2a61-159">**ConvertTimeFormat**</span></span>](csourceseeking-converttimeformat.md)       | <span data-ttu-id="f2a61-160">Konvertiert von einem Zeitformat in ein anderes.</span><span class="sxs-lookup"><span data-stu-id="f2a61-160">Converts from one time format to another.</span></span>                                                   |
| [<span data-ttu-id="f2a61-161">**Setpositions**</span><span class="sxs-lookup"><span data-stu-id="f2a61-161">**SetPositions**</span></span>](csourceseeking-setpositions.md)                 | <span data-ttu-id="f2a61-162">Legt die aktuelle Position und die Position des Stopps fest.</span><span class="sxs-lookup"><span data-stu-id="f2a61-162">Sets the current position and the stop position.</span></span>                                            |
| [<span data-ttu-id="f2a61-163">**Getpositions**</span><span class="sxs-lookup"><span data-stu-id="f2a61-163">**GetPositions**</span></span>](csourceseeking-getpositions.md)                 | <span data-ttu-id="f2a61-164">Ruft die aktuelle Position und die Position des Stopps ab.</span><span class="sxs-lookup"><span data-stu-id="f2a61-164">Retrieves the current position and the stop position.</span></span>                                       |
| [<span data-ttu-id="f2a61-165">**Getavailable**</span><span class="sxs-lookup"><span data-stu-id="f2a61-165">**GetAvailable**</span></span>](csourceseeking-getavailable.md)                 | <span data-ttu-id="f2a61-166">Ruft den Zeitraum ab, in dem die Suche effizient ist.</span><span class="sxs-lookup"><span data-stu-id="f2a61-166">Retrieves the range of times in which seeking is efficient.</span></span>                                 |
| [<span data-ttu-id="f2a61-167">**-Aktivität**</span><span class="sxs-lookup"><span data-stu-id="f2a61-167">**SetRate**</span></span>](csourceseeking-setrate.md)                           | <span data-ttu-id="f2a61-168">Legt die Wiedergabe Rate fest.</span><span class="sxs-lookup"><span data-stu-id="f2a61-168">Sets the playback rate.</span></span>                                                                     |
| [<span data-ttu-id="f2a61-169">**Getrate**</span><span class="sxs-lookup"><span data-stu-id="f2a61-169">**GetRate**</span></span>](csourceseeking-getrate.md)                           | <span data-ttu-id="f2a61-170">Ruft die Wiedergabe Rate ab.</span><span class="sxs-lookup"><span data-stu-id="f2a61-170">Retrieves the playback rate.</span></span>                                                                |
| [<span data-ttu-id="f2a61-171">**Getpreroll**</span><span class="sxs-lookup"><span data-stu-id="f2a61-171">**GetPreroll**</span></span>](csourceseeking-getpreroll.md)                     | <span data-ttu-id="f2a61-172">Ruft die Vorabversion ab.</span><span class="sxs-lookup"><span data-stu-id="f2a61-172">Retrieves the preroll time.</span></span>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f2a61-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2a61-173">Remarks</span></span>

<span data-ttu-id="f2a61-174">Wenn sich die Anfangsposition, die Position der Position oder die Wiedergabe Rate ändert, ruft das **csourceseeking** -Objekt eine entsprechende rein virtuelle Methode auf:</span><span class="sxs-lookup"><span data-stu-id="f2a61-174">Whenever the start position, stop position, or playback rate changes, the **CSourceSeeking** object calls a corresponding pure virtual method:</span></span>

-   <span data-ttu-id="f2a61-175">Start Position: [ **csourceseeking:: changestart**](csourceseeking-changestart.md)</span><span class="sxs-lookup"><span data-stu-id="f2a61-175">Start position: [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)</span></span>
-   <span data-ttu-id="f2a61-176">Position des Stopps: [ **csourceseeking:: changestoppt**](csourceseeking-changestop.md)</span><span class="sxs-lookup"><span data-stu-id="f2a61-176">Stop position: [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md)</span></span>
-   <span data-ttu-id="f2a61-177">Wiedergabe Rate: [ **csourceseeking:: changerate**](csourceseeking-changerate.md)</span><span class="sxs-lookup"><span data-stu-id="f2a61-177">Playback rate: [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md)</span></span>

<span data-ttu-id="f2a61-178">Diese Methoden müssen von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="f2a61-178">The derived class must implement these methods.</span></span> <span data-ttu-id="f2a61-179">Nach jedem Suchvorgang muss ein Filter folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="f2a61-179">After any seek operation, a filter must do the following:</span></span>

1.  <span data-ttu-id="f2a61-180">Aufrufen der [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode für die downstreameingabepin.</span><span class="sxs-lookup"><span data-stu-id="f2a61-180">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the downstream input pin.</span></span>
2.  <span data-ttu-id="f2a61-181">Stoppt den Arbeits Thread, der Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f2a61-181">Halt the worker thread that is delivering data.</span></span>
3.  <span data-ttu-id="f2a61-182">Ruft die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="f2a61-182">Call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>
4.  <span data-ttu-id="f2a61-183">Starten Sie den Arbeits Thread neu.</span><span class="sxs-lookup"><span data-stu-id="f2a61-183">Restart the worker thread.</span></span>
5.  <span data-ttu-id="f2a61-184">Ruft die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="f2a61-184">Call the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>
6.  <span data-ttu-id="f2a61-185">Legen Sie die Diskontinuität-Eigenschaft im ersten Beispiel fest.</span><span class="sxs-lookup"><span data-stu-id="f2a61-185">Set the discontinuity property on the first sample.</span></span> <span data-ttu-id="f2a61-186">Aufrufen der [**imediasample:: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f2a61-186">Call the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="f2a61-187">Der Aufrufen von [**beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) gibt den Arbeits Thread frei, wenn der Thread blockiert wird, um ein Beispiel zu liefern.</span><span class="sxs-lookup"><span data-stu-id="f2a61-187">The call to [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) frees the worker thread, if the thread is blocked waiting to deliver a sample.</span></span>

<span data-ttu-id="f2a61-188">Stellen Sie in Schritt 2 sicher, dass der Thread das Senden von Daten beendet hat.</span><span class="sxs-lookup"><span data-stu-id="f2a61-188">In step 2, make sure that the thread has stopped sending data.</span></span> <span data-ttu-id="f2a61-189">Abhängig von der Implementierung müssen Sie möglicherweise warten, bis der Thread beendet wird, oder wenn der Thread eine Antwort einer Art signalisiert.</span><span class="sxs-lookup"><span data-stu-id="f2a61-189">Depending on the implementation, you might need to wait for the thread to exit, or for the thread to signal a response of some kind.</span></span> <span data-ttu-id="f2a61-190">Wenn der Filter die [**csourcestream**](csourcestream.md) -Klasse verwendet, blockiert die [**csourcestream:: stoppt**](csourcestream-stop.md) -Methode, bis der Arbeits Thread antwortet.</span><span class="sxs-lookup"><span data-stu-id="f2a61-190">If your filter uses the [**CSourceStream**](csourcestream.md) class, the [**CSourceStream::Stop**](csourcestream-stop.md) method blocks until the worker thread replies.</span></span>

<span data-ttu-id="f2a61-191">Idealerweise sollte das neue Segment (Schritt 5) vom Arbeits Thread übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="f2a61-191">Ideally, the new segment (step 5) should be delivered from the worker thread.</span></span> <span data-ttu-id="f2a61-192">Dies kann auch durch das **csourceseeking** -Objekt erfolgen, sofern der Filter es mit den Beispielen serialisiert.</span><span class="sxs-lookup"><span data-stu-id="f2a61-192">It can also be done by the **CSourceSeeking** object, as long as the filter serializes it with the samples.</span></span>

<span data-ttu-id="f2a61-193">Das folgende Beispiel zeigt eine mögliche Implementierung.</span><span class="sxs-lookup"><span data-stu-id="f2a61-193">The following example shows a possible implementation.</span></span> <span data-ttu-id="f2a61-194">Dabei wird davon ausgegangen, dass die Ausgabepin des Quell Filters von **csourceseeking** und [**csourcestream**](csourcestream.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="f2a61-194">It assumes that the source filter's output pin is derived from **CSourceSeeking** and [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="f2a61-195">In diesem Beispiel wird die Hilfsmethode updatefromseek definiert, mit der die Schritte 1 4 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f2a61-195">This example defines a helper method, UpdateFromSeek, that performs steps 1 4.</span></span> <span data-ttu-id="f2a61-196">Die [**csourcestream:: onthreadstartplay**](csourcestream-onthreadstartplay.md) -Methode wird überschrieben, um das neue Segment zu senden, und um ein Flag festzulegen, das die Diskontinuität angibt.</span><span class="sxs-lookup"><span data-stu-id="f2a61-196">The [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method is overridden to send the new segment, and to set a flag indicating the discontinuity.</span></span> <span data-ttu-id="f2a61-197">Der Arbeits Thread übernimmt dieses Flag und ruft die [**imediasample:: setdiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) -Methode auf:</span><span class="sxs-lookup"><span data-stu-id="f2a61-197">The worker thread picks up this flag and calls the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method:</span></span>


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a><span data-ttu-id="f2a61-198">Unterstützung zusätzlicher Zeitformate</span><span class="sxs-lookup"><span data-stu-id="f2a61-198">Supporting Additional Time Formats</span></span>

<span data-ttu-id="f2a61-199">Standardmäßig unterstützt diese Klasse das suchen nur in Einheiten der Bezugszeit (Zeit \_ Format \_ Medien \_ Zeit).</span><span class="sxs-lookup"><span data-stu-id="f2a61-199">By default, this class supports seeking only in units of reference time (TIME\_FORMAT\_MEDIA\_TIME).</span></span> <span data-ttu-id="f2a61-200">Um zusätzliche Zeitformate zu unterstützen, überschreiben Sie die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Methoden, die sich mit Zeitformaten befassen:</span><span class="sxs-lookup"><span data-stu-id="f2a61-200">To support additional time formats, override the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods that deal with time formats:</span></span>

-   [<span data-ttu-id="f2a61-201">**Imediaseeking:: getTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f2a61-201">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="f2a61-202">**Imediaseeking:: getTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f2a61-202">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="f2a61-203">**Imediaseeking:: isusingtimeformat**</span><span class="sxs-lookup"><span data-stu-id="f2a61-203">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="f2a61-204">**Imediaseeking:: isusingtimeformat**</span><span class="sxs-lookup"><span data-stu-id="f2a61-204">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="f2a61-205">**Imediaseeking:: settimeformat**</span><span class="sxs-lookup"><span data-stu-id="f2a61-205">**IMediaSeeking::SetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

<span data-ttu-id="f2a61-206">Überschreiben Sie außerdem die verbleibenden [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Methoden, um die erforderlichen Konvertierungen Zwischenzeit Formaten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f2a61-206">In addition, override the remaining [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods to perform the necessary conversions between time formats.</span></span> <span data-ttu-id="f2a61-207">Nachdem die [**settimeformat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) -Methode aufgerufen wurde, müssen alle **imediaseeking** -Methoden die eingehenden und ausgehenden Zeitparameter als im neuen Zeitformat behandeln.</span><span class="sxs-lookup"><span data-stu-id="f2a61-207">After the [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method is called, all **IMediaSeeking** methods must treat incoming and outgoing time parameters as being in the new time format.</span></span> <span data-ttu-id="f2a61-208">Wenn die Variable " *m \_ rtduration* " z. b. die Dauer in Einheiten der Verweis Zeit darstellt, das aktuelle Zeitformat aber Frames ist, muss die [**getduration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) -Methode den Wert " *m \_ rtduration* " zurückgeben, der in Frames konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="f2a61-208">For example, if the *m\_rtDuration* variable represents the duration in units of reference time, but the current time format is frames, then the [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method must return the value *m\_rtDuration* converted to frames.</span></span> <span data-ttu-id="f2a61-209">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f2a61-209">For example:</span></span>


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



<span data-ttu-id="f2a61-210">Stellen Sie außerdem sicher, dass Sie \_ \_ in der [**imediaseeking:: setpositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) -Methode auf das Flag zum Suchen von returntime achten.</span><span class="sxs-lookup"><span data-stu-id="f2a61-210">Also, make sure to check for the AM\_SEEKING\_ReturnTime flag in the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span> <span data-ttu-id="f2a61-211">Wenn dieses Flag vorhanden ist, konvertieren Sie die Positionswerte in Verweis Zeiten, wenn Sie Sie an den Aufrufer zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f2a61-211">If this flag is present, convert the position values into reference times when you return them to the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2a61-212">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2a61-212">Requirements</span></span>



| <span data-ttu-id="f2a61-213">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2a61-213">Requirement</span></span> | <span data-ttu-id="f2a61-214">Wert</span><span class="sxs-lookup"><span data-stu-id="f2a61-214">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2a61-215">Header</span><span class="sxs-lookup"><span data-stu-id="f2a61-215">Header</span></span><br/>  | <dl> <span data-ttu-id="f2a61-216"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2a61-216"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f2a61-217">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2a61-217">Library</span></span><br/> | <dl> <span data-ttu-id="f2a61-218">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f2a61-218"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2a61-219">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2a61-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2a61-220">Unterstützen der Suche in einem Quell Filter</span><span class="sxs-lookup"><span data-stu-id="f2a61-220">Supporting Seeking in a Source Filter</span></span>](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




