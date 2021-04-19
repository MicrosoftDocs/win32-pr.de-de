---
description: Nicht komprimierte Video Puffer
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Nicht komprimierte Video Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345863"
---
# <a name="uncompressed-video-buffers"></a><span data-ttu-id="27cd7-103">Nicht komprimierte Video Puffer</span><span class="sxs-lookup"><span data-stu-id="27cd7-103">Uncompressed Video Buffers</span></span>

<span data-ttu-id="27cd7-104">In diesem Artikel wird beschrieben, wie Sie mit Medien Puffern arbeiten, die nicht komprimierte Video Frames enthalten.</span><span class="sxs-lookup"><span data-stu-id="27cd7-104">This article describes how to work with media buffers that contain uncompressed video frames.</span></span> <span data-ttu-id="27cd7-105">In der bevorzugten Reihenfolge sind die folgenden Optionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="27cd7-105">In order of preference, the following options are available.</span></span> <span data-ttu-id="27cd7-106">Nicht jeder Medien Puffer unterstützt die einzelnen Optionen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-106">Not every media buffer supports each option.</span></span>

1.  <span data-ttu-id="27cd7-107">Verwenden Sie die zugrunde liegende Direct3D-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="27cd7-107">Use the underlying Direct3D surface.</span></span> <span data-ttu-id="27cd7-108">(Gilt nur für Video Frames, die auf Direct3D-Oberflächen gespeichert sind.)</span><span class="sxs-lookup"><span data-stu-id="27cd7-108">(Applies only to video frames stored in Direct3D surfaces.)</span></span>
2.  <span data-ttu-id="27cd7-109">Verwenden Sie die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="27cd7-109">Use the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
3.  <span data-ttu-id="27cd7-110">Verwenden Sie die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="27cd7-110">Use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>

## <a name="use-the-underlying-direct3d-surface"></a><span data-ttu-id="27cd7-111">Zugrunde liegende Direct3D-Oberfläche verwenden</span><span class="sxs-lookup"><span data-stu-id="27cd7-111">Use the Underlying Direct3D Surface</span></span>

<span data-ttu-id="27cd7-112">Der Videoframe kann in einer Direct3D-Oberfläche gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="27cd7-112">The video frame might be stored inside a Direct3D surface.</span></span> <span data-ttu-id="27cd7-113">Wenn dies der Fall ist, können Sie einen Zeiger auf die-Oberfläche abrufen, indem Sie [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) oder [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) für das Medien Puffer Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-113">If so, you can get a pointer to the surface by calling [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) or [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) on the media buffer object.</span></span> <span data-ttu-id="27cd7-114">Verwenden Sie den Dienst Bezeichner Mr- \_ Puffer \_ Dienst.</span><span class="sxs-lookup"><span data-stu-id="27cd7-114">Use the service identifier MR\_BUFFER\_SERVICE.</span></span> <span data-ttu-id="27cd7-115">Diese Vorgehensweise wird empfohlen, wenn die Komponente, die auf den Videoframe zugreift, Direct3D verwendet.</span><span class="sxs-lookup"><span data-stu-id="27cd7-115">This approach is recommended when the component accessing the video frame is designed to use Direct3D.</span></span> <span data-ttu-id="27cd7-116">Beispielsweise sollte ein Video Decoder, der die DirectX-Videobeschleunigung unterstützt, diesen Ansatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="27cd7-116">For example, a video decoder that supports DirectX Video Acceleration should use this approach.</span></span>

<span data-ttu-id="27cd7-117">Der folgende Code zeigt, wie Sie den **IDirect3DSurface9** -Zeiger aus einem Medien Puffer erhalten.</span><span class="sxs-lookup"><span data-stu-id="27cd7-117">The following code shows how to get the **IDirect3DSurface9** pointer from a media buffer.</span></span>


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



<span data-ttu-id="27cd7-118">Die folgenden Objekte unterstützen den Dienst " **Mr- \_ Puffer \_ Dienst** ":</span><span class="sxs-lookup"><span data-stu-id="27cd7-118">The following objects support the **MR\_BUFFER\_SERVICE** service:</span></span>

