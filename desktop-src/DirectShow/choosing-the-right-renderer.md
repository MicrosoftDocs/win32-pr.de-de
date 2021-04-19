---
description: Auswählen des richtigen Videorenderers
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Auswählen des richtigen Videorenderers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346207"
---
# <a name="choosing-the-right-video-renderer"></a><span data-ttu-id="01533-103">Auswählen des richtigen Videorenderers</span><span class="sxs-lookup"><span data-stu-id="01533-103">Choosing the Right Video Renderer</span></span>

<span data-ttu-id="01533-104">DirectShow stellt verschiedene Videorendererfilter bereit, die in der folgenden Tabelle zusammengefasst sind.</span><span class="sxs-lookup"><span data-stu-id="01533-104">DirectShow provides several video renderer filters, summarized in the following table.</span></span>



| <span data-ttu-id="01533-105">Filter</span><span class="sxs-lookup"><span data-stu-id="01533-105">Filter</span></span>                                                                  | <span data-ttu-id="01533-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01533-106">Remarks</span></span>                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="01533-107">[**Erweiterter Videorenderer**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="01533-107">[**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR)</span></span> | <span data-ttu-id="01533-108">Verwendet Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="01533-108">Uses Direct3D 9.</span></span> <span data-ttu-id="01533-109">Erfordert Windows Vista oder höher.</span><span class="sxs-lookup"><span data-stu-id="01533-109">Requires Windows Vista or later.</span></span> |
| <span data-ttu-id="01533-110">[Video Mischungs-Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="01533-110">[Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>   | <span data-ttu-id="01533-111">Verwendet Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="01533-111">Uses Direct3D 9.</span></span> <span data-ttu-id="01533-112">Erfordert Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="01533-112">Requires Windows XP or later.</span></span>    |
| <span data-ttu-id="01533-113">[Video Mischungs Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="01533-113">[Video Mixing Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>     | <span data-ttu-id="01533-114">Verwendet DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="01533-114">Uses DirectDraw.</span></span> <span data-ttu-id="01533-115">Erfordert Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="01533-115">Requires Windows XP or later.</span></span>    |
| [<span data-ttu-id="01533-116">Überlagerungs Mixer</span><span class="sxs-lookup"><span data-stu-id="01533-116">Overlay Mixer</span></span>](using-the-overlay-mixer-in-video-capture.md)           | <span data-ttu-id="01533-117">Unterstützt Hardware Überlagerungen durch DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="01533-117">Supports hardware overlays through DirectDraw.</span></span>    |
| <span data-ttu-id="01533-118">Der Legacy- [Videorenderer](video-renderer-filter.md) -Filter.</span><span class="sxs-lookup"><span data-stu-id="01533-118">Legacy [Video Renderer](video-renderer-filter.md) filter.</span></span>              | <span data-ttu-id="01533-119">Verwendet DirectDraw oder (selten) GDI</span><span class="sxs-lookup"><span data-stu-id="01533-119">Uses DirectDraw or (rarely) GDI</span></span>                   |



 

<span data-ttu-id="01533-120">Welcher Renderer verwendet werden soll, hängt größtenteils davon ab, welche Versionen von Windows unterstützt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="01533-120">Which renderer to use depends largely on which versions of Windows you need to support.</span></span>

-   <span data-ttu-id="01533-121">In Windows Vista und höher sollten Anwendungen den EVR verwenden, wenn Sie von der Hardware unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="01533-121">In Windows Vista and later, applications should use the EVR if the hardware supports it.</span></span> <span data-ttu-id="01533-122">Andernfalls greifen Sie auf VMR-9 oder VMR-7 zurück.</span><span class="sxs-lookup"><span data-stu-id="01533-122">Otherwise, fall back to the VMR-9 or VMR-7.</span></span> <span data-ttu-id="01533-123">Der EVR bietet eine bessere Leistung und bessere Videoqualität als vorherige Renderer.</span><span class="sxs-lookup"><span data-stu-id="01533-123">The EVR offers better performance and better video quality than previous renderers.</span></span> <span data-ttu-id="01533-124">Außerdem ist er für die Verwendung mit dem Desktopfenster-Manager (DWM) konzipiert.</span><span class="sxs-lookup"><span data-stu-id="01533-124">Also, it is designed to work with the Desktop Window Manager (DWM).</span></span>
-   <span data-ttu-id="01533-125">Verwenden Sie vor Windows Vista VMR-9, wenn dies von der Hardware unterstützt wird und keine Video Port Funktionen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="01533-125">Prior to Windows Vista, use the VMR-9 if the hardware supports it and video port functionality is not required.</span></span> <span data-ttu-id="01533-126">Verwenden Sie andernfalls VMR-7.</span><span class="sxs-lookup"><span data-stu-id="01533-126">Otherwise, use the VMR-7.</span></span>
-   <span data-ttu-id="01533-127">Auf älteren Systemen müssen Sie möglicherweise den Overlay-Mixer (für den Videoport oder die Unterstützung der Hardware Überlagerung) oder den Legacy-Videorendererfilter verwenden.</span><span class="sxs-lookup"><span data-stu-id="01533-127">On older systems, you might need to use the Overlay Mixer (for video port or hardware overlay support) or the legacy Video Renderer filter.</span></span>

<span data-ttu-id="01533-128">Die [**igraphbuilder:: Rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) -Methode und die [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) -Methode verwenden standardmäßig VMR-7.</span><span class="sxs-lookup"><span data-stu-id="01533-128">The [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) and [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) methods use the VMR-7 by default.</span></span> <span data-ttu-id="01533-129">Wenn die Hardware VMR-7 nicht unterstützt, greifen diese Methoden auf den Legacy-Videorendererfilter zurück.</span><span class="sxs-lookup"><span data-stu-id="01533-129">If the hardware does not support the VMR-7, these methods fall back to the legacy Video Renderer filter.</span></span> <span data-ttu-id="01533-130">Der EVR und VMR-9 sind nie die Standardrenderer.</span><span class="sxs-lookup"><span data-stu-id="01533-130">The EVR and VMR-9 are never the default renderers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01533-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="01533-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01533-132">Videorendering</span><span class="sxs-lookup"><span data-stu-id="01533-132">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



