---
description: Die cbasereferenceclock-Klasse implementiert eine Referenzuhr.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: Cbasereferenceclock-Klasse (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358608"
---
# <a name="cbasereferenceclock-class"></a><span data-ttu-id="ef4f4-103">Cbasereferenceclock-Klasse</span><span class="sxs-lookup"><span data-stu-id="ef4f4-103">CBaseReferenceClock class</span></span>

![cbasereferenceclock-Klassenhierarchie](images/rclock01.png)

<span data-ttu-id="ef4f4-105">Die- `CBaseReferenceClock` Klasse implementiert eine verweisuhr.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-105">The `CBaseReferenceClock` class implements a reference clock.</span></span>



| <span data-ttu-id="ef4f4-106">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="ef4f4-106">Protected Member Variables</span></span>                                                         | <span data-ttu-id="ef4f4-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef4f4-107">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef4f4-108">**m \_ pschedule**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-108">**m\_pSchedule**</span></span>](cbasereferenceclock-m-pschedule.md)                            | <span data-ttu-id="ef4f4-109">Ein " [**camschedule**](camschedule.md) "-Objekt, das Planungsaufgaben für die Uhr behandelt.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-109">[**CAMSchedule**](camschedule.md) object that handles scheduling tasks for the clock.</span></span> |
| <span data-ttu-id="ef4f4-110">Geschützte Methoden</span><span class="sxs-lookup"><span data-stu-id="ef4f4-110">Protected Methods</span></span>                                                                  | <span data-ttu-id="ef4f4-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef4f4-111">Description</span></span>                                                                            |
| [<span data-ttu-id="ef4f4-112">**~ Cbasereferenceclock**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-112">**~CBaseReferenceClock**</span></span>](cbasereferenceclock--cbasereferenceclock.md)           | <span data-ttu-id="ef4f4-113">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-113">Destructor method.</span></span>                                                                     |
| <span data-ttu-id="ef4f4-114">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="ef4f4-114">Public Methods</span></span>                                                                     | <span data-ttu-id="ef4f4-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef4f4-115">Description</span></span>                                                                            |
| [<span data-ttu-id="ef4f4-116">**Cbasereferenceclock**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-116">**CBaseReferenceClock**</span></span>](cbasereferenceclock-cbasereferenceclock.md)             | <span data-ttu-id="ef4f4-117">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-117">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="ef4f4-118">**Getprivatetime**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-118">**GetPrivateTime**</span></span>](cbasereferenceclock-getprivatetime.md)                       | <span data-ttu-id="ef4f4-119">Ruft die tatsächliche Uhrzeit von der Uhr ab.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-119">Retrieves the real time from the clock.</span></span>                                                |
| [<span data-ttu-id="ef4f4-120">**Settimedelta**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-120">**SetTimeDelta**</span></span>](cbasereferenceclock-settimedelta.md)                           | <span data-ttu-id="ef4f4-121">Passt die interne Uhrzeit an.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-121">Adjusts the internal clock time.</span></span>                                                       |
| [<span data-ttu-id="ef4f4-122">**Getschedule**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-122">**GetSchedule**</span></span>](cbasereferenceclock-getschedule.md)                             | <span data-ttu-id="ef4f4-123">Ruft einen Zeiger auf das Zeit Planungs Objekt der Uhr ab.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-123">Retrieves a pointer to the clock's scheduling object.</span></span>                                  |
| [<span data-ttu-id="ef4f4-124">**Triggerthread**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-124">**TriggerThread**</span></span>](cbasereferenceclock-triggerthread.md)                         | <span data-ttu-id="ef4f4-125">Aktiviert den Arbeits Thread, der die Planung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-125">Wakes up the worker thread that handles scheduling.</span></span>                                    |
| <span data-ttu-id="ef4f4-126">IReferenceClock-Methoden</span><span class="sxs-lookup"><span data-stu-id="ef4f4-126">IReferenceClock Methods</span></span>                                                            | <span data-ttu-id="ef4f4-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef4f4-127">Description</span></span>                                                                            |
| [<span data-ttu-id="ef4f4-128">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-128">**GetTime**</span></span>](cbasereferenceclock-gettime.md)                                     | <span data-ttu-id="ef4f4-129">Ruft den aktuellen Verweis Zeitpunkt ab.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-129">Retrieves the current reference time.</span></span>                                                  |
| [<span data-ttu-id="ef4f4-130">**Empfehlungen**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-130">**AdviseTime**</span></span>](cbasereferenceclock-advisetime.md)                               | <span data-ttu-id="ef4f4-131">Erstellt eine One-Shot-anforderungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-131">Creates a one-shot advise request.</span></span>                                                     |
| [<span data-ttu-id="ef4f4-132">**Empfehlungen regelmäßig**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-132">**AdvisePeriodic**</span></span>](cbasereferenceclock-adviseperiodic.md)                       | <span data-ttu-id="ef4f4-133">Erstellt eine regelmäßige anforderungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-133">Creates a periodic advise request.</span></span>                                                     |
| [<span data-ttu-id="ef4f4-134">**Unadvise**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-134">**Unadvise**</span></span>](cbasereferenceclock-unadvise.md)                                   | <span data-ttu-id="ef4f4-135">Entfernt eine ausstehende Benachrichtigungs Anforderung.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-135">Removes a pending advise request.</span></span>                                                      |
| <span data-ttu-id="ef4f4-136">Ireferenceclocktimercontrol-Methoden</span><span class="sxs-lookup"><span data-stu-id="ef4f4-136">IReferenceClockTimerControl Methods</span></span>                                                | <span data-ttu-id="ef4f4-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef4f4-137">Description</span></span>                                                                            |
| [<span data-ttu-id="ef4f4-138">**Getdefaulttimerresolution**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-138">**GetDefaultTimerResolution**</span></span>](cbasereferenceclock-getdefaulttimerresolution.md) | <span data-ttu-id="ef4f4-139">Gibt die aktuelle Auflösung des Zeit Gebers der verweisuhr zurück.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-139">Returns the current resolution of the reference clock's timer.</span></span>                         |
| [<span data-ttu-id="ef4f4-140">**Setdefaulttimerresolution**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-140">**SetDefaultTimerResolution**</span></span>](cbasereferenceclock-setdefaulttimerresolution.md) | <span data-ttu-id="ef4f4-141">Legt die Auflösung des Zeit Gebers der verweisuhr fest.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-141">Sets the resolution of the reference clock's timer.</span></span>                                    |
| <span data-ttu-id="ef4f4-142">Hilfsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ef4f4-142">Helper Functions</span></span>                                                                   | <span data-ttu-id="ef4f4-143">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef4f4-143">Description</span></span>                                                                            |
| [<span data-ttu-id="ef4f4-144">**Convertummillisekunden**</span><span class="sxs-lookup"><span data-stu-id="ef4f4-144">**ConvertToMilliseconds**</span></span>](converttomilliseconds.md)                             | <span data-ttu-id="ef4f4-145">Konvertiert eine Verweis Zeit in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-145">Converts a reference time to milliseconds.</span></span>                                             |



 

## <a name="remarks"></a><span data-ttu-id="ef4f4-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef4f4-146">Remarks</span></span>

<span data-ttu-id="ef4f4-147">Diese Klasse implementiert eine Referenzuhr, die die Schnittstellen [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) und [**ireferenceclocktimercontrol**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-147">This class implements a reference clock that supports the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) and [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) interfaces.</span></span> <span data-ttu-id="ef4f4-148">Wenn ein Filter beispielsweise eine Referenzuhr für das Filter Diagramm bereitstellen kann, kann er durch den Zugriff auf ein Hardware Gerät diese Klasse zum Implementieren der Uhr verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-148">If a filter can provide a reference clock for the filter graph for example, by accessing a hardware device it can use this class to implement the clock.</span></span>

<span data-ttu-id="ef4f4-149">Das- `CBaseReferenceClock` Objekt verwaltet zwei unterschiedliche Uhrzeitwerte:</span><span class="sxs-lookup"><span data-stu-id="ef4f4-149">The `CBaseReferenceClock` object maintains two distinct time values:</span></span>

-   <span data-ttu-id="ef4f4-150">Intern gibt die [**cbasereferenceclock:: getprivatetime**](cbasereferenceclock-getprivatetime.md) -Methode die tatsächliche Zeit zurück, die von der Uhr aufbewahrt wird.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-150">Internally, the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method returns the actual time kept by the clock.</span></span>
-   <span data-ttu-id="ef4f4-151">Extern gibt die [**cbasereferenceclock:: getTime**](cbasereferenceclock-gettime.md) -Methode die Verweis Zeit für das Filter Diagramm zurück.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-151">Externally, the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method returns the reference time for the filter graph.</span></span>

<span data-ttu-id="ef4f4-152">Es ist gültig, dass die interne Uhr rückwärts in kurzen Zeitabständen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-152">It is valid for the internal clock to run backward over brief periods.</span></span> <span data-ttu-id="ef4f4-153">Wenn z. b. die Uhr vorwärts abweicht, kann Sie vom Filter rückwärts angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-153">For example, if the clock drifts forward, the filter can adjust it backward.</span></span> <span data-ttu-id="ef4f4-154">(Siehe [**cbasereferenceclock:: settimedelta**](cbasereferenceclock-settimedelta.md).) Die **GetTime** -Methode verwendet die von **getprivatetime** gemeldeten Zeit Werte.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-154">(See [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).) The **GetTime** method uses the time values reported by **GetPrivateTime**.</span></span> <span data-ttu-id="ef4f4-155">Die Verweis Zeit nimmt jedoch monoton zu. Das heißt, es wird nie rückwärts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-155">However, the reference time is monotonically increasing; in other words, it never runs backward.</span></span> <span data-ttu-id="ef4f4-156">Wenn die interne Uhr rückwärts ausgeführt wird, meldet **GetTime** daher weiterhin die alte Zeit, bis die interne Uhr abfängt.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-156">Therefore, if the internal clock runs backward, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

<span data-ttu-id="ef4f4-157">Beispielsweise können die beiden Methoden die folgenden Sequenzen zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="ef4f4-157">For example, the two methods might return the following sequences:</span></span>

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

<span data-ttu-id="ef4f4-158">Auf dem dritten Takt springt die interne Uhr rückwärts zu 103.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-158">On the third clock tick, the internal clock jumps backward to 103.</span></span> <span data-ttu-id="ef4f4-159">Die **GetTime** -Methode meldet den Bericht 106 so lange, bis die interne Uhr wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-159">The **GetTime** method continues to report 106 until the internal clock catches up.</span></span>

<span data-ttu-id="ef4f4-160">Standardmäßig gibt **getprivatetime** die Systemzeit durch einen Aufruf der **timeGetTime** -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-160">By default, **GetPrivateTime** returns the system time, through a call to the **timeGetTime** function.</span></span> <span data-ttu-id="ef4f4-161">Ein Filter, der eine Referenzuhr von einem externen Gerät bereitstellt, kann eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="ef4f4-161">A filter that is providing a reference clock from an external device can do one of the following:</span></span>

-   <span data-ttu-id="ef4f4-162">Überschreiben Sie **getprivatetime** , um die Uhrzeit vom Gerät zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-162">Override **GetPrivateTime** to return the time from the device.</span></span>
-   <span data-ttu-id="ef4f4-163">Überwachen Sie die Diskrepanz zwischen der Geräte Zeit und der Systemzeit, und wenden Sie **settimedelta** an, um Korrekturen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-163">Monitor the discrepancy between the device time and the system time, and call **SetTimeDelta** to make corrections.</span></span>

<span data-ttu-id="ef4f4-164">Diese Klasse verwendet ein [**camschedule**](camschedule.md) -Objekt, um die Planung von Anforderungs Anforderungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ef4f4-164">This class uses a [**CAMSchedule**](camschedule.md) object to handle scheduling of advise requests.</span></span> <span data-ttu-id="ef4f4-165">Weitere Informationen finden Sie in der Dokumentation für die Klasse " **camschedule** ".</span><span class="sxs-lookup"><span data-stu-id="ef4f4-165">For details, see the documentation for the **CAMSchedule** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef4f4-166">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef4f4-166">Requirements</span></span>



| <span data-ttu-id="ef4f4-167">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef4f4-167">Requirement</span></span> | <span data-ttu-id="ef4f4-168">Wert</span><span class="sxs-lookup"><span data-stu-id="ef4f4-168">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4f4-169">Header</span><span class="sxs-lookup"><span data-stu-id="ef4f4-169">Header</span></span><br/>  | <dl> <span data-ttu-id="ef4f4-170"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef4f4-170"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ef4f4-171">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef4f4-171">Library</span></span><br/> | <dl> <span data-ttu-id="ef4f4-172">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ef4f4-172"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