-   [<span data-ttu-id="27cd7-119">DirectX-Oberflächen Puffer</span><span class="sxs-lookup"><span data-stu-id="27cd7-119">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)
-   [<span data-ttu-id="27cd7-120">Video Beispiele</span><span class="sxs-lookup"><span data-stu-id="27cd7-120">Video Samples</span></span>](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a><span data-ttu-id="27cd7-121">Verwenden der IMF2DBuffer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="27cd7-121">Use the IMF2DBuffer Interface</span></span>

<span data-ttu-id="27cd7-122">Wenn der Videorahmen nicht in einer Direct3D-Oberfläche gespeichert ist oder die Komponente nicht für die Verwendung von Direct3D konzipiert ist, wird als nächstes empfohlen, auf den Videoframe zuzugreifen, um den Puffer für die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle abzufragen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-122">If the video frame is not stored inside a Direct3D surface, or the component is not designed to use Direct3D, the next recommended way to access the video frame is to query the buffer for the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="27cd7-123">Diese Schnittstelle wurde speziell für Bilddaten entwickelt.</span><span class="sxs-lookup"><span data-stu-id="27cd7-123">This interface is designed specifically for image data.</span></span> <span data-ttu-id="27cd7-124">Um einen Zeiger auf diese Schnittstelle abzurufen, nennen Sie **QueryInterface** für den Medien Puffer.</span><span class="sxs-lookup"><span data-stu-id="27cd7-124">To get a pointer to this interface, call **QueryInterface** on the media buffer.</span></span> <span data-ttu-id="27cd7-125">Diese Schnittstelle wird nicht von allen Medien Puffer Objekten verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="27cd7-125">Not all media buffer objects expose this interface.</span></span> <span data-ttu-id="27cd7-126">Wenn ein Medien Puffer jedoch die **IMF2DBuffer** -Schnittstelle verfügbar macht, sollten Sie diese Schnittstelle verwenden, um möglichst auf die Daten zuzugreifen, anstatt [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="27cd7-126">But if a media buffer does expose the **IMF2DBuffer** interface, you should use that interface to access the data, if possible, rather than using [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer).</span></span> <span data-ttu-id="27cd7-127">Sie können weiterhin die **imfmediabuffer** -Schnittstelle verwenden, Sie ist jedoch möglicherweise weniger effizient.</span><span class="sxs-lookup"><span data-stu-id="27cd7-127">You can still use the **IMFMediaBuffer** interface, but it might be less efficient.</span></span>

1.  <span data-ttu-id="27cd7-128">Ruft **QueryInterface** für den Medien Puffer auf, um die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-128">Call **QueryInterface** on the media buffer to get the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>
2.  <span data-ttu-id="27cd7-129">Aufrufen von [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) , um auf den Arbeitsspeicher für den Puffer zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-129">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) to access the memory for the buffer.</span></span> <span data-ttu-id="27cd7-130">Diese Methode gibt einen Zeiger auf das erste Byte der obersten Zeile der Pixel zurück.</span><span class="sxs-lookup"><span data-stu-id="27cd7-130">This method returns a pointer to the first byte of the top row of pixels.</span></span> <span data-ttu-id="27cd7-131">Außerdem wird der Bild Sprung zurückgegeben, bei dem es sich um die Anzahl der Bytes vom Anfang einer Zeile bis zum Anfang der nächsten Zeile handelt.</span><span class="sxs-lookup"><span data-stu-id="27cd7-131">It also returns the image stride, which is the number of bytes from the start of a row of pixels to the start of the next row.</span></span> <span data-ttu-id="27cd7-132">Der Puffer kann nach jeder Zeile von Pixeln Auffüll Bytes enthalten, sodass der Stride breiter als die Bildbreite in Bytes sein kann.</span><span class="sxs-lookup"><span data-stu-id="27cd7-132">The buffer might contain padding bytes after each row of pixels, so the stride might be wider than the image width in bytes.</span></span> <span data-ttu-id="27cd7-133">Stride kann auch negativ sein, wenn das Bild im Arbeitsspeicher nach unten ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="27cd7-133">Stride can also be negative if the image is oriented bottom-up in memory.</span></span> <span data-ttu-id="27cd7-134">Weitere Informationen finden Sie unter [Image Stride](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="27cd7-134">For more information, see [Image Stride](image-stride.md).</span></span>
3.  <span data-ttu-id="27cd7-135">Behalten Sie den Puffer nur dann bei, wenn Sie auf den Speicher zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-135">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="27cd7-136">Entsperren Sie den Puffer durch Aufrufen von [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span><span class="sxs-lookup"><span data-stu-id="27cd7-136">Unlock the buffer by calling [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).</span></span>

<span data-ttu-id="27cd7-137">Nicht jeder Medien Puffer implementiert die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="27cd7-137">Not every media buffer implements the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span> <span data-ttu-id="27cd7-138">Wenn der Medien Puffer diese Schnittstelle nicht implementiert (d. h., das Puffer Objekt gibt E \_ nointerface in Schritt 1 zurück), müssen Sie die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstellen Schnittstelle verwenden, die weiter unten beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="27cd7-138">If the media buffer does not implement this interface (that is, the buffer object returns E\_NOINTERFACE in step 1), you must use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface interface, described next.</span></span>

## <a name="use-the-imfmediabuffer-interface"></a><span data-ttu-id="27cd7-139">Verwenden der imfmediabuffer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="27cd7-139">Use the IMFMediaBuffer Interface</span></span>

<span data-ttu-id="27cd7-140">Wenn ein Medien Puffer die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle nicht verfügbar macht, verwenden Sie die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="27cd7-140">If a media buffer does not expose the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="27cd7-141">Die allgemeine Semantik dieser Schnittstelle wird im Thema [Arbeiten mit Medien Puffern](working-with-media-buffers.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="27cd7-141">The general semantics of this interface are described in the topic [Working with Media Buffers](working-with-media-buffers.md).</span></span>

1.  <span data-ttu-id="27cd7-142">Ruft **QueryInterface** für den Medien Puffer auf, um die [**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-142">Call **QueryInterface** on the media buffer to get the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span>
2.  <span data-ttu-id="27cd7-143">Aufrufen von [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) , um auf den Pufferspeicher zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-143">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to access the buffer memory.</span></span> <span data-ttu-id="27cd7-144">Diese Methode gibt einen Zeiger auf den Pufferspeicher zurück.</span><span class="sxs-lookup"><span data-stu-id="27cd7-144">This method returns a pointer to the buffer memory.</span></span> <span data-ttu-id="27cd7-145">Wenn die **Lock** -Methode verwendet wird, ist der Stride immer der minimale Schritt für das betreffende Videoformat und ohne zusätzliche Auffüll Zeichen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-145">When the **Lock** method is used, the stride is always the minimum stride for the video format in question, with no extra padding bytes.</span></span>
3.  <span data-ttu-id="27cd7-146">Behalten Sie den Puffer nur dann bei, wenn Sie auf den Speicher zugreifen müssen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-146">Keep the buffer locked only while you need to access the memory.</span></span> <span data-ttu-id="27cd7-147">Entsperren Sie den Puffer, indem Sie [**imfmediabuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-147">Unlock the buffer by calling [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).</span></span>

<span data-ttu-id="27cd7-148">Sie sollten immer vermeiden, dass [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufgerufen wird, wenn der Puffer [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)verfügbar macht, da die **Lock** -Methode das Puffer Objekt für den Videoframe in einem zusammenhängenden Speicherblock erzwingen und dann wieder zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="27cd7-148">You should always avoid calling [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) if the buffer exposes [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), because the **Lock** method can force the buffer object to the video frame into a contiguous memory block and then back again.</span></span> <span data-ttu-id="27cd7-149">Wenn der Puffer dagegen **IMF2DBuffer** nicht unterstützt, führt **imfmediabuffer:: Lock** wahrscheinlich nicht zu einer Kopie.</span><span class="sxs-lookup"><span data-stu-id="27cd7-149">On the other hand, if the buffer does not support **IMF2DBuffer**, then **IMFMediaBuffer::Lock** will probably not result in a copy.</span></span>

<span data-ttu-id="27cd7-150">Berechnen Sie den minimalen Schritt vom Medientyp wie folgt:</span><span class="sxs-lookup"><span data-stu-id="27cd7-150">Calculate the minimum stride from the media type as follows:</span></span>

-   <span data-ttu-id="27cd7-151">Der minimale Schritt kann im [**MF \_ MT-Standard- \_ \_ Stride**](mf-mt-default-stride-attribute.md) -Attribut gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="27cd7-151">The minimum stride might be stored in the [**MF\_MT\_DEFAULT\_STRIDE**](mf-mt-default-stride-attribute.md) attribute.</span></span>
-   <span data-ttu-id="27cd7-152">Wenn das **MF \_ MT- \_ Standard- \_ Stride** -Attribut nicht festgelegt ist, müssen Sie die [**mfgetstrideforbitmapinfoheader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) -Funktion aufrufen, um den Schritt für die meisten gängigen Videoformate zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-152">If the **MF\_MT\_DEFAULT\_STRIDE** attribute is not set, call the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function to calculate the stride for most common video formats.</span></span>
-   <span data-ttu-id="27cd7-153">Wenn die [**mfgetstrideforbitmapinfoheader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) -Funktion das Format nicht erkennt, müssen Sie den Stride basierend auf der Definition des Formats berechnen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-153">If the [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) function does not recognize the format, you must calculate the stride based on the definition of the format.</span></span> <span data-ttu-id="27cd7-154">In diesem Fall gibt es keine allgemeine Regel. Sie müssen die Details der Format Definition kennen.</span><span class="sxs-lookup"><span data-stu-id="27cd7-154">In that case, there is no general rule; you need to know the details of the format definition.</span></span>

<span data-ttu-id="27cd7-155">Der folgende Code zeigt, wie Sie den Standard Schritt für die gängigsten Videoformate erhalten.</span><span class="sxs-lookup"><span data-stu-id="27cd7-155">The following code shows how to get the default stride for the most common video formats.</span></span>


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



<span data-ttu-id="27cd7-156">Abhängig von Ihrer Anwendung können Sie im Voraus wissen, ob ein bestimmter Medien Puffer [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) unterstützt (z. b. Wenn Sie den Puffer erstellt haben).</span><span class="sxs-lookup"><span data-stu-id="27cd7-156">Depending on your application, you might know in advance whether a given media buffer supports [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) (for example, if you created the buffer).</span></span> <span data-ttu-id="27cd7-157">Andernfalls müssen Sie darauf vorbereitet sein, eine der beiden Puffer Schnittstellen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="27cd7-157">Otherwise, you must be prepared to use either of the two buffer interfaces.</span></span>

<span data-ttu-id="27cd7-158">Das folgende Beispiel zeigt eine Hilfsklasse, die einige dieser Details verbirgt.</span><span class="sxs-lookup"><span data-stu-id="27cd7-158">The following example shows a helper class that hides some of these details.</span></span> <span data-ttu-id="27cd7-159">Diese Klasse verfügt über eine LockBuffer-Methode, die entweder [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) oder [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) aufruft und einen Zeiger auf den Anfang der ersten Zeile der Pixel zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="27cd7-159">This class has a LockBuffer method that calls either [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) or [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and returns a pointer to the start of the first row of pixels.</span></span> <span data-ttu-id="27cd7-160">(Dieses Verhalten stimmt mit der **Lock2D** -Methode überein.) Die LockBuffer-Methode nimmt den Standard Stride als Eingabeparameter an und gibt den eigentlichen Stride als Ausgabeparameter zurück.</span><span class="sxs-lookup"><span data-stu-id="27cd7-160">(This behavior matches the **Lock2D** method.) The LockBuffer method takes the default stride as an input parameter and returns the actual stride as an output parameter.</span></span>


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a><span data-ttu-id="27cd7-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="27cd7-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27cd7-162">Bild Schritt</span><span class="sxs-lookup"><span data-stu-id="27cd7-162">Image Stride</span></span>](image-stride.md)
</dt> <dt>

[<span data-ttu-id="27cd7-163">Medien Puffer</span><span class="sxs-lookup"><span data-stu-id="27cd7-163">Media Buffers</span></span>](media-buffers.md)
</dt> </dl>

 

 



