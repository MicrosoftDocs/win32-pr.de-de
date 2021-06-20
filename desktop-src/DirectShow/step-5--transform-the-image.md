---
description: Verwenden Sie dieses Beispiel, um zu verstehen, wie der RLE-Encoder die -Methode beim Schreiben eines Transformationsfilters implementieren kann.
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: 'Schritt 5: Transformieren des Bilds'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac9d32e48ba438f8bde2d8d4d9aca3b827ebc0c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406783"
---
# <a name="step-5-transform-the-image"></a><span data-ttu-id="89c82-104">Schritt 5:</span><span class="sxs-lookup"><span data-stu-id="89c82-104">Step 5.</span></span> <span data-ttu-id="89c82-105">Transformieren des Bilds</span><span class="sxs-lookup"><span data-stu-id="89c82-105">Transform the Image</span></span>

<span data-ttu-id="89c82-106">Dies ist Schritt 5 des Tutorials Schreiben von [Transformationsfiltern.](writing-transform-filters.md)</span><span class="sxs-lookup"><span data-stu-id="89c82-106">This is step 5 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="89c82-107">Der Upstreamfilter übermittelt Medienbeispiele an den Transformationsfilter, indem er die [**IMemInputPin::Receive-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) auf dem Eingabepin des Transformationsfilters aufruft.</span><span class="sxs-lookup"><span data-stu-id="89c82-107">The upstream filter delivers media samples to the transform filter by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the transform filter's input pin.</span></span> <span data-ttu-id="89c82-108">Um die Daten zu verarbeiten, ruft der Transformationsfilter die **Transformationsmethode auf,** die rein virtuell ist.</span><span class="sxs-lookup"><span data-stu-id="89c82-108">To process the data, the transform filter calls the **Transform** method, which is pure virtual.</span></span> <span data-ttu-id="89c82-109">Die Klassen **CTransformFilter** und **CTransInPlaceFilter** verwenden zwei verschiedene Versionen dieser Methode:</span><span class="sxs-lookup"><span data-stu-id="89c82-109">The **CTransformFilter** and **CTransInPlaceFilter** classes use two different versions of this method:</span></span>

-   <span data-ttu-id="89c82-110">[**CTransformFilter::Transform**](ctransformfilter-transform.md) verwendet einen Zeiger auf das Eingabebeispiel und einen Zeiger auf das Ausgabebeispiel.</span><span class="sxs-lookup"><span data-stu-id="89c82-110">[**CTransformFilter::Transform**](ctransformfilter-transform.md) takes a pointer to the input sample and a pointer to the output sample.</span></span> <span data-ttu-id="89c82-111">Bevor der Filter die -Methode aufruft, kopiert er die Beispieleigenschaften aus dem Eingabebeispiel in das Ausgabebeispiel, einschließlich der Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="89c82-111">Before the filter calls the method, it copies the sample properties from the input sample to the output sample, including the time stamps.</span></span>
-   <span data-ttu-id="89c82-112">[**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) verwendet einen Zeiger auf das Eingabebeispiel.</span><span class="sxs-lookup"><span data-stu-id="89c82-112">[**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) takes a pointer to the input sample.</span></span> <span data-ttu-id="89c82-113">Der Filter ändert die daten vor Ort.</span><span class="sxs-lookup"><span data-stu-id="89c82-113">The filter modifies the data in place.</span></span>

<span data-ttu-id="89c82-114">Wenn die **Transform-Methode** S \_ OK zurückgibt, übermittelt der Filter das Beispiel downstream.</span><span class="sxs-lookup"><span data-stu-id="89c82-114">If the **Transform** method returns S\_OK, the filter delivers the sample downstream.</span></span> <span data-ttu-id="89c82-115">Um einen Frame zu überspringen, geben Sie S \_ FALSE zurück.</span><span class="sxs-lookup"><span data-stu-id="89c82-115">To skip a frame, return S\_FALSE.</span></span> <span data-ttu-id="89c82-116">Wenn ein Streamingfehler auftritt, geben Sie einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="89c82-116">If there is a streaming error, return a failure code.</span></span>

