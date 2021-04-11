---
description: Verwenden des Overlay-Mischers bei der Video Erfassung
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Verwenden des Overlay-Mischers bei der Video Erfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042559"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a><span data-ttu-id="ca2ca-103">Verwenden des Overlay-Mischers bei der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="ca2ca-103">Using the Overlay Mixer in Video Capture</span></span>

<span data-ttu-id="ca2ca-104">Es gibt bestimmte Arten von Videos, die der [Videorenderer](video-renderer-filter.md) -Filter nicht Selbstanzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-104">There are certain kinds of video that the [Video Renderer](video-renderer-filter.md) filter cannot display by itself.</span></span> <span data-ttu-id="ca2ca-105">In diesen Fällen muss der Videorenderer mit dem [Überlagerungs-Mischungs](overlay-mixer-filter.md) Filter arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-105">In these situations, the Video Renderer must work with the [Overlay Mixer](overlay-mixer-filter.md) filter.</span></span> <span data-ttu-id="ca2ca-106">Der Überlagerungs-Mixer verwaltet das Rendering, während der Videorenderer das Videofenster verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-106">The Overlay Mixer manages the rendering, while the Video Renderer manages the video window.</span></span> <span data-ttu-id="ca2ca-107">Der Überlagerungs Mixer ist in den folgenden Situationen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="ca2ca-107">The Overlay Mixer is needed in the following situations:</span></span>

-   <span data-ttu-id="ca2ca-108">"Videoport"-Pins (VP).</span><span class="sxs-lookup"><span data-stu-id="ca2ca-108">Video port (VP) pins.</span></span> <span data-ttu-id="ca2ca-109">Wenn das Erfassungsgerät einen Videoport verwendet, verwaltet der Überlagerungs Mixer die Hardware Überlagerung.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-109">If the capture device uses a video port, the Overlay Mixer manages the hardware overlay.</span></span>
-   <span data-ttu-id="ca2ca-110">Video mit Zeilen Sprung.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-110">Interlaced video.</span></span> <span data-ttu-id="ca2ca-111">Für ein Zeilen Sprung Video benötigt der Decoder ein [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format, das der Videorenderer nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-111">For interlaced video, the decoder requires a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format, which the Video Renderer does not support.</span></span>
-   <span data-ttu-id="ca2ca-112">Untertitel.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-112">Closed captions.</span></span> <span data-ttu-id="ca2ca-113">Der Beschriftungs Text wird als 8-Bit-pro-Pixel-Bitmaps gerendert, das der Überlagerungs-Mixer auf das Video überlagert.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-113">The caption text is rendered as 8-bits-per-pixel bitmaps, which the Overlay Mixer overlays onto the video.</span></span>

<span data-ttu-id="ca2ca-114">Die **RenderStream** -Methode des Capture Graph-Generators fügt den Überlagerungs-Mixer bei Bedarf ein.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-114">The Capture Graph Builder's **RenderStream** method inserts the Overlay Mixer whenever needed.</span></span> <span data-ttu-id="ca2ca-115">Wenn Sie das Diagramm erstellen, ohne den Erfassungs Diagramm-Generator zu verwenden, müssen Sie jedoch jede dieser Situationen überprüfen und den Überlagerungs Mixer selbst einfügen.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-115">If you are building the graph without using the Capture Graph Builder, however, you must check for each of these situations and insert the Overlay Mixer yourself.</span></span>

-   <span data-ttu-id="ca2ca-116">\[! Wichtig\]</span><span class="sxs-lookup"><span data-stu-id="ca2ca-116">\[!Important\]</span></span>  
    > <span data-ttu-id="ca2ca-117">Wenn das Gerät über eine VP-Pin verfügt, müssen Sie den Überlagerungs-Mixer auch dann verbinden, wenn Sie in Ihrer Anwendung keine Vorschau Funktionalität benötigen.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-117">If the device has a VP pin, you must connect the Overlay Mixer even if you do not need preview functionality in your application.</span></span> <span data-ttu-id="ca2ca-118">Mit einem Videoport sendet das Erfassungsgerät die Videodaten immer an die Hardware Überlagerung, sodass der Überlagerungs Mixer immer benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-118">With a video port, the capture device always sends the video data to the hardware overlay, so the Overlay Mixer is always needed.</span></span>

     

<span data-ttu-id="ca2ca-119">Die videomischungs-rendererfilter (VMR-7 und VMR-9) unterstützen beide Zeilen Sprung Videos und können geschlossene Beschriftungs Bitmaps in das primäre Video mischen.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-119">The Video Mixing Renderer filters (VMR-7 and VMR-9) both support interlaced video, and are able to mix closed caption bitmaps onto the primary video.</span></span> <span data-ttu-id="ca2ca-120">Wenn Sie den VMR für diese Szenarien verwenden, müssen Sie den Überlagerungs-Mixer nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-120">If you are using the VMR for those scenarios, then you do not need to use the Overlay Mixer.</span></span> <span data-ttu-id="ca2ca-121">VMR-9 unterstützt keine VP-Pin-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-121">The VMR-9 does not support VP pin connections.</span></span> <span data-ttu-id="ca2ca-122">VMR-7 unterstützt VP-Pin-Verbindungen über den Video Port-Manager-Filter.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-122">The VMR-7 supports VP pin connections through the Video Port Manager filter.</span></span> <span data-ttu-id="ca2ca-123">Allerdings können Sie feststellen, dass einige Treiber nicht ordnungsgemäß mit dem Videoport-Manager funktionieren.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-123">However, you may find that some drivers do not work correctly with the Video Port Manager.</span></span> <span data-ttu-id="ca2ca-124">Aus diesem Grund wird der Überlagerungs Mixer weiterhin für VP Pins empfohlen.</span><span class="sxs-lookup"><span data-stu-id="ca2ca-124">For that reason, the Overlay Mixer is still recommended for VP pins.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca2ca-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ca2ca-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca2ca-126">Erweiterte Erfassungs Themen</span><span class="sxs-lookup"><span data-stu-id="ca2ca-126">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="ca2ca-127">VideoPort-Pins</span><span class="sxs-lookup"><span data-stu-id="ca2ca-127">Video Port Pins</span></span>](video-port-pins.md)
</dt> <dt>

[<span data-ttu-id="ca2ca-128">VideoInfo2-Formattyp</span><span class="sxs-lookup"><span data-stu-id="ca2ca-128">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
</dt> </dl>

 

 



