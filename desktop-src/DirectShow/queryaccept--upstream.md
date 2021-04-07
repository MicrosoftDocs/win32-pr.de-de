---
description: Queryaccept (Upstream)
ms.assetid: 3153e3a4-2227-4fdd-b2b0-218763013d2d
title: Queryaccept (Upstream)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7707c52d36c3d065c4a7277939f724aabdb73e46
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747096"
---
# <a name="queryaccept-upstream"></a><span data-ttu-id="129c3-103">Queryaccept (Upstream)</span><span class="sxs-lookup"><span data-stu-id="129c3-103">QueryAccept (Upstream)</span></span>

<span data-ttu-id="129c3-104">Dieser Mechanismus ermöglicht es einer Eingabe-PIN, eine Formatänderung an Ihren upstreampeer vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="129c3-104">This mechanism enables an input pin to propose a format change to its upstream peer.</span></span> <span data-ttu-id="129c3-105">Der downstreamfilter muss einen Medientyp an das Beispiel anfügen, den der Upstream-Filter beim nächsten Aufrufen von [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)erhält.</span><span class="sxs-lookup"><span data-stu-id="129c3-105">The downstream filter must attach a media type to the sample that the upstream filter will obtain in its next call to [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).</span></span> <span data-ttu-id="129c3-106">Zu diesem Zweck muss der Downstream-Filter jedoch eine benutzerdefinierte Zuweisung für die Verbindung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="129c3-106">In order to do this, however, the downstream filter must provide a custom allocator for the connection.</span></span> <span data-ttu-id="129c3-107">Diese Zuweisung muss eine private Methode implementieren, mit der der Downstream-Filter den Medientyp im nächsten Beispiel festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="129c3-107">This allocator must implement a private method that the downstream filter can use to set the media type on the next sample.</span></span>

<span data-ttu-id="129c3-108">Dabei werden die folgenden Schritte ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="129c3-108">The following steps occur:</span></span>

1.  <span data-ttu-id="129c3-109">Der Downstream-Filter überprüft, ob die PIN-Verbindung die benutzerdefinierte Zuweisung des Filters verwendet.</span><span class="sxs-lookup"><span data-stu-id="129c3-109">The downstream filter checks whether the pin connection uses the filter's custom allocator.</span></span> <span data-ttu-id="129c3-110">Wenn der upstreamfilter die Zuweisung besitzt, kann der Downstream-Filter das Format nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="129c3-110">If the upstream filter owns the allocator, the downstream filter cannot change the format.</span></span>
2.  <span data-ttu-id="129c3-111">Der Downstream-Filter ruft [**IPin:: queryaccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) für die upstreamausgabepin auf (siehe Abbildung, Schritt A).</span><span class="sxs-lookup"><span data-stu-id="129c3-111">The downstream filter calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream output pin (see illustration, step A).</span></span>
3.  <span data-ttu-id="129c3-112">Wenn `QueryAccept` S OK zurückgibt \_ , ruft der Downstream-Filter die private-Methode für seine Zuweisung auf, um den Medientyp festzulegen.</span><span class="sxs-lookup"><span data-stu-id="129c3-112">If `QueryAccept` returns S\_OK, the downstream filter calls the private method on its allocator in order to set the media type.</span></span> <span data-ttu-id="129c3-113">Innerhalb dieser privaten Methode ruft die Zuweisung [**imediasample:: setmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) beim nächsten verfügbaren Beispiel (B) auf.</span><span class="sxs-lookup"><span data-stu-id="129c3-113">Within this private method, the allocator calls [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) on the next available sample (B).</span></span>
4.  <span data-ttu-id="129c3-114">Der upstreamfilter ruft **GetBuffer** auf, um ein neues Beispiel (C) und [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) zum erhalten des Medientyps (D) zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="129c3-114">The upstream filter calls **GetBuffer** to get a new sample (C) and [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) to get the media type (D).</span></span>
5.  <span data-ttu-id="129c3-115">Wenn der upstreamfilter das Beispiel liefert, sollte der Medientyp an dieses Beispiel angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="129c3-115">When the upstream filter delivers the sample, it should leave the media type attached to that sample.</span></span> <span data-ttu-id="129c3-116">Auf diese Weise kann der Downstream-Filter bestätigen, dass sich der Medientyp geändert hat (E).</span><span class="sxs-lookup"><span data-stu-id="129c3-116">That way, the downstream filter can confirm that the media type has changed (E).</span></span>

