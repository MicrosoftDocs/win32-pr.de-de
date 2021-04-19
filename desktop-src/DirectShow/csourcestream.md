---
description: Die csourcestream-Klasse stellt eine Ausgabe-PIN für die CSource-Filterklasse bereit.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Csourcestream-Klasse (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368644"
---
# <a name="csourcestream-class"></a><span data-ttu-id="f2223-103">Csourcestream-Klasse</span><span class="sxs-lookup"><span data-stu-id="f2223-103">CSourceStream class</span></span>

![csourcestream-Klassenhierarchie](images/source02.png)

<span data-ttu-id="f2223-105">Die **csourcestream** -Klasse stellt eine Ausgabe-PIN für die [**CSource**](csource.md) -Filterklasse bereit.</span><span class="sxs-lookup"><span data-stu-id="f2223-105">The **CSourceStream** class provides an output pin for the [**CSource**](csource.md) filter class.</span></span>

<span data-ttu-id="f2223-106">Weitere Informationen zur Verwendung dieser Klasse finden Sie unter [**CSource**](csource.md).</span><span class="sxs-lookup"><span data-stu-id="f2223-106">For information on using this class, see [**CSource**](csource.md).</span></span> <span data-ttu-id="f2223-107">Diese Klasse erbt die Klasse " [**camthread**](camthread.md) ", die einen Arbeits Thread zum Streamen von Daten aus der PIN bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f2223-107">This class inherits the [**CAMThread**](camthread.md) class, which provides a worker thread for streaming data from the pin.</span></span> <span data-ttu-id="f2223-108">Die **csourcestream** -Klasse implementiert die folgenden Hilfsmethoden, um Anforderungen an den Thread zu senden:</span><span class="sxs-lookup"><span data-stu-id="f2223-108">The **CSourceStream** class implements the following helper methods to send requests to the thread:</span></span>

-   [<span data-ttu-id="f2223-109">**Csourcestream:: Exit**</span><span class="sxs-lookup"><span data-stu-id="f2223-109">**CSourceStream::Exit**</span></span>](csourcestream-exit.md)
-   [<span data-ttu-id="f2223-110">**Csourcestream:: init**</span><span class="sxs-lookup"><span data-stu-id="f2223-110">**CSourceStream::Init**</span></span>](csourcestream-init.md)
-   [<span data-ttu-id="f2223-111">**Csourcestream::P ause**</span><span class="sxs-lookup"><span data-stu-id="f2223-111">**CSourceStream::Pause**</span></span>](csourcestream-pause.md)
-   [<span data-ttu-id="f2223-112">**Csourcestream:: Run**</span><span class="sxs-lookup"><span data-stu-id="f2223-112">**CSourceStream::Run**</span></span>](csourcestream-run.md)
-   [<span data-ttu-id="f2223-113">**Csourcestream:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="f2223-113">**CSourceStream::Stop**</span></span>](csourcestream-stop.md)

<span data-ttu-id="f2223-114">Die erste Anforderung an den Thread muss [**Init**](csourcestream-init.md)sein.</span><span class="sxs-lookup"><span data-stu-id="f2223-114">The first request to the thread must be [**Init**](csourcestream-init.md).</span></span> <span data-ttu-id="f2223-115">Die [**Beendigungs Anforderung beendet den Thread**](csourcestream-exit.md) .</span><span class="sxs-lookup"><span data-stu-id="f2223-115">The [**Exit**](csourcestream-exit.md) request terminates the thread.</span></span> <span data-ttu-id="f2223-116">In der Praxis ist es nicht notwendig, eine dieser Methoden direkt aufzurufen, da die [**csourcestream:: Active**](csourcestream-active.md) -und [**csourcestream:: ininaktiven**](csourcestream-inactive.md) -Methoden der PIN diese bei Bedarf aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f2223-116">In practice, it is not necessary to call any of these methods directly, because the pin's [**CSourceStream::Active**](csourcestream-active.md) and [**CSourceStream::Inactive**](csourcestream-inactive.md) methods call them as needed.</span></span>

<span data-ttu-id="f2223-117">Die Klasse stellt auch mehrere "Handlermethoden" bereit:</span><span class="sxs-lookup"><span data-stu-id="f2223-117">The class also provides several "handler" methods:</span></span>

-   [<span data-ttu-id="f2223-118">**Csourcestream:: onthreadcreate**</span><span class="sxs-lookup"><span data-stu-id="f2223-118">**CSourceStream::OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)
-   [<span data-ttu-id="f2223-119">**Csourcestream:: onthreaddestroy**</span><span class="sxs-lookup"><span data-stu-id="f2223-119">**CSourceStream::OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)
-   [<span data-ttu-id="f2223-120">**Csourcestream:: onthreadstartplay**</span><span class="sxs-lookup"><span data-stu-id="f2223-120">**CSourceStream::OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)

<span data-ttu-id="f2223-121">Diese Aktionen werden in der Basisklasse nicht durchgesetzt, aber die abgeleitete Klasse kann Sie überschreiben.</span><span class="sxs-lookup"><span data-stu-id="f2223-121">These do nothing in the base class, but the derived class can override them.</span></span>



| <span data-ttu-id="f2223-122">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="f2223-122">Protected Member Variables</span></span>                                             | <span data-ttu-id="f2223-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2223-123">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2223-124">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="f2223-124">**m\_pFilter**</span></span>](csourcestream-m-pfilter.md)                          | <span data-ttu-id="f2223-125">Zeiger auf den Filter, der diese PIN enthält.</span><span class="sxs-lookup"><span data-stu-id="f2223-125">Pointer to the filter that contains this pin.</span></span>                                                                                     |
| <span data-ttu-id="f2223-126">Geschützte Methoden</span><span class="sxs-lookup"><span data-stu-id="f2223-126">Protected Methods</span></span>                                                      | <span data-ttu-id="f2223-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2223-127">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="f2223-128">**Onthreadcreate**</span><span class="sxs-lookup"><span data-stu-id="f2223-128">**OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)                 | <span data-ttu-id="f2223-129">Wird aufgerufen, wenn der streamingindthread initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f2223-129">Called when the streaming thread is initialized.</span></span> <span data-ttu-id="f2223-130">Virtu.</span><span class="sxs-lookup"><span data-stu-id="f2223-130">Virtual.</span></span>                                                                         |
| [<span data-ttu-id="f2223-131">**Onthreaddestroy**</span><span class="sxs-lookup"><span data-stu-id="f2223-131">**OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)               | <span data-ttu-id="f2223-132">Wird aufgerufen, wenn der streamingthread gerade beendet wird.</span><span class="sxs-lookup"><span data-stu-id="f2223-132">Called when the streaming thread is about to exit.</span></span> <span data-ttu-id="f2223-133">Virtu.</span><span class="sxs-lookup"><span data-stu-id="f2223-133">Virtual.</span></span>                                                                       |
| [<span data-ttu-id="f2223-134">**Onthreadstartplay**</span><span class="sxs-lookup"><span data-stu-id="f2223-134">**OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)           | <span data-ttu-id="f2223-135">Wird am Anfang der [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f2223-135">Called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="f2223-136">Virtu.</span><span class="sxs-lookup"><span data-stu-id="f2223-136">Virtual.</span></span> |
| [<span data-ttu-id="f2223-137">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="f2223-137">**Active**</span></span>](csourcestream-active.md)                                 | <span data-ttu-id="f2223-138">Benachrichtigt die PIN, dass der Filter jetzt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="f2223-138">Notifies the pin that the filter is now active.</span></span>                                                                                   |
| [<span data-ttu-id="f2223-139">**Inaktiv**</span><span class="sxs-lookup"><span data-stu-id="f2223-139">**Inactive**</span></span>](csourcestream-inactive.md)                             | <span data-ttu-id="f2223-140">Benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="f2223-140">Notifies the pin that the filter is no longer active.</span></span>                                                                             |
| [<span data-ttu-id="f2223-141">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="f2223-141">**GetRequest**</span></span>](csourcestream-getrequest.md)                         | <span data-ttu-id="f2223-142">Wartet auf die nächste Thread Anforderung.</span><span class="sxs-lookup"><span data-stu-id="f2223-142">Waits for the next thread request.</span></span>                                                                                                |
| [<span data-ttu-id="f2223-143">**Check Request**</span><span class="sxs-lookup"><span data-stu-id="f2223-143">**CheckRequest**</span></span>](csourcestream-checkrequest.md)                     | <span data-ttu-id="f2223-144">Überprüft, ob eine Thread Anforderung vorhanden ist, ohne zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="f2223-144">Checks if there is a thread request, without blocking.</span></span>                                                                            |
| [<span data-ttu-id="f2223-145">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="f2223-145">**ThreadProc**</span></span>](csourcestream-threadproc.md)                         | <span data-ttu-id="f2223-146">Thread Prozedur.</span><span class="sxs-lookup"><span data-stu-id="f2223-146">Thread procedure.</span></span> <span data-ttu-id="f2223-147">Virtu.</span><span class="sxs-lookup"><span data-stu-id="f2223-147">Virtual.</span></span>                                                                                                        |
| [<span data-ttu-id="f2223-148">**Dobufferprocessingloop**</span><span class="sxs-lookup"><span data-stu-id="f2223-148">**DoBufferProcessingLoop**</span></span>](csourcestream-dobufferprocessingloop.md) | <span data-ttu-id="f2223-149">Generiert Mediendaten und übergibt sie an die downstreameingabepin.</span><span class="sxs-lookup"><span data-stu-id="f2223-149">Generates media data and delivers it to the downstream input pin.</span></span> <span data-ttu-id="f2223-150">Virtu.</span><span class="sxs-lookup"><span data-stu-id="f2223-150">Virtual.</span></span>                                                        |
| [<span data-ttu-id="f2223-151">**Checkmediatype**</span><span class="sxs-lookup"><span data-stu-id="f2223-151">**CheckMediaType**</span></span>](csourcestream-checkmediatype.md)                 | <span data-ttu-id="f2223-152">Bestimmt, ob die PIN einen bestimmten Medientyp akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="f2223-152">Determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="f2223-153">Virtu.</span><span class="sxs-lookup"><span data-stu-id="f2223-153">Virtual.</span></span>                                                                     |
| [<span data-ttu-id="f2223-154">**Getmediatype**</span><span class="sxs-lookup"><span data-stu-id="f2223-154">**GetMediaType**</span></span>](csourcestream-getmediatype.md)                     | <span data-ttu-id="f2223-155">Ruft einen bevorzugten Medientyp ab.</span><span class="sxs-lookup"><span data-stu-id="f2223-155">Retrieves a preferred media type.</span></span> <span data-ttu-id="f2223-156">Virtu.</span><span class="sxs-lookup"><span data-stu-id="f2223-156">Virtual.</span></span>                                                                                        |
| <span data-ttu-id="f2223-157">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="f2223-157">Public Methods</span></span>                                                         | <span data-ttu-id="f2223-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2223-158">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="f2223-159">**Csourcestream**</span><span class="sxs-lookup"><span data-stu-id="f2223-159">**CSourceStream**</span></span>](csourcestream-csourcestream.md)                   | <span data-ttu-id="f2223-160">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f2223-160">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="f2223-161">**~ Csourcestream**</span><span class="sxs-lookup"><span data-stu-id="f2223-161">**~ CSourceStream**</span></span>](csourcestream--csourcestream.md)                | <span data-ttu-id="f2223-162">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="f2223-162">Destructor method.</span></span> <span data-ttu-id="f2223-163">Virtu.</span><span class="sxs-lookup"><span data-stu-id="f2223-163">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="f2223-164">**Init**</span><span class="sxs-lookup"><span data-stu-id="f2223-164">**Init**</span></span>](csourcestream-init.md)                                     | <span data-ttu-id="f2223-165">Initialisiert den streamingthread.</span><span class="sxs-lookup"><span data-stu-id="f2223-165">Initializes the streaming thread.</span></span>                                                                                                 |
| [<span data-ttu-id="f2223-166">**Beenden**</span><span class="sxs-lookup"><span data-stu-id="f2223-166">**Exit**</span></span>](csourcestream-exit.md)                                     | <span data-ttu-id="f2223-167">Signalisiert dem streamingthread, den Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f2223-167">Signals the streaming thread to exit.</span></span>                                                                                             |
| [<span data-ttu-id="f2223-168">**Ausführen**</span><span class="sxs-lookup"><span data-stu-id="f2223-168">**Run**</span></span>](csourcestream-run.md)                                       | <span data-ttu-id="f2223-169">Signalisiert, dass der streamingthread ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2223-169">Signals the streaming thread to run.</span></span>                                                                                              |
| [<span data-ttu-id="f2223-170">**Anhalten**</span><span class="sxs-lookup"><span data-stu-id="f2223-170">**Pause**</span></span>](csourcestream-pause.md)                                   | <span data-ttu-id="f2223-171">Signalisiert, dass der streamingingthread aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="f2223-171">Signals the streaming thread to become active.</span></span>                                                                                    |
| [<span data-ttu-id="f2223-172">**Stop**</span><span class="sxs-lookup"><span data-stu-id="f2223-172">**Stop**</span></span>](csourcestream-stop.md)                                     | <span data-ttu-id="f2223-173">Signalisiert, dass der Streaminginhalt beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2223-173">Signals the streaming thread to stop.</span></span>                                                                                             |
| <span data-ttu-id="f2223-174">Reine virtuelle Methoden</span><span class="sxs-lookup"><span data-stu-id="f2223-174">Pure Virtual Methods</span></span>                                                   | <span data-ttu-id="f2223-175">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2223-175">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="f2223-176">**FillBuffer**</span><span class="sxs-lookup"><span data-stu-id="f2223-176">**FillBuffer**</span></span>](csourcestream-fillbuffer.md)                         | <span data-ttu-id="f2223-177">Füllt ein Medien Beispiel mit Daten.</span><span class="sxs-lookup"><span data-stu-id="f2223-177">Fills a media sample with data.</span></span>                                                                                                   |
| <span data-ttu-id="f2223-178">IPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="f2223-178">IPin Methods</span></span>                                                           | <span data-ttu-id="f2223-179">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f2223-179">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="f2223-180">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="f2223-180">**QueryId**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | <span data-ttu-id="f2223-181">Ruft einen Bezeichner für die PIN ab.</span><span class="sxs-lookup"><span data-stu-id="f2223-181">Retrieves an identifier for the pin.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="f2223-182">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2223-182">Requirements</span></span>



| <span data-ttu-id="f2223-183">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2223-183">Requirement</span></span> | <span data-ttu-id="f2223-184">Wert</span><span class="sxs-lookup"><span data-stu-id="f2223-184">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2223-185">Header</span><span class="sxs-lookup"><span data-stu-id="f2223-185">Header</span></span><br/>  | <dl> <span data-ttu-id="f2223-186"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f2223-186"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f2223-187">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2223-187">Library</span></span><br/> | <dl> <span data-ttu-id="f2223-188">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f2223-188"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2223-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2223-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2223-190">Schreiben von Quell Filtern</span><span class="sxs-lookup"><span data-stu-id="f2223-190">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




