---
description: VBI-Oberflächen Zuweisung
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: VBI-Oberflächen Zuweisung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4edd698ed37c7b180bee27d0a99e95096080d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757675"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="77a20-103">VBI-Oberflächen Zuweisung</span><span class="sxs-lookup"><span data-stu-id="77a20-103">VBI Surface Allocator</span></span>

<span data-ttu-id="77a20-104">Der VBI Surface Allocator steuert die Zuordnung von VBI-Puffern in analogen Fernseh Diagrammen mit hardwareporterfassungs-Szenarios.</span><span class="sxs-lookup"><span data-stu-id="77a20-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="77a20-105">Bei Geräten wie dem Bt829-Decoder kann der Frame Puffer mehrere VBI-Aufzeichnungs Puffer enthalten, auf die über einen proprietären hardwarebasierten Mechanismus zugegriffen wird, der generisch als Videoport bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="77a20-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="77a20-106">Der VBI-Oberflächen Zuordnungsfilter stellt eine Downstreamverbindung mit dem Erfassungs Filter her und hat keine Ausgabe-PIN</span><span class="sxs-lookup"><span data-stu-id="77a20-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="77a20-107">Der Filter arbeitet eng mit dem [Überlagerungs-Mixer](overlay-mixer-filter.md) (über DirectDraw) zusammen, um koordinierte Vorgänge auf dem Hardwareport durchzuführen, wobei der gleiche beschränkte SVGA-Frame Puffer Arbeitsspeicher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="77a20-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



|                                          |                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="77a20-108">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="77a20-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="77a20-109">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="77a20-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="77a20-110">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="77a20-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="77a20-111">MediaType- \_ Video, mediasubtype \_ vpvbi</span><span class="sxs-lookup"><span data-stu-id="77a20-111">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="77a20-112">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="77a20-112">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="77a20-113">**"Ikspropertyset"**</span><span class="sxs-lookup"><span data-stu-id="77a20-113">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="77a20-114">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="77a20-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="77a20-115">MediaType \_ NULL, mediasubtype \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="77a20-115">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="77a20-116">(Nichts ist jemals mit der Ausgabe-PIN verbunden.)</span><span class="sxs-lookup"><span data-stu-id="77a20-116">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="77a20-117">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="77a20-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="77a20-118">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="77a20-118">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="77a20-119">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="77a20-119">Filter CLSID</span></span>                             | <span data-ttu-id="77a20-120">CLSID- \_ vbioberflächen</span><span class="sxs-lookup"><span data-stu-id="77a20-120">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="77a20-121">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="77a20-121">Property Page CLSID</span></span>                      | <span data-ttu-id="77a20-122">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="77a20-122">No property page.</span></span>                                                                   |
| <span data-ttu-id="77a20-123">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="77a20-123">Executable</span></span>                               | <span data-ttu-id="77a20-124">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="77a20-124">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="77a20-125">Verdienst</span><span class="sxs-lookup"><span data-stu-id="77a20-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="77a20-126">Verdienst \_ Normal</span><span class="sxs-lookup"><span data-stu-id="77a20-126">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="77a20-127">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="77a20-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="77a20-128">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="77a20-128">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="77a20-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77a20-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77a20-130">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="77a20-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



