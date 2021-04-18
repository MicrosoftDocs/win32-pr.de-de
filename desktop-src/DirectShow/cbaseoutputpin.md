---
description: Die cbaseoutputpin-Klasse ist eine abstrakte Basisklasse, die eine Ausgabe-PIN implementiert.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: Cbaseoutputpin-Klasse (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365543"
---
# <a name="cbaseoutputpin-class"></a><span data-ttu-id="eaee8-103">Cbaseoutputpin-Klasse</span><span class="sxs-lookup"><span data-stu-id="eaee8-103">CBaseOutputPin class</span></span>

![cbaseoutputpin-Klassenhierarchie](images/filter06.png)

<span data-ttu-id="eaee8-105">Die- `CBaseOutputPin` Klasse ist eine abstrakte Basisklasse, die eine Ausgabe-PIN implementiert.</span><span class="sxs-lookup"><span data-stu-id="eaee8-105">The `CBaseOutputPin` class is an abstract base class that implements an output pin.</span></span>

<span data-ttu-id="eaee8-106">Diese Klasse wird von [**cbasepin**](cbasepin.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="eaee8-106">This class derives from [**CBasePin**](cbasepin.md).</span></span> <span data-ttu-id="eaee8-107">Dies unterscheidet sich von **cbasepin** in den folgenden Punkten:</span><span class="sxs-lookup"><span data-stu-id="eaee8-107">It differs from **CBasePin** in the following respects:</span></span>

-   <span data-ttu-id="eaee8-108">Es stellt nur eine Verbindung mit Eingabe Pins her, die die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="eaee8-108">It connects only to input pins that support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="eaee8-109">Es unterstützt den lokalen Speicher Transport über die [**imembelegcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eaee8-109">It supports local memory transport through the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>
-   <span data-ttu-id="eaee8-110">Er lehnt Streamende-, Lösch-und neue Segment Benachrichtigungen ab.</span><span class="sxs-lookup"><span data-stu-id="eaee8-110">It rejects end-of-stream, flush, and new-segment notifications.</span></span> <span data-ttu-id="eaee8-111">(Diese sollten nicht an eine Ausgabepin gesendet werden.)</span><span class="sxs-lookup"><span data-stu-id="eaee8-111">(These should not be sent to an output pin.)</span></span>
-   <span data-ttu-id="eaee8-112">Es stellt Methoden zum Bereitstellen von Abtastungen bereit.</span><span class="sxs-lookup"><span data-stu-id="eaee8-112">It provides methods for delivering samples downstream.</span></span>

<span data-ttu-id="eaee8-113">Wenn die PIN eine Verbindung herstellt, wird von der eingabepin eine Speicherzuweisung angefordert.</span><span class="sxs-lookup"><span data-stu-id="eaee8-113">When the pin connects, it requests a memory allocator from the input pin.</span></span> <span data-ttu-id="eaee8-114">Wenn ein Fehler auftritt, wird ein neues zuordnerobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="eaee8-114">Failing that, it creates a new allocator object.</span></span> <span data-ttu-id="eaee8-115">Die Ausgabepin ist für das Festlegen der zuweicatoreigenschaften verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="eaee8-115">The output pin is responsible for setting the allocator properties.</span></span> <span data-ttu-id="eaee8-116">Dies erfolgt über die reine virtuelle Methode [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="eaee8-116">It does this through the pure virtual method [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span> <span data-ttu-id="eaee8-117">Überschreiben Sie diese Methode in der abgeleiteten Klasse.</span><span class="sxs-lookup"><span data-stu-id="eaee8-117">Override this method in your derived class.</span></span> <span data-ttu-id="eaee8-118">Wenn die Eingabe-PIN beliebige Puffer Anforderungen hat, werden Sie an die **decidebuffersize** -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="eaee8-118">If the input pin has any buffer requirements, they are passed to the **DecideBufferSize** method.</span></span>

<span data-ttu-id="eaee8-119">Rufen Sie die [**cbaseoutputpin:: getdeliverybuffer**](cbaseoutputpin-getdeliverybuffer.md) -Methode auf, um ein leeres Medien Beispiel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="eaee8-119">Call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain an empty media sample.</span></span> <span data-ttu-id="eaee8-120">Rufen Sie die [**cbaseoutputpin::D eliver**](cbaseoutputpin-deliver.md) -Methode auf, um Abtastungen übermitteln.</span><span class="sxs-lookup"><span data-stu-id="eaee8-120">Call the [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) method to deliver samples downstream.</span></span>

<span data-ttu-id="eaee8-121">Ihre abgeleitete Klasse muss die rein virtuelle [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode überschreiben, um den Medientyp während der PIN-Verbindungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="eaee8-121">Your derived class must override the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to validate the media type during pin connections.</span></span>



| <span data-ttu-id="eaee8-122">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="eaee8-122">Protected Member Variables</span></span>                                      | <span data-ttu-id="eaee8-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eaee8-123">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="eaee8-124">**m- \_ pallocator**</span><span class="sxs-lookup"><span data-stu-id="eaee8-124">**m\_pAllocator**</span></span>](cbaseoutputpin-m-pallocator.md)            | <span data-ttu-id="eaee8-125">Zeiger auf die Speicherzuweisung.</span><span class="sxs-lookup"><span data-stu-id="eaee8-125">Pointer to the memory allocator.</span></span>                                           |
| [<span data-ttu-id="eaee8-126">**m \_ pinputpin**</span><span class="sxs-lookup"><span data-stu-id="eaee8-126">**m\_pInputPin**</span></span>](cbaseoutputpin-m-pinputpin.md)              | <span data-ttu-id="eaee8-127">Zeiger auf die Eingabe-PIN, die mit dieser Pin verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="eaee8-127">Pointer to the input pin connected to this pin.</span></span>                            |
| <span data-ttu-id="eaee8-128">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="eaee8-128">Public Methods</span></span>                                                  | <span data-ttu-id="eaee8-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eaee8-129">Description</span></span>                                                                |
| [<span data-ttu-id="eaee8-130">**Cbaseoutputpin**</span><span class="sxs-lookup"><span data-stu-id="eaee8-130">**CBaseOutputPin**</span></span>](cbaseoutputpin-cbaseoutputpin.md)         | <span data-ttu-id="eaee8-131">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="eaee8-131">Constructor method.</span></span>                                                        |
| [<span data-ttu-id="eaee8-132">**Completeconnect**</span><span class="sxs-lookup"><span data-stu-id="eaee8-132">**CompleteConnect**</span></span>](cbaseoutputpin-completeconnect.md)       | <span data-ttu-id="eaee8-133">Schließt eine Verbindung mit einer Eingabe-PIN ab.</span><span class="sxs-lookup"><span data-stu-id="eaee8-133">Completes a connection to an input pin.</span></span> <span data-ttu-id="eaee8-134">Virtu.</span><span class="sxs-lookup"><span data-stu-id="eaee8-134">Virtual.</span></span>                           |
| [<span data-ttu-id="eaee8-135">**Decidezuordcator**</span><span class="sxs-lookup"><span data-stu-id="eaee8-135">**DecideAllocator**</span></span>](cbaseoutputpin-decideallocator.md)       | <span data-ttu-id="eaee8-136">Wählt eine Speicherzuweisung aus.</span><span class="sxs-lookup"><span data-stu-id="eaee8-136">Selects a memory allocator.</span></span> <span data-ttu-id="eaee8-137">Virtu.</span><span class="sxs-lookup"><span data-stu-id="eaee8-137">Virtual.</span></span>                                       |
| [<span data-ttu-id="eaee8-138">**Getdeliverybuffer**</span><span class="sxs-lookup"><span data-stu-id="eaee8-138">**GetDeliveryBuffer**</span></span>](cbaseoutputpin-getdeliverybuffer.md)   | <span data-ttu-id="eaee8-139">Ruft ein Medien Beispiel ab, das einen leeren Puffer enthält.</span><span class="sxs-lookup"><span data-stu-id="eaee8-139">Retrieves a media sample that contains an empty buffer.</span></span> <span data-ttu-id="eaee8-140">Virtu.</span><span class="sxs-lookup"><span data-stu-id="eaee8-140">Virtual.</span></span>           |
| [<span data-ttu-id="eaee8-141">**Bereitstellen**</span><span class="sxs-lookup"><span data-stu-id="eaee8-141">**Deliver**</span></span>](cbaseoutputpin-deliver.md)                       | <span data-ttu-id="eaee8-142">Übermittelt ein Medien Beispiel an die verbundene Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="eaee8-142">Delivers a media sample to the connected input pin.</span></span> <span data-ttu-id="eaee8-143">Virtu.</span><span class="sxs-lookup"><span data-stu-id="eaee8-143">Virtual.</span></span>               |
| [<span data-ttu-id="eaee8-144">**Initzuweisung**</span><span class="sxs-lookup"><span data-stu-id="eaee8-144">**InitAllocator**</span></span>](cbaseoutputpin-initallocator.md)           | <span data-ttu-id="eaee8-145">Erstellt eine Speicherzuweisung.</span><span class="sxs-lookup"><span data-stu-id="eaee8-145">Creates a memory allocator.</span></span> <span data-ttu-id="eaee8-146">Virtu.</span><span class="sxs-lookup"><span data-stu-id="eaee8-146">Virtual.</span></span>                                       |
| [<span data-ttu-id="eaee8-147">**Check Connect**</span><span class="sxs-lookup"><span data-stu-id="eaee8-147">**CheckConnect**</span></span>](cbaseoutputpin-checkconnect.md)             | <span data-ttu-id="eaee8-148">Bestimmt, ob eine PIN-Verbindung geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="eaee8-148">Determines whether a pin connection is suitable.</span></span>                           |
| [<span data-ttu-id="eaee8-149">**Breakconnect**</span><span class="sxs-lookup"><span data-stu-id="eaee8-149">**BreakConnect**</span></span>](cbaseoutputpin-breakconnect.md)             | <span data-ttu-id="eaee8-150">Gibt die PIN von einer Verbindung frei.</span><span class="sxs-lookup"><span data-stu-id="eaee8-150">Releases the pin from a connection.</span></span>                                        |
| [<span data-ttu-id="eaee8-151">**Aktiv**</span><span class="sxs-lookup"><span data-stu-id="eaee8-151">**Active**</span></span>](cbaseoutputpin-active.md)                         | <span data-ttu-id="eaee8-152">Benachrichtigt die PIN, dass der Filter jetzt aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="eaee8-152">Notifies the pin that the filter is now active.</span></span>                            |
| [<span data-ttu-id="eaee8-153">**Inaktiv**</span><span class="sxs-lookup"><span data-stu-id="eaee8-153">**Inactive**</span></span>](cbaseoutputpin-inactive.md)                     | <span data-ttu-id="eaee8-154">Benachrichtigt die PIN, dass der Filter nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="eaee8-154">Notifies the pin that the filter is no longer active.</span></span>                      |
| [<span data-ttu-id="eaee8-155">**Deliverendof**</span><span class="sxs-lookup"><span data-stu-id="eaee8-155">**DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md) | <span data-ttu-id="eaee8-156">Übermittelt eine Benachrichtigung über das Ende des Streams an die verbundene Eingabe-PIN. Virtu.</span><span class="sxs-lookup"><span data-stu-id="eaee8-156">Delivers an end-of-stream notification to the connected input pin.Virtual.</span></span> |
| [<span data-ttu-id="eaee8-157">**Deliverbeginflush**</span><span class="sxs-lookup"><span data-stu-id="eaee8-157">**DeliverBeginFlush**</span></span>](cbaseoutputpin-deliverbeginflush.md)   | <span data-ttu-id="eaee8-158">Fordert an, dass die verbundene Eingabe-PIN einen Leerungs Vorgang startet.</span><span class="sxs-lookup"><span data-stu-id="eaee8-158">Requests the connected input pin to begin a flush operation.</span></span> <span data-ttu-id="eaee8-159">Virtu.</span><span class="sxs-lookup"><span data-stu-id="eaee8-159">Virtual.</span></span>      |
| [<span data-ttu-id="eaee8-160">**Deliverendflush**</span><span class="sxs-lookup"><span data-stu-id="eaee8-160">**DeliverEndFlush**</span></span>](cbaseoutputpin-deliverendflush.md)       | <span data-ttu-id="eaee8-161">Fordert die verbundene Eingabe-PIN an, einen Leerungs Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="eaee8-161">Requests the connected input pin to end a flush operation.</span></span> <span data-ttu-id="eaee8-162">Virtu.</span><span class="sxs-lookup"><span data-stu-id="eaee8-162">Virtual.</span></span>        |
| [<span data-ttu-id="eaee8-163">**Delivernewsegment**</span><span class="sxs-lookup"><span data-stu-id="eaee8-163">**DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)   | <span data-ttu-id="eaee8-164">Übermittelt eine Benachrichtigung über ein neues Segment an die verbundene Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="eaee8-164">Delivers a new-segment notification to the connected input pin.</span></span> <span data-ttu-id="eaee8-165">Virtu.</span><span class="sxs-lookup"><span data-stu-id="eaee8-165">Virtual.</span></span>   |
| <span data-ttu-id="eaee8-166">Reine virtuelle Methoden</span><span class="sxs-lookup"><span data-stu-id="eaee8-166">Pure Virtual Methods</span></span>                                            | <span data-ttu-id="eaee8-167">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eaee8-167">Description</span></span>                                                                |
| [<span data-ttu-id="eaee8-168">**Decidebuffersize**</span><span class="sxs-lookup"><span data-stu-id="eaee8-168">**DecideBufferSize**</span></span>](cbaseoutputpin-decidebuffersize.md)     | <span data-ttu-id="eaee8-169">Legt die Puffer Anforderungen fest.</span><span class="sxs-lookup"><span data-stu-id="eaee8-169">Sets the buffer requirements.</span></span>                                              |
| <span data-ttu-id="eaee8-170">IPin-Methoden</span><span class="sxs-lookup"><span data-stu-id="eaee8-170">IPin Methods</span></span>                                                    | <span data-ttu-id="eaee8-171">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eaee8-171">Description</span></span>                                                                |
| [<span data-ttu-id="eaee8-172">**Beginflush**</span><span class="sxs-lookup"><span data-stu-id="eaee8-172">**BeginFlush**</span></span>](cbaseoutputpin-beginflush.md)                 | <span data-ttu-id="eaee8-173">Startet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="eaee8-173">Begins a flush operation.</span></span>                                                  |
| [<span data-ttu-id="eaee8-174">**Endflush**</span><span class="sxs-lookup"><span data-stu-id="eaee8-174">**EndFlush**</span></span>](cbaseoutputpin-endflush.md)                     | <span data-ttu-id="eaee8-175">Beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="eaee8-175">Ends a flush operation.</span></span>                                                    |
| [<span data-ttu-id="eaee8-176">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="eaee8-176">**EndOfStream**</span></span>](cbaseoutputpin-endofstream.md)               | <span data-ttu-id="eaee8-177">Benachrichtigt die PIN, dass keine weiteren Daten erwartet werden.</span><span class="sxs-lookup"><span data-stu-id="eaee8-177">Notifies the pin that no additional data is expected.</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="eaee8-178">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eaee8-178">Requirements</span></span>



| <span data-ttu-id="eaee8-179">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eaee8-179">Requirement</span></span> | <span data-ttu-id="eaee8-180">Wert</span><span class="sxs-lookup"><span data-stu-id="eaee8-180">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaee8-181">Header</span><span class="sxs-lookup"><span data-stu-id="eaee8-181">Header</span></span><br/>  | <dl> <span data-ttu-id="eaee8-182"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eaee8-182"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eaee8-183">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eaee8-183">Library</span></span><br/> | <dl> <span data-ttu-id="eaee8-184">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="eaee8-184"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




