---
description: DirectX-Oberflächen Puffer
ms.assetid: 2c82c023-4436-4f8a-b896-7f4765f989b3
title: DirectX-Oberflächen Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02211d268e23bd7185cd480bee4e4dff297293b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127904"
---
# <a name="directx-surface-buffer"></a><span data-ttu-id="ada56-103">DirectX-Oberflächen Puffer</span><span class="sxs-lookup"><span data-stu-id="ada56-103">DirectX Surface Buffer</span></span>

<span data-ttu-id="ada56-104">Das DirectX-Oberflächen Puffer Objekt ist ein Medien Puffer, der eine Direct3D-Oberfläche verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ada56-104">The DirectX surface buffer object is a media buffer that manages a Direct3D surface.</span></span> <span data-ttu-id="ada56-105">Um eine Instanz dieses Objekts zu erstellen, rufen Sie [**mfkreatedxsurfacebuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) auf und übergeben einen Zeiger auf die DirectX-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="ada56-105">To create an instance of this object, call [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer) and pass in a pointer to the DirectX surface.</span></span> <span data-ttu-id="ada56-106">Der DirectX-Oberflächen Puffer macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="ada56-106">The DirectX surface buffer exposes the following interfaces:</span></span>

-   [<span data-ttu-id="ada56-107">**Imfmediabuffer**</span><span class="sxs-lookup"><span data-stu-id="ada56-107">**IMFMediaBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
-   [<span data-ttu-id="ada56-108">**IMF2DBuffer**</span><span class="sxs-lookup"><span data-stu-id="ada56-108">**IMF2DBuffer**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)
-   [<span data-ttu-id="ada56-109">**IMF-Dienst**</span><span class="sxs-lookup"><span data-stu-id="ada56-109">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

<span data-ttu-id="ada56-110">Es gibt mehrere Möglichkeiten, auf den Surface-Speicher aus dem Puffer Objekt zuzugreifen:</span><span class="sxs-lookup"><span data-stu-id="ada56-110">There are several ways to access the surface memory from the buffer object:</span></span>

-   <span data-ttu-id="ada56-111">Empfohlen: [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) wird für den Puffer aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ada56-111">Recommended: Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the buffer.</span></span> <span data-ttu-id="ada56-112">Verwenden Sie den Dienst Bezeichner **Mr- \_ Puffer \_ Dienst**.</span><span class="sxs-lookup"><span data-stu-id="ada56-112">Use the service identifier **MR\_BUFFER\_SERVICE**.</span></span> <span data-ttu-id="ada56-113">Die-Methode gibt einen Zeiger auf die zugrunde liegende Direct3D-Oberfläche zurück.</span><span class="sxs-lookup"><span data-stu-id="ada56-113">The method returns a pointer to the underlying Direct3D surface.</span></span>
-   <span data-ttu-id="ada56-114">[**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ada56-114">Call [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d).</span></span> <span data-ttu-id="ada56-115">Diese Methode ruft **IDirect3DSurface9:: lockrect** direkt auf der-Oberfläche auf.</span><span class="sxs-lookup"><span data-stu-id="ada56-115">This method calls **IDirect3DSurface9::LockRect** directly on the surface.</span></span> <span data-ttu-id="ada56-116">Die [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) -Methode ruft **unlockrect** auf der-Oberfläche auf.</span><span class="sxs-lookup"><span data-stu-id="ada56-116">The [**IMF2DBuffer::Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d) method calls **UnlockRect** on the surface.</span></span>
-   <span data-ttu-id="ada56-117">Rückrufe [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span><span class="sxs-lookup"><span data-stu-id="ada56-117">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock).</span></span> <span data-ttu-id="ada56-118">Dies wird im Allgemeinen nicht empfohlen, da das-Objekt zwingt, Arbeitsspeicher von der Direct3D-Oberfläche und dann wieder zurück zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="ada56-118">Generally this is not recommended, because it forces the object to copy memory from the Direct3D surface and then back again.</span></span> <span data-ttu-id="ada56-119">Die [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) -Methode ist effizienter.</span><span class="sxs-lookup"><span data-stu-id="ada56-119">The [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method is more efficient.</span></span>

<span data-ttu-id="ada56-120">Sowohl [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) als auch [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) können fehlschlagen, wenn die zugrunde liegende Oberfläche nicht Sperr fähig ist.</span><span class="sxs-lookup"><span data-stu-id="ada56-120">Both [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) and [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) can fail if the underlying surface is not lockable.</span></span> <span data-ttu-id="ada56-121">Der DirectX-Oberflächen Puffer implementiert diese beiden Methoden primär für Komponenten, die nicht für die Verwendung mit Direct3D-Oberflächen entwickelt wurden.</span><span class="sxs-lookup"><span data-stu-id="ada56-121">The DirectX surface buffer implements these two methods primarily for components that are not designed to work with Direct3D surfaces.</span></span>

<span data-ttu-id="ada56-122">Der Enhanced Video Renderer (EVR) erstellt DirectX-Oberflächen Puffer, wenn der Decoder nicht für die DirectX-Videobeschleunigung (DXVA) konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="ada56-122">The enhanced video renderer (EVR) creates DirectX surface buffers when the decoder is not configured for DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="ada56-123">Weitere Informationen finden Sie unter [**IMF videosamplezuordcator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span><span class="sxs-lookup"><span data-stu-id="ada56-123">For more information, see [**IMFVideoSampleAllocator**](/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator).</span></span>

### <a name="obtaining-the-direct3d-surface"></a><span data-ttu-id="ada56-124">Abrufen der Direct3D-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="ada56-124">Obtaining the Direct3D Surface</span></span>

<span data-ttu-id="ada56-125">Gehen Sie folgendermaßen vor, um eine Direct3D-Oberfläche aus einem Video Beispiel zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="ada56-125">To get a Direct3D surface from a video sample, do the following:</span></span>

1.  <span data-ttu-id="ada56-126">Aufrufen von [**imfsample:: getbufferbyindex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) mit einem Indexwert von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ada56-126">Call [**IMFSample::GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) with an index value of zero.</span></span>
2.  <span data-ttu-id="ada56-127">Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) und angeben des Dienst Bezeichners für den **Mr- \_ Puffer \_ Dienst** .</span><span class="sxs-lookup"><span data-stu-id="ada56-127">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and specify the **MR\_BUFFER\_SERVICE** service identifier.</span></span>

<span data-ttu-id="ada56-128">Diese Schritte sind im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ada56-128">The following code shows these steps:</span></span>


```C++
HRESULT GetD3DSurfaceFromSample(IMFSample *pSample, IDirect3DSurface9 **ppSurface)
{
    *ppSurface = NULL;

    IMFMediaBuffer *pBuffer = NULL;

    HRESULT hr = pSample->GetBufferByIndex(0, &pBuffer);
    if (SUCCEEDED(hr))
    {
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(ppSurface));
        pBuffer->Release();
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ada56-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ada56-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ada56-130">Medien Puffer</span><span class="sxs-lookup"><span data-stu-id="ada56-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="ada56-131">Video Beispiele</span><span class="sxs-lookup"><span data-stu-id="ada56-131">Video Samples</span></span>](video-samples.md)
</dt> </dl>

 

 



