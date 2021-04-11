---
description: 'Schritt 5:'
ms.assetid: b7d878ab-523f-4b52-b98d-c9d4fa18ce8a
title: 'Schritt 5: Transformieren des Bilds'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609acb626d00dbceea8b6f5bca6af012d8158b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217480"
---
# <a name="step-5-transform-the-image"></a><span data-ttu-id="63795-104">Schritt 5:</span><span class="sxs-lookup"><span data-stu-id="63795-104">Step 5.</span></span> <span data-ttu-id="63795-105">Transformieren des Bilds</span><span class="sxs-lookup"><span data-stu-id="63795-105">Transform the Image</span></span>

<span data-ttu-id="63795-106">Dies ist Schritt 5 des Tutorials zum [Schreiben von Transformations Filtern](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="63795-106">This is step 5 of the tutorial [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="63795-107">Der upstreamfilter liefert Medien Beispiele für den Transformations Filter, indem die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode für die Eingabe-PIN des Transformations Filters aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="63795-107">The upstream filter delivers media samples to the transform filter by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the transform filter's input pin.</span></span> <span data-ttu-id="63795-108">Um die Daten zu verarbeiten, ruft der Transformations Filter die **transformier** Methode auf, die rein virtuell ist.</span><span class="sxs-lookup"><span data-stu-id="63795-108">To process the data, the transform filter calls the **Transform** method, which is pure virtual.</span></span> <span data-ttu-id="63795-109">Die **ctransformfilter** -Klasse und die **ctransinplacefilter** -Klasse verwenden zwei unterschiedliche Versionen dieser Methode:</span><span class="sxs-lookup"><span data-stu-id="63795-109">The **CTransformFilter** and **CTransInPlaceFilter** classes use two different versions of this method:</span></span>

-   <span data-ttu-id="63795-110">[**Ctransformfilter:: Transform**](ctransformfilter-transform.md) übernimmt einen Zeiger auf das Eingabe Beispiel und einen Zeiger auf das Ausgabe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="63795-110">[**CTransformFilter::Transform**](ctransformfilter-transform.md) takes a pointer to the input sample and a pointer to the output sample.</span></span> <span data-ttu-id="63795-111">Bevor der Filter die-Methode aufruft, werden die Beispiel Eigenschaften aus dem Eingabe Beispiel in das Ausgabe Beispiel kopiert, einschließlich der Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="63795-111">Before the filter calls the method, it copies the sample properties from the input sample to the output sample, including the time stamps.</span></span>
-   <span data-ttu-id="63795-112">[**Ctransinplacefilter:: Transform**](ctransinplacefilter-transform.md) nimmt einen Zeiger auf das Eingabe Beispiel an.</span><span class="sxs-lookup"><span data-stu-id="63795-112">[**CTransInPlaceFilter::Transform**](ctransinplacefilter-transform.md) takes a pointer to the input sample.</span></span> <span data-ttu-id="63795-113">Der Filter ändert die Daten an Ort und Stelle.</span><span class="sxs-lookup"><span data-stu-id="63795-113">The filter modifies the data in place.</span></span>

<span data-ttu-id="63795-114">Wenn die **Transform** -Methode "S OK" zurückgibt, übermittelt \_ der Filter das Beispiel nach unten.</span><span class="sxs-lookup"><span data-stu-id="63795-114">If the **Transform** method returns S\_OK, the filter delivers the sample downstream.</span></span> <span data-ttu-id="63795-115">Um einen Frame zu überspringen, geben Sie "false" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="63795-115">To skip a frame, return S\_FALSE.</span></span> <span data-ttu-id="63795-116">Wenn ein Streamingfehler vorliegt, wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="63795-116">If there is a streaming error, return a failure code.</span></span>

<span data-ttu-id="63795-117">Das folgende Beispiel zeigt, wie der RLE-Encoder diese Methode implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="63795-117">The following example shows how the RLE encoder might implement this method.</span></span> <span data-ttu-id="63795-118">Abhängig von der Art Ihres Filters kann sich Ihre eigene Implementierung erheblich unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="63795-118">Your own implementation might differ considerably, depending on what your filter does.</span></span>


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



<span data-ttu-id="63795-119">In diesem Beispiel wird davon ausgegangen, dass encodeframe eine private Methode ist, die die RLE-Codierung implementiert.</span><span class="sxs-lookup"><span data-stu-id="63795-119">This example assumes that EncodeFrame is a private method that implements the RLE encoding.</span></span> <span data-ttu-id="63795-120">Der Codierungs Algorithmus selbst wird hier nicht beschrieben. Weitere Informationen finden Sie im Thema "Bitmapkomprimierung" in der Platform SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="63795-120">The encoding algorithm itself is not described here; for details, see the topic "Bitmap Compression" in the Platform SDK documentation.</span></span>

<span data-ttu-id="63795-121">Zunächst wird im Beispiel [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) aufgerufen, um die Adressen der zugrunde liegenden Puffer abzurufen.</span><span class="sxs-lookup"><span data-stu-id="63795-121">First, the example calls [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) to retrieve the addresses of the underlying buffers.</span></span> <span data-ttu-id="63795-122">Sie übergibt diese an die private encoderframe-Methode.</span><span class="sxs-lookup"><span data-stu-id="63795-122">It passes these to the private EncoderFrame method.</span></span> <span data-ttu-id="63795-123">Anschließend wird [**imediasample:: setactualdatalength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) aufgerufen, um die Länge der codierten Daten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="63795-123">Then it calls [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) to specify the length of the encoded data.</span></span> <span data-ttu-id="63795-124">Der Downstream-Filter benötigt diese Informationen, damit der Puffer ordnungsgemäß verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="63795-124">The downstream filter needs this information so that it can manage the buffer properly.</span></span> <span data-ttu-id="63795-125">Schließlich ruft die-Methode [**imediasample:: setsyncpoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) auf, um das schlüsselframe-Flag auf " **true**" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="63795-125">Finally, the method calls [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) to set the key frame flag to **TRUE**.</span></span> <span data-ttu-id="63795-126">Bei der Codierung der Lauf Zeit Länge werden keine Delta Frames verwendet, sodass jeder Frame ein Keyframe ist.</span><span class="sxs-lookup"><span data-stu-id="63795-126">Run-length encoding does not use any delta frames, so every frame is a key frame.</span></span> <span data-ttu-id="63795-127">Legen Sie für Delta Frames den Wert auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="63795-127">For delta frames, set the value to **FALSE**.</span></span>

<span data-ttu-id="63795-128">Weitere Aspekte, die Sie berücksichtigen müssen, sind:</span><span class="sxs-lookup"><span data-stu-id="63795-128">Other issues that you must consider include:</span></span>

-   <span data-ttu-id="63795-129">Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="63795-129">Time stamps.</span></span> <span data-ttu-id="63795-130">Die **ctransformfilter** -Klasse Zeitstempel das Ausgabe Beispiel vor dem Aufruf der **Transform** -Methode.</span><span class="sxs-lookup"><span data-stu-id="63795-130">The **CTransformFilter** class timestamps the output sample before calling the **Transform** method.</span></span> <span data-ttu-id="63795-131">Die Zeitstempel Werte werden aus dem Eingabe Beispiel kopiert, ohne Sie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="63795-131">It copies the time stamp values from the input sample, without modifying them.</span></span> <span data-ttu-id="63795-132">Wenn der Filter die Zeitstempel ändern muss, nennen Sie [**imediasample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) im Ausgabe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="63795-132">If your filter needs to change the time stamps, call [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) on the output sample.</span></span>
-   <span data-ttu-id="63795-133">Formatieren von Änderungen.</span><span class="sxs-lookup"><span data-stu-id="63795-133">Format changes.</span></span> <span data-ttu-id="63795-134">Der upstreamfilter kann die Formate in der Mitte des Datenstroms ändern, indem er dem Beispiel einen Medientyp anfügt.</span><span class="sxs-lookup"><span data-stu-id="63795-134">The upstream filter can change formats mid-stream by attaching a media type to the sample.</span></span> <span data-ttu-id="63795-135">Vor diesem Vorgang wird [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) in der Eingabe-PIN Ihres Filters aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="63795-135">Before doing so, it calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on your filter's input pin.</span></span> <span data-ttu-id="63795-136">In der **ctransformfilter** -Klasse führt dies zu einem Rückruf von **checkinputtype** , gefolgt von **checktransform**.</span><span class="sxs-lookup"><span data-stu-id="63795-136">In the **CTransformFilter** class, this results in a call to **CheckInputType** followed by **CheckTransform**.</span></span> <span data-ttu-id="63795-137">Der downstreamfilter kann auch die Medientypen mithilfe desselben Mechanismus ändern.</span><span class="sxs-lookup"><span data-stu-id="63795-137">The downstream filter can also change media types, using the same mechanism.</span></span> <span data-ttu-id="63795-138">In Ihrem eigenen Filter müssen Sie zwei Dinge beachten:</span><span class="sxs-lookup"><span data-stu-id="63795-138">In your own filter, there are two things to watch for:</span></span>

    -   <span data-ttu-id="63795-139">Stellen Sie sicher, dass **queryaccept** keine falschen Annahmen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="63795-139">Make sure that **QueryAccept** does not return false acceptances.</span></span>
    -   <span data-ttu-id="63795-140">Wenn der Filter Formatänderungen annimmt, überprüfen Sie diese in der **Transformations** Methode, indem Sie [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="63795-140">If your filter does accept format changes, check for them inside the **Transform** method by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="63795-141">Wenn diese Methode S OK zurückgibt \_ , muss der Filter auf die Formatänderung reagieren.</span><span class="sxs-lookup"><span data-stu-id="63795-141">If that method returns S\_OK, your filter must respond to the format change.</span></span>

    <span data-ttu-id="63795-142">Weitere Informationen finden Sie unter [dynamische Format Änderungen](dynamic-format-changes.md).</span><span class="sxs-lookup"><span data-stu-id="63795-142">For more information, see [Dynamic Format Changes](dynamic-format-changes.md).</span></span>

-   <span data-ttu-id="63795-143">Threads.</span><span class="sxs-lookup"><span data-stu-id="63795-143">Threads.</span></span> <span data-ttu-id="63795-144">In **ctransformfilter** und **ctransinplacefilter** liefert der Transformations Filter Ausgabe Beispiele synchron innerhalb der **Receive** -Methode.</span><span class="sxs-lookup"><span data-stu-id="63795-144">In both **CTransformFilter** and **CTransInPlaceFilter**, the transform filter delivers output samples synchronously inside the **Receive** method.</span></span> <span data-ttu-id="63795-145">Der Filter erstellt keine Arbeitsthreads, um die Daten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="63795-145">The filter does not create any worker threads to process the data.</span></span> <span data-ttu-id="63795-146">In der Regel gibt es keinen Grund für einen Transformations Filter zum Erstellen von Arbeitsthreads.</span><span class="sxs-lookup"><span data-stu-id="63795-146">Typically, there is no reason for a transform filter to create worker threads.</span></span>

<span data-ttu-id="63795-147">Weiter: [Schritt 6. Unterstützung für com hinzufügen](step-6--add-support-for-com.md).</span><span class="sxs-lookup"><span data-stu-id="63795-147">Next: [Step 6. Add Support for COM](step-6--add-support-for-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="63795-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63795-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63795-149">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="63795-149">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



