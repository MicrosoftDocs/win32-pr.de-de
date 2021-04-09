---
description: Video Beispiele
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Video Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863924"
---
# <a name="video-samples"></a><span data-ttu-id="6aaff-103">Video Beispiele</span><span class="sxs-lookup"><span data-stu-id="6aaff-103">Video Samples</span></span>

<span data-ttu-id="6aaff-104">Das Video Sample-Objekt ist eine spezialisierte Implementierung der [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle für die Verwendung mit dem [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="6aaff-104">The video sample object is a specialized implementation of the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface for use with the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="6aaff-105">Rufen Sie die [**mfcreatevideosamplefromsurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) -Funktion auf, um eine Instanz dieses Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6aaff-105">To create an instance of this object, call the [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) function.</span></span> <span data-ttu-id="6aaff-106">Die Funktion nimmt einen Zeiger auf eine Direct3D-Oberfläche und gibt einen Zeiger auf die **imfsample** -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="6aaff-106">The function takes a pointer to a Direct3D surface and returns a pointer to the **IMFSample** interface.</span></span> <span data-ttu-id="6aaff-107">Die folgenden Objekttypen sollten mithilfe dieser Funktion Beispiele zuordnen:</span><span class="sxs-lookup"><span data-stu-id="6aaff-107">The following types of objects should allocate samples using this function:</span></span>

-   <span data-ttu-id="6aaff-108">Benutzerdefinierte EVR-Moderatoren.</span><span class="sxs-lookup"><span data-stu-id="6aaff-108">Custom EVR presenters.</span></span> <span data-ttu-id="6aaff-109">Ein Presenter ordnet Videobeispiele zu und sendet Sie an die [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode des Mischers.</span><span class="sxs-lookup"><span data-stu-id="6aaff-109">A presenter allocates video samples and sends them to the mixer's [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) method.</span></span> <span data-ttu-id="6aaff-110">Weitere Informationen finden Sie unter [How to Write a EVR Presenter](how-to-write-an-evr-presenter.md).</span><span class="sxs-lookup"><span data-stu-id="6aaff-110">For more information, see [How to Write an EVR Presenter](how-to-write-an-evr-presenter.md).</span></span>

-   <span data-ttu-id="6aaff-111">Video-Decoder, die Videobeschleunigung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6aaff-111">Video decoders that support video acceleration.</span></span> <span data-ttu-id="6aaff-112">Weitere Informationen finden Sie [unter unterstützen von DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="6aaff-112">For more information, see [Supporting DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).</span></span>

<span data-ttu-id="6aaff-113">Das Video Sample-Objekt implementiert die folgenden Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="6aaff-113">The video sample object implements the following interfaces:</span></span>

-   [<span data-ttu-id="6aaff-114">**IMF Sample**</span><span class="sxs-lookup"><span data-stu-id="6aaff-114">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [<span data-ttu-id="6aaff-115">**IMF-redsample**</span><span class="sxs-lookup"><span data-stu-id="6aaff-115">**IMFDesiredSample**</span></span>](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [<span data-ttu-id="6aaff-116">**IMF trackedsample**</span><span class="sxs-lookup"><span data-stu-id="6aaff-116">**IMFTrackedSample**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

<span data-ttu-id="6aaff-117">Wenn der *punksurface* -Parameter von [**MF createvideosamplefromsurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) nicht **null** ist, enthält das resultierende Video Beispiel einen einzelnen Medien Puffer, der die Direct3D-Oberfläche kapselt.</span><span class="sxs-lookup"><span data-stu-id="6aaff-117">If the *pUnkSurface* parameter of [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) is non-**NULL**, the resulting video sample contains a single media buffer that encapsulates the Direct3D surface.</span></span> <span data-ttu-id="6aaff-118">Dieses Puffer Objekt verfügt über eingeschränkte Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="6aaff-118">This buffer object has limited functionality:</span></span>

-   <span data-ttu-id="6aaff-119">Die [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) -Methode des Puffers gibt E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="6aaff-119">The buffer's [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) method returns E\_NOTIMPL.</span></span>

-   <span data-ttu-id="6aaff-120">Die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle wird vom Puffer nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="6aaff-120">The buffer does not implement the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

<span data-ttu-id="6aaff-121">Die einzige Möglichkeit für den Zugriff auf die-Oberfläche aus dem Puffer besteht darin, [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)mit dem Dienst Bezeichner Mr- \_ Puffer Dienst aufzurufen \_ .</span><span class="sxs-lookup"><span data-stu-id="6aaff-121">The only way to access the surface from the buffer is to call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice), using the service identifier MR\_BUFFER\_SERVICE.</span></span>

<span data-ttu-id="6aaff-122">Wenn der Parameter " *punksurface* " **null** ist, wird das Video Beispiel mit NULL Medien Puffern erstellt.</span><span class="sxs-lookup"><span data-stu-id="6aaff-122">If the *pUnkSurface* parameter is **NULL**, the video sample is created with zero media buffers.</span></span> <span data-ttu-id="6aaff-123">Um dem Beispiel einen Puffer hinzuzufügen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="6aaff-123">To add a buffer the sample, do the following:</span></span>

1.  <span data-ttu-id="6aaff-124">Erstellen Sie eine Direct3D-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="6aaff-124">Create a Direct3D surface.</span></span>

2.  <span data-ttu-id="6aaff-125">Erstellen Sie einen Oberflächen Puffer, indem Sie [**mfcreatedxsurfacebuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6aaff-125">Create a surface buffer by calling [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer).</span></span> <span data-ttu-id="6aaff-126">Weitere Informationen finden Sie unter [DirectX-Oberflächen Puffer](directx-surface-buffer.md).</span><span class="sxs-lookup"><span data-stu-id="6aaff-126">For more information, see [DirectX Surface Buffer](directx-surface-buffer.md).</span></span>

3.  <span data-ttu-id="6aaff-127">Fügen Sie den Puffer dem Beispiel hinzu, indem Sie [**imfsample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6aaff-127">Add the buffer to the sample by calling [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer).</span></span>

<span data-ttu-id="6aaff-128">Verwenden Sie diesen Ansatz, wenn Sie den Surface-Speicher über die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle zugänglich sein müssen.</span><span class="sxs-lookup"><span data-stu-id="6aaff-128">Use this approach if you need the surface memory to be accessible through the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6aaff-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6aaff-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6aaff-130">Medien Puffer</span><span class="sxs-lookup"><span data-stu-id="6aaff-130">Media Buffers</span></span>](media-buffers.md)
</dt> <dt>

[<span data-ttu-id="6aaff-131">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="6aaff-131">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 
