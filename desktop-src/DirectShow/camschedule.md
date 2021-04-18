---
description: Die Klasse "camschedule" implementiert einen Planer für Referenzuhren.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Camschedule-Klasse (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365693"
---
# <a name="camschedule-class"></a><span data-ttu-id="e2ecf-103">Camschedule-Klasse</span><span class="sxs-lookup"><span data-stu-id="e2ecf-103">CAMSchedule class</span></span>

<span data-ttu-id="e2ecf-104">Die- `CAMSchedule` Klasse implementiert einen Planer für Referenzuhren.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-104">The `CAMSchedule` class implements a scheduler for reference clocks.</span></span>



| <span data-ttu-id="e2ecf-105">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="e2ecf-105">Public Methods</span></span>                                             | <span data-ttu-id="e2ecf-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2ecf-106">Description</span></span>                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2ecf-107">**"Camschedule"**</span><span class="sxs-lookup"><span data-stu-id="e2ecf-107">**CAMSchedule**</span></span>](camschedule-camschedule.md)             | <span data-ttu-id="e2ecf-108">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-108">Constructor method.</span></span>                                                                  |
| [<span data-ttu-id="e2ecf-109">**~ Camschedule**</span><span class="sxs-lookup"><span data-stu-id="e2ecf-109">**~CAMSchedule**</span></span>](camschedule--camschedule.md)           | <span data-ttu-id="e2ecf-110">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-110">Destructor method.</span></span> <span data-ttu-id="e2ecf-111">Virtu.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-111">Virtual.</span></span>                                                          |
| [<span data-ttu-id="e2ecf-112">**Getadviercount**</span><span class="sxs-lookup"><span data-stu-id="e2ecf-112">**GetAdviseCount**</span></span>](camschedule-getadvisecount.md)       | <span data-ttu-id="e2ecf-113">Ruft die Anzahl der ausstehenden Anforderungs Anforderungen ab.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-113">Retrieves the number of pending advise requests.</span></span>                                     |
| [<span data-ttu-id="e2ecf-114">**Getnextadvictime**</span><span class="sxs-lookup"><span data-stu-id="e2ecf-114">**GetNextAdviseTime**</span></span>](camschedule-getnextadvisetime.md) | <span data-ttu-id="e2ecf-115">Ruft den Zeitpunkt der nächsten anforderungsanforderung ab.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-115">Retrieves the time of the next advise request.</span></span>                                       |
| [<span data-ttu-id="e2ecf-116">**Addadvisepacket**</span><span class="sxs-lookup"><span data-stu-id="e2ecf-116">**AddAdvisePacket**</span></span>](camschedule-addadvisepacket.md)     | <span data-ttu-id="e2ecf-117">Fügt der Liste der ausstehenden Anforderungen eine anforderungsanforderung hinzu.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-117">Adds an advise request to the list of pending requests.</span></span>                              |
| [<span data-ttu-id="e2ecf-118">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="e2ecf-118">**Unadvise**</span></span>](camschedule-unadvise.md)                   | <span data-ttu-id="e2ecf-119">Entfernt eine Benachrichtigungs Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-119">Removes an advise request.</span></span>                                                           |
| [<span data-ttu-id="e2ecf-120">**Advise**</span><span class="sxs-lookup"><span data-stu-id="e2ecf-120">**Advise**</span></span>](camschedule-advise.md)                       | <span data-ttu-id="e2ecf-121">Sendet alle Anforderungen, die für eine angegebene Zeit oder eine frühere Zeit geplant sind.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-121">Dispatches all requests that are scheduled for a specified time or earlier.</span></span>          |
| [<span data-ttu-id="e2ecf-122">**GetEvent**</span><span class="sxs-lookup"><span data-stu-id="e2ecf-122">**GetEvent**</span></span>](camschedule-getevent.md)                   | <span data-ttu-id="e2ecf-123">Ruft ein Ereignis Handle ab, das verwendet wird, um eine Änderung in der nächsten Empfehlung zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-123">Retrieves an event handle, which is used to signal a change in the next advise time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e2ecf-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2ecf-124">Remarks</span></span>

<span data-ttu-id="e2ecf-125">Dieses Hilfsobjekt verwaltet eine Liste von Anforderungs Anforderungen für eine Referenzuhr.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-125">This helper object maintains a list of advise requests for a reference clock.</span></span> <span data-ttu-id="e2ecf-126">Die [**cbasereferenceclock**](cbasereferenceclock.md) -Klasse verwendet diese, um Anforderungs Anforderungen zu planen.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-126">The [**CBaseReferenceClock**](cbasereferenceclock.md) class uses it to help schedule advise requests.</span></span> <span data-ttu-id="e2ecf-127">Uhren verwenden dieses Objekt wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e2ecf-127">Clocks use this object in the following manner:</span></span>

1.  <span data-ttu-id="e2ecf-128">Die Uhr erstellt einen Arbeits Thread zur Handhabung der Planung.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-128">The clock creates a worker thread to handle scheduling.</span></span>
2.  <span data-ttu-id="e2ecf-129">Der Arbeits Thread ruft die " [**camschedule:: GetEvent**](camschedule-getevent.md) "-Methode auf, um ein Ereignis Handle aus dem Scheduler abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-129">The worker thread calls the [**CAMSchedule::GetEvent**](camschedule-getevent.md) method to retrieve an event handle from the scheduler.</span></span> <span data-ttu-id="e2ecf-130">Er wartet auf dieses Ereignis, anfänglich mit einem unendlichen Timeout.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-130">It waits on this event, initially with an infinite time-out.</span></span>
3.  <span data-ttu-id="e2ecf-131">Zum Planen einer neuen Benachrichtigungs Anforderung Ruft die Uhr die " [**camschedule:: addadvisepacket**](camschedule-addadvisepacket.md) "-Methode auf.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-131">To schedule a new advise request, the clock calls the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span> <span data-ttu-id="e2ecf-132">Eine Benachrichtigungs Anforderung kann ein-oder periodisch sein.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-132">An advise request can be one-shot or periodic.</span></span> <span data-ttu-id="e2ecf-133">Der Scheduler speichert die Liste der Anforderungen in der angegebenen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-133">The scheduler keeps the list of requests in time order.</span></span>
4.  <span data-ttu-id="e2ecf-134">Wenn eine Anforderung am Anfang der Liste hinzugefügt wird, signalisiert der Planer das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-134">If a request is added to the front of the list, the scheduler signals the event.</span></span> <span data-ttu-id="e2ecf-135">(Die Liste ist zuerst leer, sodass die erste Anforderung das Ereignis garantiert signalisiert.)</span><span class="sxs-lookup"><span data-stu-id="e2ecf-135">(The list is empty at first, so the first request is guaranteed to signal the event.)</span></span>
5.  <span data-ttu-id="e2ecf-136">Wenn das Ereignis signalisiert wird, ruft der Arbeits Thread die Methode " [**camschedule:: Empfehlung**](camschedule-advise.md) " auf und gibt den aktuellen Verweis Zeitpunkt an.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-136">When the event is signaled, the worker thread calls the [**CAMSchedule::Advise**](camschedule-advise.md) method, specifying the current reference time.</span></span> <span data-ttu-id="e2ecf-137">Wenn ausstehende Anforderungen abgelaufen sind, werden Sie vom Scheduler versendet.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-137">If any pending requests have expired, the scheduler dispatches them.</span></span>
6.  <span data-ttu-id="e2ecf-138">Die Methode "Empfehlung" gibt den Zeitpunkt der nächsten Anforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-138">The Advise method returns the time of the next request.</span></span> <span data-ttu-id="e2ecf-139">Der Arbeits Thread verwendet diesen Wert, um einen neuen Timeout Wert zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-139">The worker thread uses this value to calculate a new time-out value.</span></span>
7.  <span data-ttu-id="e2ecf-140">Die Schritte 2 6 werden unbegrenzt wiederholt.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-140">Steps 2 6 repeat indefinitely.</span></span>
8.  <span data-ttu-id="e2ecf-141">Um den Arbeits Thread zu beenden, legt die Uhr ein internes Flag fest und signalisiert das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-141">To terminate the worker thread, the clock sets an internal flag and signals the event.</span></span>

<span data-ttu-id="e2ecf-142">In Schritt 2 wird entweder das Ereignis signalisiert, oder der Warte Vorgang ist abgelaufen. Wenn das Ereignis signalisiert wird, bedeutet dies, dass am Anfang der Liste eine neue Anforderung hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-142">In step 2, either the event is signaled, or the wait times out. If the event is signaled, it means that a new request was added to the front of the list.</span></span> <span data-ttu-id="e2ecf-143">Der Arbeits Thread muss einen neuen Timeout Wert berechnen.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-143">The worker thread must calculate a new time-out value.</span></span> <span data-ttu-id="e2ecf-144">Andererseits bedeutet dies, dass bei einem Timeout eine anforderungsanforderung ausgegeben wurde und verteilt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-144">On the other hand, if the wait times out, it means that an advise request has come due and must be dispatched.</span></span> <span data-ttu-id="e2ecf-145">Der in Schritt 5 genannte Anrufe behandelt beide Fälle.</span><span class="sxs-lookup"><span data-stu-id="e2ecf-145">The call to Advise in step 5 handles both cases.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2ecf-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2ecf-146">Requirements</span></span>



| <span data-ttu-id="e2ecf-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2ecf-147">Requirement</span></span> | <span data-ttu-id="e2ecf-148">Wert</span><span class="sxs-lookup"><span data-stu-id="e2ecf-148">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ecf-149">Header</span><span class="sxs-lookup"><span data-stu-id="e2ecf-149">Header</span></span><br/>  | <dl> <span data-ttu-id="e2ecf-150"><dt>Dsschedule. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2ecf-150"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="e2ecf-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2ecf-151">Library</span></span><br/> | <dl> <span data-ttu-id="e2ecf-152">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e2ecf-152"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