<span data-ttu-id="129c3-117">Wenn der upstreamfilter die Formatänderung annimmt, muss er auch in der Lage sein, zurück zum ursprünglichen Medientyp zu wechseln, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="129c3-117">If the upstream filter accepts the format change, it must also be able to switch back to the original media type, as shown in the following diagram.</span></span>

![queryaccept (Upstream)](images/dynformat4.png)

<span data-ttu-id="129c3-119">Die wichtigsten Beispiele für diese Art von Formatänderung betreffen die DirectShow-Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="129c3-119">The main examples of this kind of format change involve the DirectShow video renderers.</span></span>

-   <span data-ttu-id="129c3-120">Der ursprüngliche [Videorendererfilter](video-renderer-filter.md) kann während des Streamings zwischen RGB-und YUV-Typen wechseln.</span><span class="sxs-lookup"><span data-stu-id="129c3-120">The original [Video Renderer](video-renderer-filter.md) filter can switch between RGB and YUV types during streaming.</span></span> <span data-ttu-id="129c3-121">Wenn der Filter eine Verbindung herstellt, ist ein RGB-Format erforderlich, das den aktuellen Anzeigeeinstellungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="129c3-121">When the filter connects, it requires an RGB format that matches the current display settings.</span></span> <span data-ttu-id="129c3-122">Dadurch wird sichergestellt, dass GDI auf GDI zurückgegriffen werden kann, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="129c3-122">This guarantees that it can fall back on GDI if it needs to.</span></span> <span data-ttu-id="129c3-123">Nachdem das Streaming begonnen hat, fordert der Videorenderer eine Formatänderung an einen YUV-Typ an, wenn DirectDraw verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="129c3-123">After streaming begins, if DirectDraw is available, the Video Renderer requests a format change to a YUV type.</span></span> <span data-ttu-id="129c3-124">Zu einem späteren Zeitpunkt wechselt Sie möglicherweise zurück zu RGB, wenn die DirectDraw-Oberfläche aus irgendeinem Grund verloren geht.</span><span class="sxs-lookup"><span data-stu-id="129c3-124">Later, it might switch back to RGB if it loses the DirectDraw surface for any reason.</span></span>
-   <span data-ttu-id="129c3-125">Der neuere Filter für Video Mischungs Renderer (VMR) stellt eine Verbindung mit einem beliebigen Format her, das von der Grafikhardware unterstützt wird, einschließlich YUV-Typen.</span><span class="sxs-lookup"><span data-stu-id="129c3-125">The newer Video Mixing Renderer (VMR) filter will connect with any format that is supported by the graphics hardware, including YUV types.</span></span> <span data-ttu-id="129c3-126">Allerdings kann die Grafikhardware den Schritt der zugrunde liegenden DirectDraw-Oberfläche ändern, um die Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="129c3-126">However, the graphics hardware might change the stride of the underlying DirectDraw surface in order to optimize performance.</span></span> <span data-ttu-id="129c3-127">Der VMR-Filter verwendet, `QueryAccept` um den neuen Stride zu melden, der im **biwidth** -Member der **BITMAPINFOHEADER** -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="129c3-127">The VMR filter uses `QueryAccept` to report the new stride, which is specified in the **biWidth** member of the **BITMAPINFOHEADER** structure.</span></span> <span data-ttu-id="129c3-128">Die Quell-und Ziel Rechtecke in der **videoinfoheader** -oder **VIDEOINFOHEADER2** -Struktur identifizieren die Region, in der das Video decodiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="129c3-128">The source and target rectangles in the **VIDEOINFOHEADER** or **VIDEOINFOHEADER2** structure identify the region where the video should be decoded.</span></span>

