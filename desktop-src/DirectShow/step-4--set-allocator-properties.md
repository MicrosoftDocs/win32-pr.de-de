---
description: Schritt 4.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Schritt 4. Festlegen von zuordnereigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32d5e3affba32b96dc93cb97e1886322bc6f2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350034"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="d26d8-104">Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="d26d8-104">Step 4.</span></span> <span data-ttu-id="d26d8-105">Festlegen von zuordnereigenschaften</span><span class="sxs-lookup"><span data-stu-id="d26d8-105">Set Allocator Properties</span></span>

<span data-ttu-id="d26d8-106">Dies ist Schritt 4 des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d26d8-106">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="d26d8-107">Dieser Schritt ist für Filter, die von **ctransinplacefilter** abgeleitet werden, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d26d8-107">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="d26d8-108">Nachdem zwei Pins einem Medientyp zugestimmt haben, wählen Sie eine Zuweisung für die Verbindungs-und Aushandlungs Eigenschaften aus, z. b. die Puffergröße und die Anzahl der Puffer.</span><span class="sxs-lookup"><span data-stu-id="d26d8-108">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="d26d8-109">In der **ctransformfilter** -Klasse gibt es zwei Zuweisungen, eine für die Upstream-Pin-Verbindung und eine für die downstreampin-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d26d8-109">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="d26d8-110">Der upstreamfilter wählt die upstreamzuweisung aus und wählt außerdem die zuordnereigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="d26d8-110">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="d26d8-111">Die Eingabe-PIN akzeptiert das, was der Upstream-Filter entscheidet.</span><span class="sxs-lookup"><span data-stu-id="d26d8-111">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="d26d8-112">Wenn Sie dieses Verhalten ändern müssen, überschreiben Sie die [**cbasonputpin:: notifyzucator**](cbaseinputpin-notifyallocator.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d26d8-112">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="d26d8-113">Mit dem Ausgabepin des Transformations Filters wird die Downstream-Zuweisung ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="d26d8-113">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="d26d8-114">Sie führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d26d8-114">It performs the following steps:</span></span>

