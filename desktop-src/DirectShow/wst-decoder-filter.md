---
description: WST-Decoderfilter
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: WST-Decoderfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f2d20873ff9a5e7c009c4a84f7a23c273d6590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863383"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="26f17-103">WST-Decoderfilter</span><span class="sxs-lookup"><span data-stu-id="26f17-103">WST Decoder Filter</span></span>

<span data-ttu-id="26f17-104">Diese Komponente wurde aus Windows Vista und höheren Betriebssystemen entfernt.</span><span class="sxs-lookup"><span data-stu-id="26f17-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="26f17-105">Es ist für die Verwendung in den Betriebssystemen Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="26f17-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="26f17-106">Ab Windows Vista bietet DirectShow keinen Filter zum Decodieren von "World Standard Teletext (WST)".</span><span class="sxs-lookup"><span data-stu-id="26f17-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="26f17-107">Der WST-Decoder ist ein kernelmodusfilter, der decodierte World Standard-Teletextdaten aus dem [WST-Codec](wst-codec-filter.md) akzeptiert und die Bitmaps mit den von Microsoft bereitgestellten Schriftarten an Pin 2 auf dem [Overlay-Mixer](overlay-mixer-filter.md) übergibt.</span><span class="sxs-lookup"><span data-stu-id="26f17-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="26f17-108">Zurzeit werden nur westeuropäische Sprachen unterstützt. Zurzeit werden keine Unicode-Schriftarten bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="26f17-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="26f17-109">Dieser Filter kann durch Aufrufen von [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)mithilfe der Ausgabe-PIN des WST-Codecs automatisch dem Diagramm hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="26f17-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



|                                          |                                                               |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="26f17-110">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="26f17-110">Filter Interfaces</span></span>                        | <span data-ttu-id="26f17-111">ISpecifyPropertyPages, [ **iamwstdecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="26f17-111">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="26f17-112">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="26f17-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="26f17-113">MediaType \_ VBI, mediasubtype \_ Teletext</span><span class="sxs-lookup"><span data-stu-id="26f17-113">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="26f17-114">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="26f17-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="26f17-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="26f17-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="26f17-116">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="26f17-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="26f17-117">MediaType- \_ Video</span><span class="sxs-lookup"><span data-stu-id="26f17-117">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="26f17-118">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="26f17-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="26f17-119">**IPin**</span><span class="sxs-lookup"><span data-stu-id="26f17-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="26f17-120">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="26f17-120">Filter CLSID</span></span>                             | <span data-ttu-id="26f17-121">CLSID- \_ wstdecoder</span><span class="sxs-lookup"><span data-stu-id="26f17-121">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="26f17-122">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="26f17-122">Property Page CLSID</span></span>                      | <span data-ttu-id="26f17-123">CLSID \_ wstdecoderpropertypage</span><span class="sxs-lookup"><span data-stu-id="26f17-123">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="26f17-124">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="26f17-124">Executable</span></span>                               | <span data-ttu-id="26f17-125">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="26f17-125">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="26f17-126">Verdienst</span><span class="sxs-lookup"><span data-stu-id="26f17-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="26f17-127">Verdienst \_ Normal</span><span class="sxs-lookup"><span data-stu-id="26f17-127">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="26f17-128">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="26f17-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="26f17-129">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="26f17-129">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="26f17-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26f17-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26f17-131">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="26f17-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="26f17-132">Anzeigen von World Standard-Teletext</span><span class="sxs-lookup"><span data-stu-id="26f17-132">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