<span data-ttu-id="129c3-129">**Implementierungs Hinweis**</span><span class="sxs-lookup"><span data-stu-id="129c3-129">**Implementation Note**</span></span>

<span data-ttu-id="129c3-130">Es ist unwahrscheinlich, dass Sie einen Filter schreiben, bei dem upstreamformatänderungen angefordert werden müssen, da dies hauptsächlich eine Funktion von Videorenderer ist.</span><span class="sxs-lookup"><span data-stu-id="129c3-130">It is unlikely that you will write a filter that needs to request upstream format changes, since this is mainly a feature of video renderers.</span></span> <span data-ttu-id="129c3-131">Wenn Sie jedoch einen Video Transformations Filter oder einen Video Decoder schreiben, muss der Filter ordnungsgemäß auf Anforderungen vom Videorenderer Antworten.</span><span class="sxs-lookup"><span data-stu-id="129c3-131">However, if you write a video transform filter or a video decoder, your filter must respond correctly to requests from the video renderer.</span></span>

<span data-ttu-id="129c3-132">Ein direkter Filter, der zwischen dem Videorenderer und dem Decoder liegt, sollte alle `QueryAccept` Aufrufe mit Upstream bestehen.</span><span class="sxs-lookup"><span data-stu-id="129c3-132">A trans-in-place filter that sits between the video renderer and the decoder should pass all `QueryAccept` calls upstream.</span></span> <span data-ttu-id="129c3-133">Speichern Sie die neuen Formatierungsinformationen, wenn Sie ankommen.</span><span class="sxs-lookup"><span data-stu-id="129c3-133">Store the new format information when it arrives.</span></span>

<span data-ttu-id="129c3-134">Ein Kopier-und Transformations Filter (d. h. ein nicht-transdirekter Filter) sollte eines der folgenden Verhaltensweisen implementieren:</span><span class="sxs-lookup"><span data-stu-id="129c3-134">A copy-transform filter (that is, a non-trans-in-place filter) should implement one of the following behaviors:</span></span>

-   <span data-ttu-id="129c3-135">Übergeben Sie die Formatänderungen Upstream, und speichern Sie die neuen Formatierungsinformationen, wenn Sie ankommen.</span><span class="sxs-lookup"><span data-stu-id="129c3-135">Pass format changes upstream and store the new format information when it arrives.</span></span> <span data-ttu-id="129c3-136">Der Filter muss eine benutzerdefinierte Zuweisung verwenden, damit er das Format an das upstreambeispiel anfügen kann.</span><span class="sxs-lookup"><span data-stu-id="129c3-136">Your filter must use a custom allocator so that it can attach the format to the upstream sample.</span></span>
-   <span data-ttu-id="129c3-137">Führen Sie die Formatkonvertierung innerhalb des Filters aus.</span><span class="sxs-lookup"><span data-stu-id="129c3-137">Perform the format conversion inside the filter.</span></span> <span data-ttu-id="129c3-138">Dies ist wahrscheinlich einfacher als das übertragen der Format Änderungs upstreamdatei.</span><span class="sxs-lookup"><span data-stu-id="129c3-138">This is probably easier than passing the format change upstream.</span></span> <span data-ttu-id="129c3-139">Möglicherweise ist Sie jedoch weniger effizient als das Decodieren des Decoders in das richtige Format.</span><span class="sxs-lookup"><span data-stu-id="129c3-139">However, it might be less efficient than letting the decoder filter decode into the correct format.</span></span>
-   <span data-ttu-id="129c3-140">Als letztes Mittel sollten Sie die Formatänderung einfach ablehnen.</span><span class="sxs-lookup"><span data-stu-id="129c3-140">As a last resort, simply reject the format change.</span></span> <span data-ttu-id="129c3-141">(Weitere Informationen finden Sie im Quellcode für die [**ctransinplaceoutputpin:: checkmediatype**](ctransinplaceoutputpin-checkmediatype.md) -Methode in der DirectShow-Basisklassen Bibliothek.) Das Ablehnen einer Formatänderung kann jedoch die Leistung beeinträchtigen, da der Videorenderer verhindert, dass das effizienteste Format verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="129c3-141">(For more information, refer to the source code for the [**CTransInPlaceOutputPin::CheckMediaType**](ctransinplaceoutputpin-checkmediatype.md) method in the DirectShow base class library.) Rejecting a format change can reduce performance, however, because it prevents the video renderer from using the most efficient format.</span></span>

