---
description: WST-Decoderfilter
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: WST-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908478"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="92f60-103">WST-Decoderfilter</span><span class="sxs-lookup"><span data-stu-id="92f60-103">WST Decoder Filter</span></span>

<span data-ttu-id="92f60-104">Diese Komponente wurde aus Windows Vista und späteren Betriebssystemen entfernt.</span><span class="sxs-lookup"><span data-stu-id="92f60-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="92f60-105">Es ist für die Verwendung in den Betriebssystemen Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92f60-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="92f60-106">Ab Windows Vista stellt DirectShow keinen Filter zum Decodieren von World Standard Teletext (WST) bereit.</span><span class="sxs-lookup"><span data-stu-id="92f60-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="92f60-107">Der WST-Decoder ist ein Kernelmodusfilter, der decodierte World Standard Teletext-Daten vom [WST-Codec](wst-codec-filter.md) akzeptiert und die Bitmaps mit von Microsoft bereitgestellten Schriftarten an Pin 2 auf dem [Overlay-Mixer](overlay-mixer-filter.md) übermittelt.</span><span class="sxs-lookup"><span data-stu-id="92f60-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="92f60-108">Derzeit werden nur westepäische Sprachen unterstützt. Derzeit werden keine Unicode-Schriftarten bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="92f60-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="92f60-109">Dieser Filter kann dem Graphen automatisch hinzugefügt werden, indem [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)mithilfe des Ausgabepins des WST-Codecs aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="92f60-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



| <span data-ttu-id="92f60-110">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="92f60-110">Label</span></span> | <span data-ttu-id="92f60-111">Wert</span><span class="sxs-lookup"><span data-stu-id="92f60-111">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="92f60-112">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="92f60-112">Filter Interfaces</span></span>                        | <span data-ttu-id="92f60-113">ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="92f60-113">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="92f60-114">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="92f60-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="92f60-115">MEDIATYPE \_ VBI, MEDIASUBTYPE \_ TELETEXT</span><span class="sxs-lookup"><span data-stu-id="92f60-115">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="92f60-116">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="92f60-116">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="92f60-117">**Ipin**</span><span class="sxs-lookup"><span data-stu-id="92f60-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="92f60-118">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="92f60-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="92f60-119">\_MEDIATYPE-Video</span><span class="sxs-lookup"><span data-stu-id="92f60-119">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="92f60-120">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="92f60-120">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="92f60-121">**Ipin**</span><span class="sxs-lookup"><span data-stu-id="92f60-121">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="92f60-122">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="92f60-122">Filter CLSID</span></span>                             | <span data-ttu-id="92f60-123">CLSID \_ WSTDecoder</span><span class="sxs-lookup"><span data-stu-id="92f60-123">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="92f60-124">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="92f60-124">Property Page CLSID</span></span>                      | <span data-ttu-id="92f60-125">CLSID \_ WstDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="92f60-125">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="92f60-126">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="92f60-126">Executable</span></span>                               | <span data-ttu-id="92f60-127">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="92f60-127">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="92f60-128">Verdienst</span><span class="sxs-lookup"><span data-stu-id="92f60-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="92f60-129">MERIT \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="92f60-129">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="92f60-130">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="92f60-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="92f60-131">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="92f60-131">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="92f60-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="92f60-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92f60-133">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="92f60-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="92f60-134">Viewing World Standard Teletext</span><span class="sxs-lookup"><span data-stu-id="92f60-134">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



