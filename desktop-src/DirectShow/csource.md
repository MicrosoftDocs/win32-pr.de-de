---
description: Die CSource-Klasse ist eine Basisklasse zum Implementieren von Quell filtern. Ein von CSource abgeleiteter Filter enthält eine oder mehrere aus der csourcestream-Klasse abgeleitete Ausgabe Pins. Jede Ausgabepin erstellt einen Arbeits Thread, der die Medien Beispiele nach unten verschiebt.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: CSource-Klasse (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368588"
---
# <a name="csource-class"></a><span data-ttu-id="16aaa-105">CSource-Klasse</span><span class="sxs-lookup"><span data-stu-id="16aaa-105">CSource class</span></span>

![CSource-Klassenhierarchie](images/source01.png)

<span data-ttu-id="16aaa-107">Die **CSource** -Klasse ist eine Basisklasse zum Implementieren von Quell filtern.</span><span class="sxs-lookup"><span data-stu-id="16aaa-107">The **CSource** class is a base class for implementing source filters.</span></span> <span data-ttu-id="16aaa-108">Ein von **CSource** abgeleiteter Filter enthält eine oder mehrere aus der [**csourcestream**](csourcestream.md) -Klasse abgeleitete Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="16aaa-108">A filter derived from **CSource** contains one or more output pins derived from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="16aaa-109">Jede Ausgabepin erstellt einen Arbeits Thread, der die Medien Beispiele nach unten verschiebt.</span><span class="sxs-lookup"><span data-stu-id="16aaa-109">Each output pin creates a worker thread that pushes media samples downstream.</span></span>

> [!Note]  
> <span data-ttu-id="16aaa-110">Die **CSource** -Klasse unterstützt das Push-Modell für den Datenfluss.</span><span class="sxs-lookup"><span data-stu-id="16aaa-110">The **CSource** class is designed to support the push model for data flow.</span></span> <span data-ttu-id="16aaa-111">Diese Klasse wird nicht zum Erstellen von Datei Leser Filtern empfohlen.</span><span class="sxs-lookup"><span data-stu-id="16aaa-111">This class is not recommended for creating file-reader filters.</span></span> <span data-ttu-id="16aaa-112">Datei Reader sollten das Pull-Modell über die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="16aaa-112">File readers should support the pull model, through the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="16aaa-113">Weitere Informationen finden Sie unter [Datenfluss für Filter Entwickler](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="16aaa-113">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

 



| <span data-ttu-id="16aaa-114">Geschützte Member-Variablen</span><span class="sxs-lookup"><span data-stu-id="16aaa-114">Protected Member Variables</span></span>                     | <span data-ttu-id="16aaa-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16aaa-115">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="16aaa-116">**m- \_ ipins**</span><span class="sxs-lookup"><span data-stu-id="16aaa-116">**m\_iPins**</span></span>](csource-m-ipins.md)            | <span data-ttu-id="16aaa-117">Anzahl der Pins für den Filter.</span><span class="sxs-lookup"><span data-stu-id="16aaa-117">Number of pins on the filter.</span></span>                                |
| [<span data-ttu-id="16aaa-118">**m- \_ Paare**</span><span class="sxs-lookup"><span data-stu-id="16aaa-118">**m\_paStreams**</span></span>](csource-m-pastreams.md)    | <span data-ttu-id="16aaa-119">Array von Pins.</span><span class="sxs-lookup"><span data-stu-id="16aaa-119">Array of pins.</span></span>                                               |
| [<span data-ttu-id="16aaa-120">**m \_ cstatus**</span><span class="sxs-lookup"><span data-stu-id="16aaa-120">**m\_cStateLock**</span></span>](csource-m-cstatelock.md)  | <span data-ttu-id="16aaa-121">Kritisches Abschnitts Objekt, das den Filter Zustand schützt.</span><span class="sxs-lookup"><span data-stu-id="16aaa-121">Critical section object that protects the filter state.</span></span>      |
| <span data-ttu-id="16aaa-122">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="16aaa-122">Public Methods</span></span>                                 | <span data-ttu-id="16aaa-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16aaa-123">Description</span></span>                                                  |
| [<span data-ttu-id="16aaa-124">**CSource**</span><span class="sxs-lookup"><span data-stu-id="16aaa-124">**CSource**</span></span>](csource-csource.md)             | <span data-ttu-id="16aaa-125">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="16aaa-125">Constructor method.</span></span>                                          |
| [<span data-ttu-id="16aaa-126">**~ CSource**</span><span class="sxs-lookup"><span data-stu-id="16aaa-126">**~CSource**</span></span>](csource--csource.md)           | <span data-ttu-id="16aaa-127">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="16aaa-127">Destructor method.</span></span>                                           |
| [<span data-ttu-id="16aaa-128">**Getpincount**</span><span class="sxs-lookup"><span data-stu-id="16aaa-128">**GetPinCount**</span></span>](csource-getpincount.md)     | <span data-ttu-id="16aaa-129">Ruft die Anzahl der Pins für den Filter ab.</span><span class="sxs-lookup"><span data-stu-id="16aaa-129">Retrieves the number of pins on the filter.</span></span>                  |
| [<span data-ttu-id="16aaa-130">**Getpin**</span><span class="sxs-lookup"><span data-stu-id="16aaa-130">**GetPin**</span></span>](csource-getpin.md)               | <span data-ttu-id="16aaa-131">Ruft eine PIN ab.</span><span class="sxs-lookup"><span data-stu-id="16aaa-131">Retrieves a pin.</span></span>                                             |
| [<span data-ttu-id="16aaa-132">**pstatus-Datei**</span><span class="sxs-lookup"><span data-stu-id="16aaa-132">**pStateLock**</span></span>](csource--pstatelock.md)      | <span data-ttu-id="16aaa-133">Ruft einen Zeiger auf das kritische Abschnitts Objekt des Filters ab.</span><span class="sxs-lookup"><span data-stu-id="16aaa-133">Retrieves a pointer to the filter's critical section object.</span></span> |
| [<span data-ttu-id="16aaa-134">**Addpin**</span><span class="sxs-lookup"><span data-stu-id="16aaa-134">**AddPin**</span></span>](csource-addpin.md)               | <span data-ttu-id="16aaa-135">Fügt dem Filter eine neue Ausgabe-PIN hinzu.</span><span class="sxs-lookup"><span data-stu-id="16aaa-135">Adds a new output pin to the filter.</span></span>                         |
| [<span data-ttu-id="16aaa-136">**Removepin**</span><span class="sxs-lookup"><span data-stu-id="16aaa-136">**RemovePin**</span></span>](csource-removepin.md)         | <span data-ttu-id="16aaa-137">Entfernt eine angegebene PIN aus dem Filter.</span><span class="sxs-lookup"><span data-stu-id="16aaa-137">Removes a specified pin from the filter.</span></span>                     |
| [<span data-ttu-id="16aaa-138">**Findpinnumber**</span><span class="sxs-lookup"><span data-stu-id="16aaa-138">**FindPinNumber**</span></span>](csource-findpinnumber.md) | <span data-ttu-id="16aaa-139">Ruft die Nummer einer angegebenen PIN für den Filter ab.</span><span class="sxs-lookup"><span data-stu-id="16aaa-139">Retrieves the number of a specified pin on the filter.</span></span>       |
| <span data-ttu-id="16aaa-140">Ibasefilter-Methoden</span><span class="sxs-lookup"><span data-stu-id="16aaa-140">IBaseFilter Methods</span></span>                            | <span data-ttu-id="16aaa-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16aaa-141">Description</span></span>                                                  |
| [<span data-ttu-id="16aaa-142">**Findpin**</span><span class="sxs-lookup"><span data-stu-id="16aaa-142">**FindPin**</span></span>](csource-findpin.md)             | <span data-ttu-id="16aaa-143">Ruft die PIN mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="16aaa-143">Retrieves the pin with the specified identifier.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="16aaa-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16aaa-144">Remarks</span></span>

<span data-ttu-id="16aaa-145">Gehen Sie folgendermaßen vor, um eine Ausgabe-PIN zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="16aaa-145">To implement an output pin, do the following:</span></span>

-   <span data-ttu-id="16aaa-146">Leiten Sie eine Klasse von [**csourcestream**](csourcestream.md)ab.</span><span class="sxs-lookup"><span data-stu-id="16aaa-146">Derive a class from [**CSourceStream**](csourcestream.md).</span></span>
-   <span data-ttu-id="16aaa-147">Überschreiben Sie die [**csourcestream:: getmediatype**](csourcestream-getmediatype.md) -Methode und möglicherweise die [**csourcestream:: checkmediatype**](csourcestream-checkmediatype.md) -Methode, die die Medientypen für die PIN überprüfen.</span><span class="sxs-lookup"><span data-stu-id="16aaa-147">Override the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method and possibly the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method, which validate media types for the pin.</span></span>
-   <span data-ttu-id="16aaa-148">Implementieren Sie die [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) -Methode, die die Puffer Anforderungen der PIN zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="16aaa-148">Implement the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method, which returns the pin's buffer requirements.</span></span>
-   <span data-ttu-id="16aaa-149">Implementieren Sie die [**csourcestream:: FillBuffer**](csourcestream-fillbuffer.md) -Methode, die einen Medien Beispiel Puffer mit Daten füllt.</span><span class="sxs-lookup"><span data-stu-id="16aaa-149">Implement the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which fills a media sample buffer with data.</span></span>

<span data-ttu-id="16aaa-150">Gehen Sie folgendermaßen vor, um den Filter zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="16aaa-150">To implement the filter, do the following:</span></span>

-   <span data-ttu-id="16aaa-151">Leiten Sie eine Klasse von **CSource** ab.</span><span class="sxs-lookup"><span data-stu-id="16aaa-151">Derive a class from **CSource**.</span></span>
-   <span data-ttu-id="16aaa-152">Erstellen Sie im Konstruktor eine oder mehrere aus [**csourcestream**](csourcestream.md)abgeleitete Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="16aaa-152">In the constructor, create one or more output pins derived from [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="16aaa-153">Die Pins fügen sich automatisch dem Filter in den Konstruktormethoden hinzu und entfernen sich selbst in ihren demarkermethoden.</span><span class="sxs-lookup"><span data-stu-id="16aaa-153">The pins automatically add themselves to the filter in their constructor methods, and remove themselves in their destructor methods.</span></span>

<span data-ttu-id="16aaa-154">Um den Filter Zustand zwischen mehreren Threads zu synchronisieren, müssen Sie die [**CSource::p statelock**](csource--pstatelock.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="16aaa-154">To synchronize the filter state among multiple threads, call the [**CSource::pStateLock**](csource--pstatelock.md) method.</span></span> <span data-ttu-id="16aaa-155">Diese Methode gibt einen Zeiger auf den kritischen Abschnitt des Filter Zustands zurück.</span><span class="sxs-lookup"><span data-stu-id="16aaa-155">This method returns a pointer to the filter-state critical section.</span></span> <span data-ttu-id="16aaa-156">Verwenden Sie die [**cautolock**](cautolock.md) -Klasse, um den kritischen Abschnitt zu halten.</span><span class="sxs-lookup"><span data-stu-id="16aaa-156">Use the [**CAutoLock**](cautolock.md) class to hold the critical section.</span></span> <span data-ttu-id="16aaa-157">Von einer PIN aus können Sie wie folgt aus der [**cbasepin:: m \_ pFilter**](cbasepin-m-pfilter.md) -Element Variablen der PIN auf **pstatus-ck** zugreifen:</span><span class="sxs-lookup"><span data-stu-id="16aaa-157">From a pin, you can access **pStateLock** from the pin's [**CBasePin::m\_pFilter**](cbasepin-m-pfilter.md) member variable, as follows:</span></span>


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a><span data-ttu-id="16aaa-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16aaa-158">Requirements</span></span>



| <span data-ttu-id="16aaa-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16aaa-159">Requirement</span></span> | <span data-ttu-id="16aaa-160">Wert</span><span class="sxs-lookup"><span data-stu-id="16aaa-160">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16aaa-161">Header</span><span class="sxs-lookup"><span data-stu-id="16aaa-161">Header</span></span><br/>  | <dl> <span data-ttu-id="16aaa-162"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16aaa-162"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="16aaa-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="16aaa-163">Library</span></span><br/> | <dl> <span data-ttu-id="16aaa-164">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="16aaa-164"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16aaa-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16aaa-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16aaa-166">Schreiben von Quell Filtern</span><span class="sxs-lookup"><span data-stu-id="16aaa-166">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




