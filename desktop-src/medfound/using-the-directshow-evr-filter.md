---
description: Verwenden des DirectShow-EVR-Filters
ms.assetid: 4d85aed0-4b11-4c5f-bfc0-cad0a7d2f490
title: Verwenden des DirectShow-EVR-Filters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02568a5ea9cbaa0310409a5a0966a2bea1bbfffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356637"
---
# <a name="using-the-directshow-evr-filter"></a><span data-ttu-id="30a99-103">Verwenden des DirectShow-EVR-Filters</span><span class="sxs-lookup"><span data-stu-id="30a99-103">Using the DirectShow EVR Filter</span></span>

<span data-ttu-id="30a99-104">Um den EVR-Filter (Enhanced Video Renderer) zu erstellen, rufen Sie **cokreateinstance** auf.</span><span class="sxs-lookup"><span data-stu-id="30a99-104">To create the enhanced video renderer (EVR) filter, call **CoCreateInstance**.</span></span> <span data-ttu-id="30a99-105">Die CLSID ist CLSID \_ enhancedvidederer, der in UUIDs. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="30a99-105">The CLSID is CLSID\_EnhancedVideoRenderer, defined in uuids.h.</span></span> <span data-ttu-id="30a99-106">Sie müssen [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) oder [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) nicht für die Verwendung des EVR-Filters anrufen.</span><span class="sxs-lookup"><span data-stu-id="30a99-106">You do not have to call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) or [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to use the EVR filter.</span></span>

<span data-ttu-id="30a99-107">Weitere Informationen zum Verwenden des EVR-Filters in einer DirectShow-Anwendung finden Sie unter [Audiowiedergabe und Video Wiedergabe in DirectShow](../directshow/audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="30a99-107">For more information about using the EVR filter in a DirectShow application, see [Audio/Video Playback in DirectShow](../directshow/audio-video-playback-in-directshow.md).</span></span>

<span data-ttu-id="30a99-108">Der EVR-Filter beginnt mit einer Eingabe-PIN, die dem Verweis Datenstrom entspricht.</span><span class="sxs-lookup"><span data-stu-id="30a99-108">The EVR filter starts with one input pin, which corresponds to the reference stream.</span></span> <span data-ttu-id="30a99-109">Um Pins für unter Ströme hinzuzufügen, Fragen Sie den Filter nach der [**ievrfilterconfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) -Schnittstelle ab, und nennen Sie [**ievrfilterconfig:: setnumofstreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span><span class="sxs-lookup"><span data-stu-id="30a99-109">To add pins for substreams, query the filter for the [**IEVRFilterConfig**](/windows/desktop/api/evr/nn-evr-ievrfilterconfig) interface and call [**IEVRFilterConfig::SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams).</span></span> <span data-ttu-id="30a99-110">Nennen Sie diese Methode, bevor Sie eine Verbindung mit Eingabe Pins herstellen.</span><span class="sxs-lookup"><span data-stu-id="30a99-110">Call this method before connecting any input pins.</span></span> <span data-ttu-id="30a99-111">PIN 0 ist immer der Verweis Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="30a99-111">Pin 0 is always the reference stream.</span></span> <span data-ttu-id="30a99-112">Verbinden Sie diese Pin vor allen anderen Pins, da das Format des Verweis Datenstroms möglicherweise einschränkt, welche substreamformate verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="30a99-112">Connect this pin before any other pins, because the format of the reference stream might limit which substream formats are available.</span></span>

<span data-ttu-id="30a99-113">Legen Sie vor dem Starten des Diagramms das Video Clipping-Fenster und das Ziel Rechteck fest.</span><span class="sxs-lookup"><span data-stu-id="30a99-113">Before starting the graph, set the video clipping window and the destination rectangle.</span></span> <span data-ttu-id="30a99-114">Weitere Informationen finden Sie unter [Verwenden der Video Anzeige Steuerelemente](using-the-video-display-controls.md).</span><span class="sxs-lookup"><span data-stu-id="30a99-114">For more information, see [Using the Video Display Controls](using-the-video-display-controls.md).</span></span>

<span data-ttu-id="30a99-115">Im Gegensatz zum Video Mischungs-Renderer (VMR) verfügt der EVR nicht über Betriebsmodi (Fenster, fensterlose usw.).</span><span class="sxs-lookup"><span data-stu-id="30a99-115">Unlike the Video Mixing Renderer (VMR), the EVR does not have operational modes (windowed, windowless, and so forth).</span></span> <span data-ttu-id="30a99-116">Dies gilt insbesondere für:</span><span class="sxs-lookup"><span data-stu-id="30a99-116">In particular:</span></span>

-   <span data-ttu-id="30a99-117">Der EVR unterstützt den Fenster-Modus nicht.</span><span class="sxs-lookup"><span data-stu-id="30a99-117">The EVR does not support windowed mode.</span></span> <span data-ttu-id="30a99-118">Die Anwendung muss das clippingfenster bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="30a99-118">The application must provide the clipping window.</span></span>
-   <span data-ttu-id="30a99-119">Der EVR weist keinen renderlosen Modus auf.</span><span class="sxs-lookup"><span data-stu-id="30a99-119">The EVR does not have a renderless mode.</span></span> <span data-ttu-id="30a99-120">Um den Standard Presenter zu ersetzen, nennen Sie [**imfvideorenderer:: initializererderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span><span class="sxs-lookup"><span data-stu-id="30a99-120">To replace the default presenter, call [**IMFVideoRenderer::InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).</span></span>
-   <span data-ttu-id="30a99-121">Der EVR weist keinen Mischungs Modus auf.</span><span class="sxs-lookup"><span data-stu-id="30a99-121">The EVR does not have a mixing mode.</span></span> <span data-ttu-id="30a99-122">Der EVR erstellt immer den Mixer.</span><span class="sxs-lookup"><span data-stu-id="30a99-122">The EVR always creates the mixer.</span></span> <span data-ttu-id="30a99-123">Wenn Sie über einen Eingabestream verfügen, ist es nicht erforderlich, [**setnumofstreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) aufzurufen, um die Verwendung des Mixers durch den EVR zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="30a99-123">If you have one input stream, it is not necessary to call [**SetNumberOfStreams**](/windows/desktop/api/evr/nf-evr-ievrfilterconfig-setnumberofstreams) to force the EVR to use the mixer.</span></span>

## <a name="filter-interfaces"></a><span data-ttu-id="30a99-124">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="30a99-124">Filter Interfaces</span></span>

<span data-ttu-id="30a99-125">Der EVR-Filter macht die folgenden Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30a99-125">The EVR filter exposes the following interfaces.</span></span> <span data-ttu-id="30a99-126">Einige dieser Schnittstellen sind im DirectShow SDK dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="30a99-126">Some of these interfaces are documented in the DirectShow SDK.</span></span> <span data-ttu-id="30a99-127">Verwenden Sie **QueryInterface** zum Abrufen von Zeigern auf diese Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="30a99-127">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   <span data-ttu-id="30a99-128">[**Iamcertifiedoutputprotection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="30a99-128">[**IAMCertifiedOutputProtection**](/windows/win32/api/strmif/nn-strmif-iamcertifiedoutputprotection) (DirectShow)</span></span>
-   <span data-ttu-id="30a99-129">[**Iamfilterfehlflags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="30a99-129">[**IAMFilterMiscFlags**](/windows/win32/api/strmif/nn-strmif-iamfiltermiscflags) (DirectShow)</span></span>
-   <span data-ttu-id="30a99-130">[**Ibasefilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="30a99-130">[**IBaseFilter**](/windows/win32/api/strmif/nn-strmif-ibasefilter) (DirectShow)</span></span>
-   [<span data-ttu-id="30a99-131">**Ievrfilterconfig**</span><span class="sxs-lookup"><span data-stu-id="30a99-131">**IEVRFilterConfig**</span></span>](/windows/desktop/api/evr/nn-evr-ievrfilterconfig)
-   <span data-ttu-id="30a99-132">" [**Ikspropertyset**](../directshow/ikspropertyset.md) " (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="30a99-132">[**IKsPropertySet**](../directshow/ikspropertyset.md) (DirectShow)</span></span>
-   <span data-ttu-id="30a99-133">[**Imediaeventsink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="30a99-133">[**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) (DirectShow)</span></span>
-   [<span data-ttu-id="30a99-134">**IMF-Dienst**</span><span class="sxs-lookup"><span data-stu-id="30a99-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="30a99-135">**IMF videopositionmapper**</span><span class="sxs-lookup"><span data-stu-id="30a99-135">**IMFVideoPositionMapper**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper)
-   [<span data-ttu-id="30a99-136">**Imsvideorenderer**</span><span class="sxs-lookup"><span data-stu-id="30a99-136">**IMFVideoRenderer**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
-   <span data-ttu-id="30a99-137">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="30a99-137">**IPersistStream**</span></span>
-   <span data-ttu-id="30a99-138">[**Iqualitycontrol**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="30a99-138">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>
-   <span data-ttu-id="30a99-139">[**Iqualprop**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="30a99-139">[**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop) (DirectShow)</span></span>
-   <span data-ttu-id="30a99-140">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="30a99-140">**ISpecifyPropertyPages**</span></span>

## <a name="input-pin-interfaces"></a><span data-ttu-id="30a99-141">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="30a99-141">Input Pin Interfaces</span></span>

<span data-ttu-id="30a99-142">Die Eingabe Pins im EVR-Filter machen die folgenden Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="30a99-142">The input pins on the EVR filter expose the following interfaces.</span></span> <span data-ttu-id="30a99-143">Verwenden Sie **QueryInterface** zum Abrufen von Zeigern auf diese Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="30a99-143">Use **QueryInterface** to retrieve pointers to these interfaces:</span></span>

-   [<span data-ttu-id="30a99-144">**Ievrvideostreamcontrol**</span><span class="sxs-lookup"><span data-stu-id="30a99-144">**IEVRVideoStreamControl**</span></span>](/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol)
-   <span data-ttu-id="30a99-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="30a99-145">[**IMemInputPin**](/windows/win32/api/strmif/nn-strmif-imeminputpin) (DirectShow)</span></span>
-   [<span data-ttu-id="30a99-146">**IMF-Dienst**</span><span class="sxs-lookup"><span data-stu-id="30a99-146">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   <span data-ttu-id="30a99-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="30a99-147">[**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) (DirectShow)</span></span>
-   <span data-ttu-id="30a99-148">[**Iqualitycontrol**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="30a99-148">[**IQualityControl**](/windows/win32/api/strmif/nn-strmif-iqualitycontrol) (DirectShow)</span></span>

<span data-ttu-id="30a99-149">Außerdem können Sie die [**imfgetservice**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle zum Abrufen der folgenden Schnittstelle verwenden:</span><span class="sxs-lookup"><span data-stu-id="30a99-149">In addition, you can use the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface to retrieve the following interface:</span></span>

-   [<span data-ttu-id="30a99-150">**Idirectxvideomemoryconfiguration**</span><span class="sxs-lookup"><span data-stu-id="30a99-150">**IDirectXVideoMemoryConfiguration**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration)

## <a name="related-topics"></a><span data-ttu-id="30a99-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="30a99-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30a99-152">Audiowiedergabe und Video Wiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="30a99-152">Audio/Video Playback in DirectShow</span></span>](../directshow/audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="30a99-153">Erweiterter Videorenderer</span><span class="sxs-lookup"><span data-stu-id="30a99-153">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 