<span data-ttu-id="89c82-117">Das folgende Beispiel zeigt, wie der RLE-Encoder diese Methode implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="89c82-117">The following example shows how the RLE encoder might implement this method.</span></span> <span data-ttu-id="89c82-118">Ihre eigene Implementierung kann sich je nach Filter erheblich unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="89c82-118">Your own implementation might differ considerably, depending on what your filter does.</span></span>


```C++
HRESULT CRleFilter::Transform(IMediaSample *pSource, IMediaSample *pDest)
{
    // Get pointers to the underlying buffers.
    BYTE *pBufferIn, *pBufferOut;
    hr = pSource->GetPointer(&pBufferIn);
    if (FAILED(hr))
    {
        return hr;
    }
    hr = pDest->GetPointer(&pBufferOut);
    if (FAILED(hr))
    {
        return hr;
    }
    // Process the data.
    DWORD cbDest = EncodeFrame(pBufferIn, pBufferOut);
    KASSERT((long)cbDest <= pDest->GetSize());

    pDest->SetActualDataLength(cbDest);
    pDest->SetSyncPoint(TRUE);
    return S_OK;
}
```



<span data-ttu-id="89c82-119">In diesem Beispiel wird davon ausgegangen, dass EncodeFrame eine private Methode ist, die die RLE-Codierung implementiert.</span><span class="sxs-lookup"><span data-stu-id="89c82-119">This example assumes that EncodeFrame is a private method that implements the RLE encoding.</span></span> <span data-ttu-id="89c82-120">Der Codierungsalgorithmus selbst wird hier nicht beschrieben. Weitere Informationen finden Sie im Thema "Bitmapkomprimierung" in der Plattform-SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="89c82-120">The encoding algorithm itself is not described here; for details, see the topic "Bitmap Compression" in the Platform SDK documentation.</span></span>

<span data-ttu-id="89c82-121">Zunächst ruft das Beispiel [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) auf, um die Adressen der zugrunde liegenden Puffer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="89c82-121">First, the example calls [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) to retrieve the addresses of the underlying buffers.</span></span> <span data-ttu-id="89c82-122">Diese werden an die private EncoderFrame-Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="89c82-122">It passes these to the private EncoderFrame method.</span></span> <span data-ttu-id="89c82-123">Anschließend ruft sie [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) auf, um die Länge der codierten Daten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="89c82-123">Then it calls [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) to specify the length of the encoded data.</span></span> <span data-ttu-id="89c82-124">Der Downstreamfilter benötigt diese Informationen, damit er den Puffer ordnungsgemäß verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="89c82-124">The downstream filter needs this information so that it can manage the buffer properly.</span></span> <span data-ttu-id="89c82-125">Schließlich ruft die -Methode [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) auf, um das Keyframeflag auf **TRUE** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="89c82-125">Finally, the method calls [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) to set the key frame flag to **TRUE**.</span></span> <span data-ttu-id="89c82-126">Bei der Codierung der Ausführungslänge werden keine Deltaframes verwendet, sodass jeder Frame ein Keyframe ist.</span><span class="sxs-lookup"><span data-stu-id="89c82-126">Run-length encoding does not use any delta frames, so every frame is a key frame.</span></span> <span data-ttu-id="89c82-127">Legen Sie für Deltaframes den Wert auf **FALSE** fest.</span><span class="sxs-lookup"><span data-stu-id="89c82-127">For delta frames, set the value to **FALSE**.</span></span>

<span data-ttu-id="89c82-128">Weitere Aspekte, die Sie berücksichtigen müssen, sind:</span><span class="sxs-lookup"><span data-stu-id="89c82-128">Other issues that you must consider include:</span></span>

