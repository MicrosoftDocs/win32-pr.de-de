---
description: EVR-Medientyp Aushandlung
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: EVR-Medientyp Aushandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb1f87a24db866c9e80b211b0385c12dcd6b594
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351458"
---
# <a name="evr-media-type-negotiation"></a><span data-ttu-id="a0650-103">EVR-Medientyp Aushandlung</span><span class="sxs-lookup"><span data-stu-id="a0650-103">EVR Media Type Negotiation</span></span>

<span data-ttu-id="a0650-104">In diesem Thema wird beschrieben, wie der Enhanced Video Renderer (EVR) Medientypen validiert.</span><span class="sxs-lookup"><span data-stu-id="a0650-104">This topic describes how the enhanced video renderer (EVR) validates media types.</span></span>

-   <span data-ttu-id="a0650-105">Beim DirectShow-EVR-Filter erfolgt die typaushandlung, wenn die Pins des Filters verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="a0650-105">For the DirectShow EVR filter, type negotiation occurs when the filter's pins are connected.</span></span>

-   <span data-ttu-id="a0650-106">Für die EVR-Medien Senke werden die Medientypen über die [**IMF mediatyethandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) -Schnittstelle auf den streamsenken festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a0650-106">For the EVR media sink, the media types are set through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream sinks.</span></span> <span data-ttu-id="a0650-107">In der Regel aushandt der topologielader die Medientypen, obwohl die Anwendung auch die Medientypen direkt festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="a0650-107">Typically the topology loader negotiates the media types, although the application can also set the media types directly.</span></span>

<span data-ttu-id="a0650-108">Der EVR meldet keine bevorzugten Medientypen.</span><span class="sxs-lookup"><span data-stu-id="a0650-108">The EVR does not report any preferred media types.</span></span> <span data-ttu-id="a0650-109">Der Client muss die Medientypen testen, bis er einen akzeptablen Typ findet.</span><span class="sxs-lookup"><span data-stu-id="a0650-109">The client must test media types until it finds an acceptable type.</span></span> <span data-ttu-id="a0650-110">Der Medientyp für den Verweis Datenstrom muss festgelegt werden, bevor die Typen für die untergeordneten Datenströme festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="a0650-110">The media type for the reference stream must be set before the types can be set on any of the substreams.</span></span>

