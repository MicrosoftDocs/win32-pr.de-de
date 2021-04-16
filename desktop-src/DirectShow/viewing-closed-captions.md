---
description: Anzeigen von Untertiteln
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Anzeigen von Untertiteln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571083"
---
# <a name="viewing-closed-captions"></a><span data-ttu-id="a4f75-103">Anzeigen von Untertiteln</span><span class="sxs-lookup"><span data-stu-id="a4f75-103">Viewing Closed Captions</span></span>

<span data-ttu-id="a4f75-104">Zur Unterstützung von Untertiteln im analogen Fernsehen macht der Erfassungs Filter eine PIN verfügbar, die entweder VBI-oder Closed Caption-Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a4f75-104">To support closed captions in analog television, the capture filter exposes a pin that delivers either VBI or closed caption data.</span></span> <span data-ttu-id="a4f75-105">Die PIN weist eine der folgenden Pin-Kategorien auf:</span><span class="sxs-lookup"><span data-stu-id="a4f75-105">The pin will have one of the following pin categories:</span></span>

-   <span data-ttu-id="a4f75-106">VBI-PIN (PIN- \_ Kategorie \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="a4f75-106">VBI pin (PIN\_CATEGORY\_VBI).</span></span> <span data-ttu-id="a4f75-107">Bietet einen Stream von VBI-Wellenform-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="a4f75-107">Delivers a stream of VBI waveform samples.</span></span> <span data-ttu-id="a4f75-108">Diese werden an einen Decoderfilter übermittelt, der die Untertitel Daten extrahiert.</span><span class="sxs-lookup"><span data-stu-id="a4f75-108">These are passed to a decoder filter that extracts the closed captioning data.</span></span>
-   <span data-ttu-id="a4f75-109">CC-PIN (PIN- \_ Kategorie \_ CC).</span><span class="sxs-lookup"><span data-stu-id="a4f75-109">CC pin (PIN\_CATEGORY\_CC).</span></span> <span data-ttu-id="a4f75-110">Übermittelt aus den Zeilen 21 Daten extrahierte Byte-Paare mit geschlossener Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="a4f75-110">Delivers closed-caption byte pairs, extracted from the line-21 data.</span></span>
-   <span data-ttu-id="a4f75-111">Hardware aufteilen CC-PIN (Pinname \_ Video \_ CC \_ Capture).</span><span class="sxs-lookup"><span data-stu-id="a4f75-111">Hardware slicing CC pin (PINNAME\_VIDEO\_CC\_CAPTURE).</span></span>

<span data-ttu-id="a4f75-112">Um Untertitel in der Vorschau anzuzeigen, nennen Sie [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) mit der VBI-Pin-Kategorie, und wenn dies nicht der Fall ist, nennen Sie es erneut mit der Kategorie cc.</span><span class="sxs-lookup"><span data-stu-id="a4f75-112">To preview closed captions, call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the VBI pin category, and if that fails, call it again with the CC category.</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



<span data-ttu-id="a4f75-113">Das folgende Diagramm zeigt ein typisches Filter Diagramm zum Anzeigen von Untertiteln.</span><span class="sxs-lookup"><span data-stu-id="a4f75-113">The following diagram shows a typical filter graph for displaying closed captions.</span></span>

![Vorschau Diagramm für Untertitel](images/vidcap08.png)

<span data-ttu-id="a4f75-115">In diesem Diagramm werden die folgenden Filter für die Anzeige von Closed Caption verwendet:</span><span class="sxs-lookup"><span data-stu-id="a4f75-115">This graph uses the following filters for closed caption display:</span></span>

-   <span data-ttu-id="a4f75-116">[Tee/Sink-zu-Sink-Konverter](tee-sink-to-sink-converter.md).</span><span class="sxs-lookup"><span data-stu-id="a4f75-116">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="a4f75-117">Akzeptiert die VBI-Informationen aus dem Erfassungs Filter und teilt Sie für jeden der Datendienste, die im Signal vorhanden sind, in separate Streams auf.</span><span class="sxs-lookup"><span data-stu-id="a4f75-117">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span> <span data-ttu-id="a4f75-118">Microsoft stellt VBI-Codecs für Closed Caption, nabts und World Standard Teletext (WST) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a4f75-118">Microsoft provides VBI codecs for Closed Caption, NABTS, and World Standard Teletext (WST).</span></span>
-   <span data-ttu-id="a4f75-119">[CC-Decoder](cc-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a4f75-119">[CC Decoder](cc-decoder-filter.md).</span></span> <span data-ttu-id="a4f75-120">Decodiert cc-Daten aus den vom Erfassungs Filter bereitgestellten VBI-Wellen Formularen.</span><span class="sxs-lookup"><span data-stu-id="a4f75-120">Decodes CC data from the sampled VBI waveforms provided by the capture filter.</span></span>
-   <span data-ttu-id="a4f75-121">[Zeile 21-Decoder](line-21-decoder-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a4f75-121">[Line 21 Decoder](line-21-decoder-filter.md).</span></span> <span data-ttu-id="a4f75-122">Übersetzt die CC-Byte-Paare und zeichnet den Beschriftungs Text auf Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="a4f75-122">Translates the CC byte pairs and draws the caption text onto bitmaps.</span></span> <span data-ttu-id="a4f75-123">Der Downstream-Filter (in diesem Fall der Überlagerungs-Mixer) überlagert die Bitmaps auf dem Video.</span><span class="sxs-lookup"><span data-stu-id="a4f75-123">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="a4f75-124">Die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode des Capture Graph-Generators fügt diese Filter automatisch hinzu.</span><span class="sxs-lookup"><span data-stu-id="a4f75-124">The Capture Graph Builder's [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds these filters automatically.</span></span> <span data-ttu-id="a4f75-125">Wenn der Erfassungs Filter über eine CC-Pin anstelle einer VBI-Pin verfügt, wird die CC-Pin direkt mit dem-Decoderfilter für die Linie 21 verbunden.</span><span class="sxs-lookup"><span data-stu-id="a4f75-125">If the capture filter has a CC pin instead of a VBI pin, the CC pin is connected directly to the Line 21 Decoder filter.</span></span>

> [!Note]  
> <span data-ttu-id="a4f75-126">Wenn Sie den Filter für Video Mischungs-Renderer (VMR) zum Rendern verwenden, verwenden Sie den Codierer-Filter 2.</span><span class="sxs-lookup"><span data-stu-id="a4f75-126">If you are using the Video Mixing Renderer (VMR) filter for rendering, use the Line 21 Decoder Filter 2.</span></span> <span data-ttu-id="a4f75-127">Dieser Filter verfügt über die gleiche Funktionalität wie der Line 21-Decoder, aber die CLSID ist CLSID \_ Line21Decoder2.</span><span class="sxs-lookup"><span data-stu-id="a4f75-127">This filter has the same functionality as the Line 21 Decoder, but the CLSID is CLSID\_Line21Decoder2.</span></span>

 

> [!Note]  
> <span data-ttu-id="a4f75-128">Der CC-Decoderfilter wurde in Windows Vista entfernt.</span><span class="sxs-lookup"><span data-stu-id="a4f75-128">The CC Decoder filter was removed in Windows Vista.</span></span> <span data-ttu-id="a4f75-129">Neue Anwendungen sollten den vbicodec-Filter verwenden, der in der Dokumentation zu Microsoft TV-Technologien dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="a4f75-129">New applications should use the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

 

<span data-ttu-id="a4f75-130">Wenn das Erfassungsgerät einen Videoport verwendet, hat der Erfassungs Filter möglicherweise eine Video Port-VBI-PIN (PIN- \_ Kategorie \_ Videoport \_ VBI).</span><span class="sxs-lookup"><span data-stu-id="a4f75-130">If the capture device uses a video port, the capture filter might have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="a4f75-131">Diese PIN muss mit dem [VBI-Oberflächen zuordnerfilter](vbi-surface-allocator.md) verbunden werden, der die erfassten VBI-Daten mithilfe von Oberflächen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="a4f75-131">This pin must be connected to the [VBI Surface Allocator](vbi-surface-allocator.md) filter, which allocates surfaces to hold the captured VBI data.</span></span> <span data-ttu-id="a4f75-132">Die [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) -Methode fügt diesen Filter hinzu, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a4f75-132">The [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds this filter if it is required.</span></span> <span data-ttu-id="a4f75-133">Das folgende Diagramm zeigt ein Filter Diagramm mit der VBI-Oberflächen Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="a4f75-133">The following diagram shows a filter graph with the VBI Surface Allocator.</span></span>

![Untertitel des Vorschau Diagramms mit VBI Surface-Zuweisung](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a><span data-ttu-id="a4f75-135">Aktivieren und Deaktivieren der Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="a4f75-135">Enabling and Disabling the Captions</span></span>

<span data-ttu-id="a4f75-136">Um die Untertitelanzeige zu steuern, verwenden Sie die [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) -Schnittstelle im Decoder-Filter für Linien 21.</span><span class="sxs-lookup"><span data-stu-id="a4f75-136">To control the captioning display, use the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface on the Line 21 Decoder filter.</span></span> <span data-ttu-id="a4f75-137">Beispielsweise können Sie die Beschriftungs Anzeige mithilfe der [**IAMLine21Decoder:: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) -Methode wie folgt deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="a4f75-137">For example, you can turn off the captioning display using the [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) method, as follows:</span></span>


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



<span data-ttu-id="a4f75-138">In diesem Beispiel wird die [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode verwendet, um die [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) -Schnittstelle zu suchen.</span><span class="sxs-lookup"><span data-stu-id="a4f75-138">This example uses the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface.</span></span> <span data-ttu-id="a4f75-139">Der erste Parameter für die **findinterface-Schnittstelle** ist **&\_ \_ nur** downstreamwert, der angibt, dass Downstream aus dem Erfassungs Filter (*pcap*) gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4f75-139">The first parameter to **FindInterface** is **&LOOK\_DOWNSTREAM\_ONLY**, which specifies to search downstream from the capture filter (*pCap*).</span></span>

### <a name="capturing-closed-caption-bitmaps"></a><span data-ttu-id="a4f75-140">Erfassen von Bitmaps für geschlossene Beschriftungen</span><span class="sxs-lookup"><span data-stu-id="a4f75-140">Capturing Closed Caption Bitmaps</span></span>

<span data-ttu-id="a4f75-141">Sie können die Beschriftungs Bitmaps in einer Datei erfassen.</span><span class="sxs-lookup"><span data-stu-id="a4f75-141">You can capture the caption bitmaps into a file.</span></span> <span data-ttu-id="a4f75-142">Fügen Sie hierzu den Abschnitt zum Schreiben von Dateien des Filter Diagramms hinzu, wie unter [Erfassen von Videos in einer Datei](capturing-video-to-a-file.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a4f75-142">To do so, add the file-writing section of the filter graph, as described in [Capturing Video to a File](capturing-video-to-a-file.md).</span></span> <span data-ttu-id="a4f75-143">Anschließend können Sie die CC-oder VBI-PIN mit dem MUX-Filter Rendering:</span><span class="sxs-lookup"><span data-stu-id="a4f75-143">Then render the CC or VBI pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



<span data-ttu-id="a4f75-144">Wenn Sie auch das Video erfassen, wird eine Datei mit zwei separaten Videostreams erstellt.</span><span class="sxs-lookup"><span data-stu-id="a4f75-144">If you are also capturing the video, this will create a file with two separate video streams.</span></span> <span data-ttu-id="a4f75-145">Videos mit Beschriftungen, die oberhalb des Bilds überlagert sind, werden nicht erfasst.</span><span class="sxs-lookup"><span data-stu-id="a4f75-145">It will not capture video with captions overlaid on top of the picture.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4f75-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a4f75-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4f75-147">Untertitel und Teletext</span><span class="sxs-lookup"><span data-stu-id="a4f75-147">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