-   <span data-ttu-id="89c82-129">Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="89c82-129">Time stamps.</span></span> <span data-ttu-id="89c82-130">Die **CTransformFilter-Klasse** zeitstempelt das Ausgabebeispiel, bevor die **Transform-Methode** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="89c82-130">The **CTransformFilter** class timestamps the output sample before calling the **Transform** method.</span></span> <span data-ttu-id="89c82-131">Die Zeitstempelwerte werden aus dem Eingabebeispiel kopiert, ohne sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="89c82-131">It copies the time stamp values from the input sample, without modifying them.</span></span> <span data-ttu-id="89c82-132">Wenn Ihr Filter die Zeitstempel ändern muss, rufen [**Sie IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) im Ausgabebeispiel auf.</span><span class="sxs-lookup"><span data-stu-id="89c82-132">If your filter needs to change the time stamps, call [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) on the output sample.</span></span>
-   <span data-ttu-id="89c82-133">Formatänderungen.</span><span class="sxs-lookup"><span data-stu-id="89c82-133">Format changes.</span></span> <span data-ttu-id="89c82-134">Der Upstreamfilter kann Formate während des Streams ändern, indem er einen Medientyp an das Beispiel anfügt.</span><span class="sxs-lookup"><span data-stu-id="89c82-134">The upstream filter can change formats mid-stream by attaching a media type to the sample.</span></span> <span data-ttu-id="89c82-135">Zuvor wird [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) auf dem Eingabepin Ihres Filters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="89c82-135">Before doing so, it calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on your filter's input pin.</span></span> <span data-ttu-id="89c82-136">In der **CTransformFilter-Klasse** führt dies zu einem Aufruf von **CheckInputType** gefolgt von **CheckTransform.**</span><span class="sxs-lookup"><span data-stu-id="89c82-136">In the **CTransformFilter** class, this results in a call to **CheckInputType** followed by **CheckTransform**.</span></span> <span data-ttu-id="89c82-137">Der Downstreamfilter kann auch Medientypen mit demselben Mechanismus ändern.</span><span class="sxs-lookup"><span data-stu-id="89c82-137">The downstream filter can also change media types, using the same mechanism.</span></span> <span data-ttu-id="89c82-138">In Ihrem eigenen Filter gibt es zwei Dinge zu beobachten:</span><span class="sxs-lookup"><span data-stu-id="89c82-138">In your own filter, there are two things to watch for:</span></span>

    -   <span data-ttu-id="89c82-139">Stellen Sie sicher, dass **QueryAccept** keine falschen Zustimmungen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="89c82-139">Make sure that **QueryAccept** does not return false acceptances.</span></span>
    -   <span data-ttu-id="89c82-140">Wenn Ihr Filter Formatänderungen akzeptiert, überprüfen Sie diese in der **Transform-Methode,** indem [**Sie IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="89c82-140">If your filter does accept format changes, check for them inside the **Transform** method by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="89c82-141">Wenn diese Methode S \_ OK zurückgibt, muss Ihr Filter auf die Formatänderung reagieren.</span><span class="sxs-lookup"><span data-stu-id="89c82-141">If that method returns S\_OK, your filter must respond to the format change.</span></span>

    <span data-ttu-id="89c82-142">Weitere Informationen finden Sie unter [Dynamische Formatänderungen.](dynamic-format-changes.md)</span><span class="sxs-lookup"><span data-stu-id="89c82-142">For more information, see [Dynamic Format Changes](dynamic-format-changes.md).</span></span>

-   <span data-ttu-id="89c82-143">Threads.</span><span class="sxs-lookup"><span data-stu-id="89c82-143">Threads.</span></span> <span data-ttu-id="89c82-144">Sowohl in **CTransformFilter** als **auch in CTransInPlaceFilter** liefert der Transformationsfilter Ausgabebeispiele synchron innerhalb der **Receive-Methode.**</span><span class="sxs-lookup"><span data-stu-id="89c82-144">In both **CTransformFilter** and **CTransInPlaceFilter**, the transform filter delivers output samples synchronously inside the **Receive** method.</span></span> <span data-ttu-id="89c82-145">Der Filter erstellt keine Arbeitsthreads zum Verarbeiten der Daten.</span><span class="sxs-lookup"><span data-stu-id="89c82-145">The filter does not create any worker threads to process the data.</span></span> <span data-ttu-id="89c82-146">In der Regel gibt es keinen Grund für einen Transformationsfilter zum Erstellen von Arbeitsthreads.</span><span class="sxs-lookup"><span data-stu-id="89c82-146">Typically, there is no reason for a transform filter to create worker threads.</span></span>

<span data-ttu-id="89c82-147">Weiter: [Schritt 6. Unterstützung für COM hinzugefügt.](step-6--add-support-for-com.md)</span><span class="sxs-lookup"><span data-stu-id="89c82-147">Next: [Step 6. Add Support for COM](step-6--add-support-for-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89c82-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="89c82-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89c82-149">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="89c82-149">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



