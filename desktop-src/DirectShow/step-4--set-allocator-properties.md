---
description: Legen Sie Zuweisungseigenschaften als Teil des Schreibens eines Transformationsfilters fest. Der Ausgabepin des Transformationsfilters wählt die Downstreamzuweisung aus.
ms.assetid: c2fd6d8b-b239-45e4-9c02-41edafa58762
title: Schritt 4. Festlegen von Zuweisungseigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ee7d9ecdc85b63ec6bd774a3a47e0e9399dcf3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406823"
---
# <a name="step-4-set-allocator-properties"></a><span data-ttu-id="de548-105">Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="de548-105">Step 4.</span></span> <span data-ttu-id="de548-106">Festlegen von Zuweisungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="de548-106">Set Allocator Properties</span></span>

<span data-ttu-id="de548-107">Dies ist Schritt 4 des Tutorials [Schreiben von Transformationsfiltern.](writing-transform-filters.md)</span><span class="sxs-lookup"><span data-stu-id="de548-107">This is step 4 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

> [!Note]  
> <span data-ttu-id="de548-108">Dieser Schritt ist für Filter, die von **CTransInPlaceFilter** abgeleitet sind, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="de548-108">This step is not required for filters that derive from **CTransInPlaceFilter**.</span></span>

 

<span data-ttu-id="de548-109">Nachdem sich zwei Pins auf einen Medientyp einigen, wählen sie eine Zuweisung für die Verbindung aus und handeln Zuweisungseigenschaften aus, z. B. die Puffergröße und die Anzahl der Puffer.</span><span class="sxs-lookup"><span data-stu-id="de548-109">After two pins agree on a media type, they select an allocator for the connection and negotiate allocator properties, such as the buffer size and the number of buffers.</span></span>

<span data-ttu-id="de548-110">In der **CTransformFilter-Klasse** gibt es zwei Zuweisungen: eine für die Upstream-Pinverbindung und eine für die Downstream-Pinverbindung.</span><span class="sxs-lookup"><span data-stu-id="de548-110">In the **CTransformFilter** class, there are two allocators, one for the upstream pin connection and one for the downstream pin connection.</span></span> <span data-ttu-id="de548-111">Der Upstreamfilter wählt die Upstreamzuweisung und auch die Zuweisungseigenschaften aus.</span><span class="sxs-lookup"><span data-stu-id="de548-111">The upstream filter selects the upstream allocator and also chooses the allocator properties.</span></span> <span data-ttu-id="de548-112">Der Eingabepin akzeptiert alles, was der Upstreamfilter entscheidet.</span><span class="sxs-lookup"><span data-stu-id="de548-112">The input pin accepts whatever the upstream filter decides.</span></span> <span data-ttu-id="de548-113">Wenn Sie dieses Verhalten ändern müssen, überschreiben Sie die [**CBaseInputPin::NotifyAllocator-Methode.**](cbaseinputpin-notifyallocator.md)</span><span class="sxs-lookup"><span data-stu-id="de548-113">If you need to modify this behavior, override the [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md) method.</span></span>

