---
description: VBI Surface Allocator
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: VBI Surface Allocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909008"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="ed6a8-103">VBI Surface Allocator</span><span class="sxs-lookup"><span data-stu-id="ed6a8-103">VBI Surface Allocator</span></span>

<span data-ttu-id="ed6a8-104">Der VBI Surface Allocator steuert die Zuordnung von VBI-Puffern in analogen Fernsehgraphen mit Hardwarevideoporterfassungsszenarien.</span><span class="sxs-lookup"><span data-stu-id="ed6a8-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="ed6a8-105">Bei Geräten wie dem Bt829-Decoder kann der Framepuffer mehrere VBI-Erfassungspuffer enthalten, auf die über einen proprietären hardwarebasierten Mechanismus zugegriffen wird, der allgemein als Videoport bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="ed6a8-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="ed6a8-106">Der VBI Surface Allocator-Filter verbindet downstream vom Erfassungsfilter und verfügt über keinen Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="ed6a8-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="ed6a8-107">Der Filter arbeitet eng mit dem [Overlay-Mixer](overlay-mixer-filter.md) (über DirectDraw) zusammen, um koordinierte Vorgänge am Hardwarevideoport durchzuführen, wobei der gleiche eingeschränkte SVGA-Framepufferspeicher genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="ed6a8-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



| <span data-ttu-id="ed6a8-108">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="ed6a8-108">Label</span></span> | <span data-ttu-id="ed6a8-109">Wert</span><span class="sxs-lookup"><span data-stu-id="ed6a8-109">Value</span></span> |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed6a8-110">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="ed6a8-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="ed6a8-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="ed6a8-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="ed6a8-112">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="ed6a8-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="ed6a8-113">MEDIATYPE \_ Video, MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="ed6a8-113">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="ed6a8-114">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ed6a8-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="ed6a8-115">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="ed6a8-115">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="ed6a8-116">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="ed6a8-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="ed6a8-117">MEDIATYPE \_ NULL, MEDIASUBTYPE \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="ed6a8-117">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="ed6a8-118">(Nichts ist jemals mit dem Ausgabepin verbunden.)</span><span class="sxs-lookup"><span data-stu-id="ed6a8-118">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="ed6a8-119">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ed6a8-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="ed6a8-120">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ed6a8-120">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="ed6a8-121">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="ed6a8-121">Filter CLSID</span></span>                             | <span data-ttu-id="ed6a8-122">CLSID \_ VBISurfaces</span><span class="sxs-lookup"><span data-stu-id="ed6a8-122">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="ed6a8-123">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="ed6a8-123">Property Page CLSID</span></span>                      | <span data-ttu-id="ed6a8-124">Keine Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="ed6a8-124">No property page.</span></span>                                                                   |
| <span data-ttu-id="ed6a8-125">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="ed6a8-125">Executable</span></span>                               | <span data-ttu-id="ed6a8-126">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="ed6a8-126">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="ed6a8-127">Verdienst</span><span class="sxs-lookup"><span data-stu-id="ed6a8-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="ed6a8-128">MERIT \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="ed6a8-128">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="ed6a8-129">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="ed6a8-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ed6a8-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ed6a8-130">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="ed6a8-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed6a8-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed6a8-132">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="ed6a8-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