1.  <span data-ttu-id="d26d8-115">Wenn der Downstream-Filter eine Zuweisung bereitstellen kann, wird diese von der Ausgabepin verwendet.</span><span class="sxs-lookup"><span data-stu-id="d26d8-115">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="d26d8-116">Andernfalls erstellt die Ausgabe-PIN eine neue Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="d26d8-116">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="d26d8-117">Durch den Aufruf von [**IMemInputPin:: getallocatorrequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements)erhält die Ausgabepin die zuordneranforderungen des nachgelagerten Filters (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="d26d8-117">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="d26d8-118">Mit der Ausgabe-PIN wird die [**ctransformfilter::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) -Methode des Transformations Filters aufgerufen, die rein virtuell ist.</span><span class="sxs-lookup"><span data-stu-id="d26d8-118">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="d26d8-119">Die Parameter für diese Methode sind ein Zeiger auf die Zuweisung und eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) Struktur mit den Anforderungen des downstreamfilters.</span><span class="sxs-lookup"><span data-stu-id="d26d8-119">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="d26d8-120">Wenn der Downstream-Filter keine zuordneranforderungen aufweist, wird die-Struktur mit nulgerwert aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="d26d8-120">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="d26d8-121">In der **decidebuffersize** -Methode legt die abgeleitete Klasse die zuordnereigenschaften fest, indem [**imemzuordcator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d26d8-121">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="d26d8-122">Im Allgemeinen wählt die abgeleitete Klasse zuordnereigenschaften basierend auf dem Ausgabeformat, den Anforderungen des downstreamfilters und den Anforderungen des Filters aus.</span><span class="sxs-lookup"><span data-stu-id="d26d8-122">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="d26d8-123">Versuchen Sie, die Eigenschaften auszuwählen, die mit der Anforderung des downstreamfilters kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="d26d8-123">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="d26d8-124">Andernfalls lehnt der Downstream-Filter die Verbindung möglicherweise ab.</span><span class="sxs-lookup"><span data-stu-id="d26d8-124">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="d26d8-125">Im folgenden Beispiel legt der RLE-Encoder die minimalen Werte für die Puffergröße, die Puffer Ausrichtung und die Puffer Anzahl fest.</span><span class="sxs-lookup"><span data-stu-id="d26d8-125">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="d26d8-126">Für das Präfix wird ein beliebiger Wert verwendet, den der Downstream-Filter angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="d26d8-126">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="d26d8-127">Das Präfix ist in der Regel 0 (null) Bytes, einige Filter erfordern es jedoch.</span><span class="sxs-lookup"><span data-stu-id="d26d8-127">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="d26d8-128">Der [AVI MUX](avi-mux-filter.md) -Filter verwendet beispielsweise das Präfix zum Schreiben von RIFF Headern.</span><span class="sxs-lookup"><span data-stu-id="d26d8-128">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


```C++
HRESULT CRleFilter::DecideBufferSize(
    IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp)
{
    AM_MEDIA_TYPE mt;
    HRESULT hr = m_pOutput->ConnectionMediaType(&mt);
    if (FAILED(hr))
    {
        return hr;
    }

    ASSERT(mt.formattype == FORMAT_VideoInfo);
    BITMAPINFOHEADER *pbmi = HEADER(mt.pbFormat);
    pProp->cbBuffer = DIBSIZE(*pbmi) * 2; 
    if (pProp->cbAlign == 0)
    {
        pProp->cbAlign = 1;
    }
    if (pProp->cBuffers == 0)
    {
        pProp->cBuffers = 1;
    }
    // Release the format block.
    FreeMediaType(mt);

    // Set allocator properties.
    ALLOCATOR_PROPERTIES Actual;
    hr = pAlloc->SetProperties(pProp, &Actual);
    if (FAILED(hr)) 
    {
        return hr;
    }
    // Even when it succeeds, check the actual result.
    if (pProp->cbBuffer > Actual.cbBuffer) 
    {
        return E_FAIL;
    }
    return S_OK;
}
```



<span data-ttu-id="d26d8-129">Die Zuweisung ist möglicherweise nicht in der Lage, Ihre Anforderung genau abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="d26d8-129">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="d26d8-130">Daher gibt die **SetProperties** -Methode das tatsächliche Ergebnis in einer separaten **zuordnereigenschafts \_** -Struktur zurück (der *tatsächliche* Parameter im vorherigen Beispiel).</span><span class="sxs-lookup"><span data-stu-id="d26d8-130">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="d26d8-131">Auch wenn **SetProperties** erfolgreich ist, sollten Sie das Ergebnis überprüfen, um sicherzustellen, dass Sie die Mindestanforderungen Ihres Filters erfüllen.</span><span class="sxs-lookup"><span data-stu-id="d26d8-131">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="d26d8-132">**Benutzerdefinierte Zuweisungen**</span><span class="sxs-lookup"><span data-stu-id="d26d8-132">**Custom Allocators**</span></span>

<span data-ttu-id="d26d8-133">Standardmäßig verwenden alle Filterklassen die [**cmemzuordcator**](cmemallocator.md) -Klasse für ihre Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="d26d8-133">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="d26d8-134">Diese Klasse ordnet Arbeitsspeicher aus dem virtuellen Adressraum des Client Prozesses zu (mit **virtualbelegc**).</span><span class="sxs-lookup"><span data-stu-id="d26d8-134">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="d26d8-135">Wenn Ihr Filter eine andere Art von Arbeitsspeicher (z. b. DirectDraw-Oberflächen) verwenden muss, können Sie eine benutzerdefinierte Zuweisung implementieren.</span><span class="sxs-lookup"><span data-stu-id="d26d8-135">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="d26d8-136">Sie können die Klasse [**cbasezucator**](cbaseallocator.md) verwenden oder eine vollständig neue zuordnerklasse schreiben.</span><span class="sxs-lookup"><span data-stu-id="d26d8-136">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="d26d8-137">Wenn Ihr Filter über einen benutzerdefinierten Zuweiser verfügt, überschreiben Sie die folgenden Methoden, je nachdem, welche PIN die Zuweisung verwendet:</span><span class="sxs-lookup"><span data-stu-id="d26d8-137">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="d26d8-138">Eingabe-PIN: [**cbaseinputpin:: getallocator**](cbaseinputpin-getallocator.md) und [**cbaseinputpin:: notifyzuweisung**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="d26d8-138">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="d26d8-139">Ausgabe-PIN: [**cbaseoutputpin::D ecidezuordcator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="d26d8-139">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="d26d8-140">Wenn der andere Filter die Verbindung mithilfe Ihrer benutzerdefinierten Zuweisung ablehnt, kann der Filter entweder die Verbindung nicht herstellen, oder es kann eine Verbindung mit der Zuweisung des anderen Filters hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d26d8-140">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="d26d8-141">Im letzteren Fall müssen Sie möglicherweise ein internes Flag festlegen, das den Typ der Zuweisung angibt.</span><span class="sxs-lookup"><span data-stu-id="d26d8-141">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="d26d8-142">Ein Beispiel für diesen Ansatz finden Sie unter [**cdrawimage-Klasse**](cdrawimage.md).</span><span class="sxs-lookup"><span data-stu-id="d26d8-142">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="d26d8-143">Weiter: [Schritt 5. Transformieren Sie das Bild](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="d26d8-143">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d26d8-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d26d8-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d26d8-145">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="d26d8-145">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