<span data-ttu-id="de548-114">Der Ausgabepin des Transformationsfilters wählt die Downstreamzuweisung aus.</span><span class="sxs-lookup"><span data-stu-id="de548-114">The transform filter's output pin selects the downstream allocator.</span></span> <span data-ttu-id="de548-115">Sie führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="de548-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="de548-116">Wenn der Downstreamfilter eine Zuweisung bereitstellen kann, verwendet der Ausgabepin diesen.</span><span class="sxs-lookup"><span data-stu-id="de548-116">If the downstream filter can provide an allocator, the output pin uses that one.</span></span> <span data-ttu-id="de548-117">Andernfalls erstellt der Ausgabepin eine neue Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="de548-117">Otherwise, the output pin creates a new allocator.</span></span>
2.  <span data-ttu-id="de548-118">Der Ausgabepin ruft die Zuweisungsanforderungen des Downstreamfilters ab (sofern vorhanden), indem [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="de548-118">The output pin gets the downstream filter's allocator requirements (if any) by calling [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements).</span></span>
3.  <span data-ttu-id="de548-119">Der Ausgabepin ruft die rein virtuelle [**CTransformFilter::D ecideBufferSize-Methode**](ctransformfilter-decidebuffersize.md) des Transformationsfilters auf.</span><span class="sxs-lookup"><span data-stu-id="de548-119">The output pin calls the transform filter's [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which is pure virtual.</span></span> <span data-ttu-id="de548-120">Die Parameter für diese Methode sind ein Zeiger auf die Zuweisung und eine [**ALLOCATOR \_ PROPERTIES-Struktur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) mit den Anforderungen des Downstreamfilters.</span><span class="sxs-lookup"><span data-stu-id="de548-120">The parameters to this method are a pointer to the allocator and an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure with the downstream filter's requirements.</span></span> <span data-ttu-id="de548-121">Wenn der Downstreamfilter keine Zuweisungsanforderungen aufweist, wird die Struktur auf null gesetzt.</span><span class="sxs-lookup"><span data-stu-id="de548-121">If the downstream filter has no allocator requirements, the structure is zeroed out.</span></span>
4.  <span data-ttu-id="de548-122">In der **DecideBufferSize-Methode** legt die abgeleitete Klasse die Zuweisungseigenschaften fest, indem [**sie IMemAllocator::SetProperties aufruft.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties)</span><span class="sxs-lookup"><span data-stu-id="de548-122">In the **DecideBufferSize** method, the derived class sets the allocator properties by calling [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties).</span></span>

<span data-ttu-id="de548-123">Im Allgemeinen wählt die abgeleitete Klasse Zuweisungseigenschaften basierend auf dem Ausgabeformat, den Anforderungen des Downstreamfilters und den eigenen Anforderungen des Filters aus.</span><span class="sxs-lookup"><span data-stu-id="de548-123">Generally, the derived class will select allocator properties based on the output format, the downstream filter's requirements, and the filter's own requirements.</span></span> <span data-ttu-id="de548-124">Versuchen Sie, Eigenschaften auszuwählen, die mit der Anforderung des Downstreamfilters kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="de548-124">Try to select properties that are compatible with the downstream filter's request.</span></span> <span data-ttu-id="de548-125">Andernfalls kann der Downstreamfilter die Verbindung ablehnen.</span><span class="sxs-lookup"><span data-stu-id="de548-125">Otherwise, the downstream filter might reject the connection.</span></span>

<span data-ttu-id="de548-126">Im folgenden Beispiel legt der RLE-Encoder Mindestwerte für Puffergröße, Pufferausrichtung und Pufferanzahl fest.</span><span class="sxs-lookup"><span data-stu-id="de548-126">In the following example, the RLE encoder sets minimum values for the buffer size, buffer alignment, and buffer count.</span></span> <span data-ttu-id="de548-127">Für das Präfix wird der Wert verwendet, den der Downstreamfilter angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="de548-127">For the prefix, it uses whatever value the downstream filter requested.</span></span> <span data-ttu-id="de548-128">Das Präfix ist in der Regel 0 Bytes, aber einige Filter erfordern es.</span><span class="sxs-lookup"><span data-stu-id="de548-128">The prefix is typically zero bytes, but some filters require it.</span></span> <span data-ttu-id="de548-129">Beispielsweise verwendet der [AVI Mux-Filter](avi-mux-filter.md) das Präfix, um HEADER zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="de548-129">For example, the [AVI Mux](avi-mux-filter.md) filter uses the prefix to write RIFF headers.</span></span>


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



<span data-ttu-id="de548-130">Die Zuweisung kann möglicherweise nicht genau mit Ihrer Anforderung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="de548-130">The allocator may not be able to match your request exactly.</span></span> <span data-ttu-id="de548-131">Daher gibt die **SetProperties-Methode** das tatsächliche Ergebnis in einer separaten **ALLOCATOR \_ PROPERTIES-Struktur** zurück (der *Actual-Parameter* im vorherigen Beispiel).</span><span class="sxs-lookup"><span data-stu-id="de548-131">Therefore, the **SetProperties** method returns the actual result in a separate **ALLOCATOR\_PROPERTIES** structure (the *Actual* parameter, in the previous example).</span></span> <span data-ttu-id="de548-132">Auch wenn **SetProperties** erfolgreich ist, sollten Sie das Ergebnis überprüfen, um sicherzustellen, dass sie die Mindestanforderungen Ihres Filters erfüllen.</span><span class="sxs-lookup"><span data-stu-id="de548-132">Even when **SetProperties** succeeds, you should check the result to make sure they meet your filter's minimum requirements.</span></span>

<span data-ttu-id="de548-133">**Benutzerdefinierte Zuweisungen**</span><span class="sxs-lookup"><span data-stu-id="de548-133">**Custom Allocators**</span></span>

<span data-ttu-id="de548-134">Standardmäßig verwenden alle Filterklassen die [**CMemAllocator-Klasse**](cmemallocator.md) für ihre Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="de548-134">By default, all of the filter classes use the [**CMemAllocator**](cmemallocator.md) class for their allocators.</span></span> <span data-ttu-id="de548-135">Diese Klasse belegt Arbeitsspeicher aus dem virtuellen Adressraum des Clientprozesses (mit **VirtualAlloc**).</span><span class="sxs-lookup"><span data-stu-id="de548-135">This class allocates memory from the virtual address space of the client process (using **VirtualAlloc**).</span></span> <span data-ttu-id="de548-136">Wenn Ihr Filter eine andere Art von Arbeitsspeicher verwenden muss, z. B. DirectDraw-Oberflächen, können Sie eine benutzerdefinierte Zuweisung implementieren.</span><span class="sxs-lookup"><span data-stu-id="de548-136">If your filter needs to use some other kind of memory, such as DirectDraw surfaces, you can implement a custom allocator.</span></span> <span data-ttu-id="de548-137">Sie können die [**CBaseAllocator-Klasse**](cbaseallocator.md) verwenden oder eine völlig neue Zuweisungsklasse schreiben.</span><span class="sxs-lookup"><span data-stu-id="de548-137">You can use the [**CBaseAllocator**](cbaseallocator.md) class or write an entirely new allocator class.</span></span> <span data-ttu-id="de548-138">Wenn Ihr Filter über eine benutzerdefinierte Zuweisung verfügt, überschreiben Sie die folgenden Methoden, je nachdem, welcher Pin die Zuweisung verwendet:</span><span class="sxs-lookup"><span data-stu-id="de548-138">If your filter has a custom allocator, override the following methods, depending on which pin uses the allocator:</span></span>

-   <span data-ttu-id="de548-139">Eingabepin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) und [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span><span class="sxs-lookup"><span data-stu-id="de548-139">Input pin: [**CBaseInputPin::GetAllocator**](cbaseinputpin-getallocator.md) and [**CBaseInputPin::NotifyAllocator**](cbaseinputpin-notifyallocator.md).</span></span>
-   <span data-ttu-id="de548-140">Ausgabepin: [**CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="de548-140">Output pin: [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="de548-141">Wenn der andere Filter die Verbindung mit der benutzerdefinierten Zuweisung verweigert, kann der Filter entweder die Verbindung fehlschlagen oder eine Verbindung mit der Zuweisung des anderen Filters herstellen.</span><span class="sxs-lookup"><span data-stu-id="de548-141">If the other filter refuses to connect using your custom allocator, your filter can either fail the connection, or else connect with the other filter's allocator.</span></span> <span data-ttu-id="de548-142">Im letzteren Fall müssen Sie möglicherweise ein internes Flag festlegen, das den Typ der Zuweisung angibt.</span><span class="sxs-lookup"><span data-stu-id="de548-142">In the latter case, you might need to set an internal flag indicating the type of allocator.</span></span> <span data-ttu-id="de548-143">Ein Beispiel für diesen Ansatz finden Sie unter [**CDrawImage-Klasse.**](cdrawimage.md)</span><span class="sxs-lookup"><span data-stu-id="de548-143">For an example of this approach, see [**CDrawImage Class**](cdrawimage.md).</span></span>

<span data-ttu-id="de548-144">Weiter: [Schritt 5. Transformieren Sie das Image](step-5--transform-the-image.md).</span><span class="sxs-lookup"><span data-stu-id="de548-144">Next: [Step 5. Transform the Image](step-5--transform-the-image.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="de548-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="de548-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de548-146">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="de548-146">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