<span data-ttu-id="129c3-142">Der folgende Pseudo Code zeigt, wie Sie einen von **ctransformfilter** abgeleiteten Kopier-und Transformations Filter implementieren können, der zwischen YUV-und RGB-Ausgabetypen wechseln kann.</span><span class="sxs-lookup"><span data-stu-id="129c3-142">The following pseudo-code shows how you might implement a copy-transform filter (derived from **CTransformFilter**) that can switch between YUV and RGB output types.</span></span> <span data-ttu-id="129c3-143">In diesem Beispiel wird davon ausgegangen, dass der Filter die Konvertierung selbst durchführt, anstatt die Formatänderung Upstream zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="129c3-143">This example assumes that the filter does the conversion itself, rather than passing the format change upstream.</span></span>


```C++
HRESULT CMyTransform::CheckInputType(const CMediaType *pmt)
{
    if (pmt is a YUV type that you support) {
        return S_OK;
    }
    else {
        return VFW_E_TYPE_NOT_ACCEPTED;
    }
}

HRESULT CMyTransform::CheckTransform(
    const CMediaType *mtIn, const CMediaType *mtOut)
{
    if (mtOut is a YUV or RGB type that you support)
    {
        if ((mtIn has the same video dimensions as mtOut) &&
            (you support the mtIn-to-mtOut transform))
        {
            return S_OK;
        }
    }
    // otherwise
    return VFW_E_TYPE_NOT_ACCEPTED;
}

// GetMediaType: Return a preferred output type.
HRESULT CMyTransform::GetMediaType(int iPosition, CMediaType *pMediaType)
{
    if (iPosition < 0) {
        return E_INVALIDARG;
    }
    switch (iPosition)
    {
    case 0:
        Copy the input type (YUV) to pMediaType
        return S_OK;
    case 1:
        Construct an RGB type that matches the input type.
        return S_OK;
    default:
        return VFW_S_NO_MORE_ITEMS;
    }
}

// SetMediaType: Override from CTransformFilter. 
HRESULT CMyTransform::SetMediaType(
    PIN_DIRECTION direction, const CMediaType *pmt)
{
    // Capture this information...
    if (direction == PINDIR_OUTPUT)
    {
       m_bYuv = (pmt->subtype == MEDIASUBTYPE_UYVY);
    }
    return S_OK;
}

HRESULT CMyTransform::Transform(
    IMediaSample *pSource, IMediaSample *pDest)
{
    // Look for format changes from downstream.
    CMediaType *pMT = NULL;
    HRESULT hr = pDest->GetMediaType((AM_MEDIA_TYPE**)&pMT);
    if (hr == S_OK)
    {
        hr = m_pOutput->CheckMediaType(pMT);
        if(FAILED(hr))
        {
            DeleteMediaType(pMT);
            return E_FAIL;
        }
        // Notify our own output pin about the new type.
        m_pOutput->SetMediaType(pMT);
        DeleteMediaType(pMT);
    }
    // Process the buffers
    if (m_bYuv) {
        return ProcessFrameYUV(pSource, pDest);
    }
    else {
        return ProcessFrameRGB(pSource, pDest);
    }
}
```



 

 



