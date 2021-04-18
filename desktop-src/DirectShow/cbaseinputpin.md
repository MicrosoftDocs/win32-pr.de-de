---
description: Die cbaseinputpin-Klasse ist eine abstrakte Basisklasse für die Implementierung von Eingabe Pins. Diese Klasse fügt zusätzlich zur Unterstützung der IPin-Schnittstelle, die von cbasepin bereitgestellt wird, Unterstützung für die IMemInputPin-Schnittstelle hinzu.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Cbaseingeputpin-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361522"
---
# <a name="cbaseinputpin-class"></a><span data-ttu-id="65220-104">Cbaseingeputpin-Klasse</span><span class="sxs-lookup"><span data-stu-id="65220-104">CBaseInputPin class</span></span>

![cbaseingeputpin-Klassenhierarchie](images/filter07.png)

<span data-ttu-id="65220-106">Bei der- `CBaseInputPin` Klasse handelt es sich um eine abstrakte Basisklasse zum Implementieren von Eingabe Pins.</span><span class="sxs-lookup"><span data-stu-id="65220-106">The `CBaseInputPin` class is an abstract base class for implementing input pins.</span></span> <span data-ttu-id="65220-107">Diese Klasse fügt zusätzlich zur Unterstützung der [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle, die von [**cbasepin**](cbasepin.md)bereitgestellt wird, Unterstützung für die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="65220-107">This class adds support for the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, in addition to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface support provided by [**CBasePin**](cbasepin.md).</span></span>

<span data-ttu-id="65220-108">Um diese Klasse zu verwenden, leiten Sie eine neue Klasse ab, und überschreiben Sie mindestens die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="65220-108">To use this class, derive a new class and override at least the following methods:</span></span>

-   [<span data-ttu-id="65220-109">**Cbaseiniputpin:: beginflush**</span><span class="sxs-lookup"><span data-stu-id="65220-109">**CBaseInputPin::BeginFlush**</span></span>](cbaseinputpin-beginflush.md)
-   [<span data-ttu-id="65220-110">**Cbaseingeputpin:: endflush**</span><span class="sxs-lookup"><span data-stu-id="65220-110">**CBaseInputPin::EndFlush**</span></span>](cbaseinputpin-endflush.md)
-   [<span data-ttu-id="65220-111">**Cbaseingeputpin:: Receive**</span><span class="sxs-lookup"><span data-stu-id="65220-111">**CBaseInputPin::Receive**</span></span>](cbaseinputpin-receive.md)
-   [<span data-ttu-id="65220-112">**Cbasepin:: checkmediatype**</span><span class="sxs-lookup"><span data-stu-id="65220-112">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="65220-113">**Cbasepin:: getmediatype**</span><span class="sxs-lookup"><span data-stu-id="65220-113">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="65220-114">Abhängig von der Funktion der PIN müssen Sie möglicherweise zusätzliche Methoden in `CBaseInputPin` oder **cbasepin** überschreiben.</span><span class="sxs-lookup"><span data-stu-id="65220-114">Depending on the function of the pin, you might need to override additional methods in `CBaseInputPin` or **CBasePin**.</span></span>



| <span data-ttu-id="65220-115">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="65220-115">Protected Member Variables</span></span>                                                 | <span data-ttu-id="65220-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65220-116">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65220-117">**m- \_ pallocator**</span><span class="sxs-lookup"><span data-stu-id="65220-117">**m\_pAllocator**</span></span>](cbaseinputpin-m-pallocator.md)                        | <span data-ttu-id="65220-118">Zeiger auf die Speicherzuweisung.</span><span class="sxs-lookup"><span data-stu-id="65220-118">Pointer to the memory allocator.</span></span>                                                                            |
| [<span data-ttu-id="65220-119">**\_nur m Brot**</span><span class="sxs-lookup"><span data-stu-id="65220-119">**m\_bReadOnly**</span></span>](cbaseinputpin-m-breadonly.md)                          | <span data-ttu-id="65220-120">Flag, das angibt, ob die Zuweisung schreibgeschützte Medien Beispiele erzeugt.</span><span class="sxs-lookup"><span data-stu-id="65220-120">Flag that indicates whether the allocator produces read-only media samples.</span></span>                                 |
| [<span data-ttu-id="65220-121">**m \_ bleeren**</span><span class="sxs-lookup"><span data-stu-id="65220-121">**m\_bFlushing**</span></span>](cbaseinputpin-m-bflushing.md)                          | <span data-ttu-id="65220-122">Flag, das angibt, ob die PIN zurzeit geleert wird.</span><span class="sxs-lookup"><span data-stu-id="65220-122">Flag that indicates whether the pin is currently flushing.</span></span>                                                  |
| [<span data-ttu-id="65220-123">**m \_ Sample-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="65220-123">**m\_SampleProps**</span></span>](cbaseinputpin-m-sampleprops.md)                      | <span data-ttu-id="65220-124">Eigenschaften des neuesten Beispiels.</span><span class="sxs-lookup"><span data-stu-id="65220-124">Properties of the most recent sample.</span></span>                                                                       |
| <span data-ttu-id="65220-125">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="65220-125">Public Methods</span></span>                                                             | <span data-ttu-id="65220-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65220-126">Description</span></span>                                                                                                 |
| [<span data-ttu-id="65220-127">**Cbaseingeputpin**</span><span class="sxs-lookup"><span data-stu-id="65220-127">**CBaseInputPin**</span></span>](cbaseinputpin-cbaseinputpin.md)                       | <span data-ttu-id="65220-128">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="65220-128">Constructor method.</span></span>                                                                                         |
| [<span data-ttu-id="65220-129">**~ Cbaseingeputpin**</span><span class="sxs-lookup"><span data-stu-id="65220-129">**~CBaseInputPin**</span></span>](cbaseinputpin--cbaseinputpin.md)                     | <span data-ttu-id="65220-130">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="65220-130">Destructor method.</span></span>                                                                                          |
| [<span data-ttu-id="65220-131">**Breakconnect**</span><span class="sxs-lookup"><span data-stu-id="65220-131">**BreakConnect**</span></span>](cbaseinputpin-breakconnect.md)                         | <span data-ttu-id="65220-132">Gibt die PIN von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="65220-132">Releases the pin from a connection.</span></span>                                                                         |
| [<span data-ttu-id="65220-133">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="65220-133">**IsReadOnly**</span></span>](cbaseinputpin-isreadonly.md)                             | <span data-ttu-id="65220-134">Fragt ab, ob die Zuweisung schreibgeschützte Medien Beispiele verwendet.</span><span class="sxs-lookup"><span data-stu-id="65220-134">Queries whether the allocator uses read-only media samples.</span></span>                                                 |
| [<span data-ttu-id="65220-135">**Isleerung**</span><span class="sxs-lookup"><span data-stu-id="65220-135">**IsFlushing**</span></span>](cbaseinputpin-isflushing.md)                             | <span data-ttu-id="65220-136">Fragt ab, ob der Filter zurzeit geleert wird.</span><span class="sxs-lookup"><span data-stu-id="65220-136">Queries whether the filter is currently flushing.</span></span>                                                           |
| [<span data-ttu-id="65220-137">**Checkstreaming**</span><span class="sxs-lookup"><span data-stu-id="65220-137">**CheckStreaming**</span></span>](cbaseinputpin-checkstreaming.md)                     | <span data-ttu-id="65220-138">Bestimmt, ob die PIN Beispiele annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="65220-138">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="65220-139">Virtu.</span><span class="sxs-lookup"><span data-stu-id="65220-139">Virtual.</span></span>                                                     |
| [<span data-ttu-id="65220-140">**Passnotify**</span><span class="sxs-lookup"><span data-stu-id="65220-140">**PassNotify**</span></span>](cbaseinputpin-passnotify.md)                             | <span data-ttu-id="65220-141">Übergibt eine Qualitäts Steuerungs Meldung an das entsprechende-Objekt.</span><span class="sxs-lookup"><span data-stu-id="65220-141">Passes a quality-control message to the appropriate object.</span></span>                                                 |
| [<span data-ttu-id="65220-142">**Inaktiv**</span><span class="sxs-lookup"><span data-stu-id="65220-142">**Inactive**</span></span>](cbaseinputpin-inactive.md)                                 | <span data-ttu-id="65220-143">Benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="65220-143">Notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="65220-144">Virtu.</span><span class="sxs-lookup"><span data-stu-id="65220-144">Virtual.</span></span>                                              |
| [<span data-ttu-id="65220-145">**Sample-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="65220-145">**SampleProps**</span></span>](cbaseinputpin-sampleprops.md)                           | <span data-ttu-id="65220-146">Ruft die Eigenschaften des neuesten Beispiels ab.</span><span class="sxs-lookup"><span data-stu-id="65220-146">Retrieves the properties of the most recent sample.</span></span>                                                         |
| <span data-ttu-id="65220-147">IPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="65220-147">IPin Methods</span></span>                                                               | <span data-ttu-id="65220-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65220-148">Description</span></span>                                                                                                 |
| [<span data-ttu-id="65220-149">**Beginflush**</span><span class="sxs-lookup"><span data-stu-id="65220-149">**BeginFlush**</span></span>](cbaseinputpin-beginflush.md)                             | <span data-ttu-id="65220-150">Startet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="65220-150">Begins a flush operation.</span></span>                                                                                   |
| [<span data-ttu-id="65220-151">**Endflush**</span><span class="sxs-lookup"><span data-stu-id="65220-151">**EndFlush**</span></span>](cbaseinputpin-endflush.md)                                 | <span data-ttu-id="65220-152">Beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="65220-152">Ends a flush operation.</span></span>                                                                                     |
| <span data-ttu-id="65220-153">IMemInputPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="65220-153">IMemInputPin Methods</span></span>                                                       | <span data-ttu-id="65220-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65220-154">Description</span></span>                                                                                                 |
| [<span data-ttu-id="65220-155">**Getallocator**</span><span class="sxs-lookup"><span data-stu-id="65220-155">**GetAllocator**</span></span>](cbaseinputpin-getallocator.md)                         | <span data-ttu-id="65220-156">Ruft die von dieser Pin vorgeschlagene Speicherzuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="65220-156">Retrieves the memory allocator proposed by this pin.</span></span>                                                        |
| [<span data-ttu-id="65220-157">**Notifyzukator**</span><span class="sxs-lookup"><span data-stu-id="65220-157">**NotifyAllocator**</span></span>](cbaseinputpin-notifyallocator.md)                   | <span data-ttu-id="65220-158">Gibt eine Zuweisung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="65220-158">Specifies an allocator for the connection.</span></span>                                                                  |
| [<span data-ttu-id="65220-159">**Getalloserorrequirements**</span><span class="sxs-lookup"><span data-stu-id="65220-159">**GetAllocatorRequirements**</span></span>](cbaseinputpin-getallocatorrequirements.md) | <span data-ttu-id="65220-160">Ruft die von der eingabepin angeforderten zuordnereigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="65220-160">Retrieves the allocator properties requested by the input pin.</span></span>                                              |
| [<span data-ttu-id="65220-161">**Medizinisch**</span><span class="sxs-lookup"><span data-stu-id="65220-161">**Receive**</span></span>](cbaseinputpin-receive.md)                                   | <span data-ttu-id="65220-162">Empfängt das nächste Medien Beispiel im Stream.</span><span class="sxs-lookup"><span data-stu-id="65220-162">Receives the next media sample in the stream.</span></span>                                                               |
| [<span data-ttu-id="65220-163">**Receivemultiple**</span><span class="sxs-lookup"><span data-stu-id="65220-163">**ReceiveMultiple**</span></span>](cbaseinputpin-receivemultiple.md)                   | <span data-ttu-id="65220-164">Empfängt mehrere Stichproben im Stream.</span><span class="sxs-lookup"><span data-stu-id="65220-164">Receives multiple samples in the stream.</span></span>                                                                    |
| [<span data-ttu-id="65220-165">**Receivecanblock**</span><span class="sxs-lookup"><span data-stu-id="65220-165">**ReceiveCanBlock**</span></span>](cbaseinputpin-receivecanblock.md)                   | <span data-ttu-id="65220-166">Bestimmt, ob Aufrufe der [**cbasinput PIN:: Receive**](cbaseinputpin-receive.md) -Methode blockiert werden könnten.</span><span class="sxs-lookup"><span data-stu-id="65220-166">Determines whether calls to the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method might block.</span></span> |
| <span data-ttu-id="65220-167">Iqualitycontrol-Methoden</span><span class="sxs-lookup"><span data-stu-id="65220-167">IQualityControl Methods</span></span>                                                    | <span data-ttu-id="65220-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65220-168">Description</span></span>                                                                                                 |
| [<span data-ttu-id="65220-169">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="65220-169">**Notify**</span></span>](cbaseinputpin-notify.md)                                     | <span data-ttu-id="65220-170">Empfängt eine Qualitäts Steuerungs Meldung.</span><span class="sxs-lookup"><span data-stu-id="65220-170">Receives a quality-control message.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="65220-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65220-171">Requirements</span></span>



| <span data-ttu-id="65220-172">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65220-172">Requirement</span></span> | <span data-ttu-id="65220-173">Wert</span><span class="sxs-lookup"><span data-stu-id="65220-173">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65220-174">Header</span><span class="sxs-lookup"><span data-stu-id="65220-174">Header</span></span><br/>  | <dl> <span data-ttu-id="65220-175"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65220-175"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="65220-176">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65220-176">Library</span></span><br/> | <dl> <span data-ttu-id="65220-177">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="65220-177"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