<span data-ttu-id="a0650-111">Für den Verweis Datenstrom erhält der EVR-Mixer eine Liste mit kompatiblen DXVA-renderingzielformaten (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="a0650-111">For the reference stream, the EVR mixer gets a list of compatible DirectX Video Acceleration (DXVA) render target formats.</span></span> <span data-ttu-id="a0650-112">Der EVR Presenter verwendet diese Liste, um das Format für die Direct3D SwapChain auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a0650-112">The EVR presenter uses this list to select the format for the Direct3D swap chain.</span></span> <span data-ttu-id="a0650-113">Wenn kein kompatibles renderzielformat gefunden werden kann, lehnt der EVR den Medientyp ab.</span><span class="sxs-lookup"><span data-stu-id="a0650-113">If no compatible render target format can be found, the EVR rejects the media type.</span></span>

<span data-ttu-id="a0650-114">Bei den Substreams fragt der EVR-Mixer, ob das DXVA-Gerät dieses substreamformat in Kombination mit dem renderzielformat unterstützt, das für den Verweis Datenstrom ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="a0650-114">For the substreams, the EVR mixer queries whether the DXVA device supports that substream format in combination with the render target format that was selected for the reference stream.</span></span> <span data-ttu-id="a0650-115">Folglich können sich die verfügbaren substreamformate abhängig vom Verweisstream ändern.</span><span class="sxs-lookup"><span data-stu-id="a0650-115">As a result, the available substream formats might change depending on the reference stream.</span></span>

<span data-ttu-id="a0650-116">Im folgenden wird der Prozess ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a0650-116">Here is the process in more detail.</span></span> <span data-ttu-id="a0650-117">Diese Details sind für die meisten Anwendungen nicht wichtig, sind aber möglicherweise hilfreich, wenn Sie einen benutzerdefinierten Mixer oder Presenter schreiben.</span><span class="sxs-lookup"><span data-stu-id="a0650-117">These details are not important for most applications, but might be helpful if you are writing a custom mixer or presenter.</span></span>

<span data-ttu-id="a0650-118">Für den Verweis Datenstrom erfolgt die Aushandlung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a0650-118">For the reference stream, negotiation happens as follows:</span></span>

1.  <span data-ttu-id="a0650-119">Der EVR ruft [**IMF Transform:: abtinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf dem Mixer auf.</span><span class="sxs-lookup"><span data-stu-id="a0650-119">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="a0650-120">Der Mixer konvertiert den Medientyp mithilfe der [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) -Struktur in eine DXVA 2,0-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="a0650-120">The mixer converts the media type to a DXVA 2.0 description, using the [**DXVA2\_VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) structure.</span></span>

3.  <span data-ttu-id="a0650-121">Der Mixer ruft [**idirectxvideoprocmeorservice:: getvideoprocess ordeviceguids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) auf, um eine Liste der Videoprozessor-GUIDs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a0650-121">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) to get a list of video processor GUIDs.</span></span>

4.  <span data-ttu-id="a0650-122">Für jede Videoprozessor-GUID ruft der-Mixer [**idirectxvideoprocesorservice:: getvideoprocess orrendertargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) auf, um die unterstützten renderzielformate zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0650-122">For each video processor GUID, the mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) to get the supported render target formats.</span></span>

5.  <span data-ttu-id="a0650-123">Der EVR ruft [**IMF videopresenter::P rocess Message**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) für den Presenter mit der \_ Meldung "invalidatemediatype" der MF-Nachricht auf \_ .</span><span class="sxs-lookup"><span data-stu-id="a0650-123">The EVR calls [**IMFVideoPresenter::ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) on the presenter with the MFVP\_MESSAGE\_INVALIDATEMEDIATYPE message.</span></span> <span data-ttu-id="a0650-124">Diese Meldung bewirkt, dass der Presenter ein neues Format auswählt.</span><span class="sxs-lookup"><span data-stu-id="a0650-124">This message causes the presenter to select a new format.</span></span>

6.  <span data-ttu-id="a0650-125">Der Presenter ruft [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) auf, um eine Liste der verfügbaren Ausgabeformate vom Mixer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0650-125">The presenter calls [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get a list of available output formats from the mixer.</span></span> <span data-ttu-id="a0650-126">Der Mixer generiert diese Liste aus den in Schritt 4 erhaltenen Formaten.</span><span class="sxs-lookup"><span data-stu-id="a0650-126">The mixer generates this list from the formats obtained in step 4.</span></span>

7.  <span data-ttu-id="a0650-127">Der Presenter wählt ein Format aus und ruft [**IMF Transform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) auf dem Mixer auf.</span><span class="sxs-lookup"><span data-stu-id="a0650-127">The presenter selects a format and calls [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) on the mixer.</span></span>

<span data-ttu-id="a0650-128">Für Substreams ist der Prozess einfacher:</span><span class="sxs-lookup"><span data-stu-id="a0650-128">For substreams, the process is simpler:</span></span>

1.  <span data-ttu-id="a0650-129">Der EVR ruft [**IMF Transform:: abtinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) auf dem Mixer auf.</span><span class="sxs-lookup"><span data-stu-id="a0650-129">The EVR calls [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) on the mixer.</span></span>

2.  <span data-ttu-id="a0650-130">Der Mixer ruft [**idirectxvideoprocess orservice:: getvideoprocess orsubstreamformats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) auf, um eine Liste der verfügbaren substreamformate zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0650-130">The mixer calls [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) to get a list of available substream formats.</span></span>

3.  <span data-ttu-id="a0650-131">Wenn das vorgeschlagene Format in dieser Liste enthalten ist, akzeptiert das EVR den Eingabetyp.</span><span class="sxs-lookup"><span data-stu-id="a0650-131">If the proposed format is contained in this list, the EVR accepts the input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0650-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a0650-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0650-133">Erweiterter Videorenderer</span><span class="sxs-lookup"><span data-stu-id="a0650-133">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



