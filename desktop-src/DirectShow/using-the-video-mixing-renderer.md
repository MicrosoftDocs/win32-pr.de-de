---
description: Verwenden des Video Mischungs Renderers
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Verwenden des Video Mischungs Renderers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359147"
---
# <a name="using-the-video-mixing-renderer"></a><span data-ttu-id="2d471-103">Verwenden des Video Mischungs Renderers</span><span class="sxs-lookup"><span data-stu-id="2d471-103">Using the Video Mixing Renderer</span></span>

<span data-ttu-id="2d471-104">Im Hinblick auf die Leistung und die Vielzahl der Features stellt der Filter für Video Mischungs Renderer (VMR) die nächste Generation im Video Rendering auf der Windows-Plattform dar.</span><span class="sxs-lookup"><span data-stu-id="2d471-104">In terms of both performance and breadth of features, the Video Mixing Renderer (VMR) filter represents the next generation in video rendering on the Windows platform.</span></span> <span data-ttu-id="2d471-105">VMR ersetzt den [Überlagerungs Mixer](overlay-mixer-filter.md) und den [Videorenderer](video-renderer-filter.md)und fügt viele neue Mischungs Funktionen hinzu.</span><span class="sxs-lookup"><span data-stu-id="2d471-105">The VMR replaces the [Overlay Mixer](overlay-mixer-filter.md) and [Video Renderer](video-renderer-filter.md), and adds many new mixing features.</span></span>

<span data-ttu-id="2d471-106">Es gibt zwei Versionen von VMR:</span><span class="sxs-lookup"><span data-stu-id="2d471-106">There are two versions of the VMR:</span></span>

-   <span data-ttu-id="2d471-107">Die VMR-7, die DirectDraw 7 zum Rendern verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d471-107">The VMR-7, which uses DirectDraw 7 for rendering.</span></span>
-   <span data-ttu-id="2d471-108">VMR-9, das Direct3D 9 verwendet.</span><span class="sxs-lookup"><span data-stu-id="2d471-108">The VMR-9, which uses Direct3D 9.</span></span>

<span data-ttu-id="2d471-109">VMR-7 ist unter Windows XP und höher verfügbar, aber nicht für die erneute Verteilung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2d471-109">The VMR-7 is available on Windows XP and later, but is not available for redistribution.</span></span> <span data-ttu-id="2d471-110">VMR-9 ist für die Weiterverteilung auf allen Plattformen verfügbar, die von DirectX 9 unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="2d471-110">The VMR-9 is available for redistribution on all platforms supported by DirectX 9.</span></span> <span data-ttu-id="2d471-111">Die beiden VMR-Filter sind in ihrer Implementierung und den von Ihnen bereitgestellten Schnittstellen sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="2d471-111">The two VMR filters are very similar in their implementation and the interfaces that they expose.</span></span>

<span data-ttu-id="2d471-112">VMR-9 hat eine eigene CLSID und einen eigenen Satz von Schnittstellen, Strukturen und Enumerationstypen, die nicht immer mit den entsprechenden Datentypen für VMR-7 identisch sind, aufgrund der zugrunde liegenden Unterschiede zwischen DirectDraw 7 und Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="2d471-112">The VMR-9 has its own CLSID and its own set of interfaces, structures and enumeration types which are not always identical to the corresponding data types for the VMR-7, due to the underlying differences between DirectDraw 7 and Direct3D 9.</span></span> <span data-ttu-id="2d471-113">Die VMR-9-Schnittstellen enden alle mit "9", z. b. **IVMRStreamConfig9**, und die Strukturen und Enumerationstypen verfügen in Ihrem Namen über "VMR9", um Sie von den Datentypen zu unterscheiden, die mit VMR-7 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2d471-113">The VMR-9 interfaces all end with "9", for example **IVMRStreamConfig9**, and the structures and enumeration types all have "VMR9" in their name to distinguish them from the data types used with the VMR-7.</span></span>

<span data-ttu-id="2d471-114">Um Abwärtskompatibilität zu gewährleisten, ist VMR-9 nicht der Standard-Renderer auf einem System.</span><span class="sxs-lookup"><span data-stu-id="2d471-114">To ensure backward-compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="2d471-115">Um VMR-9 verwenden zu können, müssen Sie es mithilfe der [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) -Methode explizit dem Filter Diagramm hinzufügen und konfigurieren, bevor Sie es mit upstreamfiltern verbinden.</span><span class="sxs-lookup"><span data-stu-id="2d471-115">To use the VMR-9, you must explicitly add it to the filter graph using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method, and configure it before connecting it to any upstream filters.</span></span>

<span data-ttu-id="2d471-116">Dieser Artikel enthält folgende Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="2d471-116">This article contains the following sections.</span></span> <span data-ttu-id="2d471-117">Sofern nicht angegeben, gelten die Informationen in diesen Abschnitten sowohl für den VMR-7-als auch für den VMR-9-Filter.</span><span class="sxs-lookup"><span data-stu-id="2d471-117">Except where noted, the information in these sections applies to both the VMR-7 and the VMR-9 filters.</span></span>

-   [<span data-ttu-id="2d471-118">Informationen zum Video Mischungs Rendering</span><span class="sxs-lookup"><span data-stu-id="2d471-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
-   [<span data-ttu-id="2d471-119">VMR-Betriebsmodi</span><span class="sxs-lookup"><span data-stu-id="2d471-119">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
-   [<span data-ttu-id="2d471-120">Aufbauen eines VMR-9-Filter Diagramms</span><span class="sxs-lookup"><span data-stu-id="2d471-120">Building a VMR-9 Filter Graph</span></span>](building-a-vmr-9-filter-graph.md)
-   [<span data-ttu-id="2d471-121">Verwenden des VMR-Mischungs Modus</span><span class="sxs-lookup"><span data-stu-id="2d471-121">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
-   [<span data-ttu-id="2d471-122">Einstellungen für deinterlace werden festgelegt</span><span class="sxs-lookup"><span data-stu-id="2d471-122">Setting Deinterlace Preferences</span></span>](setting-deinterlace-preferences.md)
-   [<span data-ttu-id="2d471-123">Verwenden von VMR für DirectShow-Filter Entwickler</span><span class="sxs-lookup"><span data-stu-id="2d471-123">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
-   [<span data-ttu-id="2d471-124">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="2d471-124">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a><span data-ttu-id="2d471-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d471-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d471-126">Video Mischungs-Renderer Filter 7</span><span class="sxs-lookup"><span data-stu-id="2d471-126">Video Mixing Renderer Filter 7</span></span>](video-mixing-renderer-filter-7.md)
</dt> <dt>

[<span data-ttu-id="2d471-127">Video Mischungs-Renderer Filter 9</span><span class="sxs-lookup"><span data-stu-id="2d471-127">Video Mixing Renderer Filter 9</span></span>](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



