---
description: AVI-Dekomprimierungsfilter
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: AVI-Dekomprimierungsfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214ccfeee18a01fa9c8d52ffbf4593b9de5664bb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910098"
---
# <a name="avi-decompressor-filter"></a><span data-ttu-id="688d7-103">AVI-Dekomprimierungsfilter</span><span class="sxs-lookup"><span data-stu-id="688d7-103">AVI Decompressor Filter</span></span>

<span data-ttu-id="688d7-104">Der FILTER FÜR DEN AVI-Dekomprimierungsfilter ermöglicht videokomprimierungs-Manager-Codecs (VCM), um einen Filtergraphen zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="688d7-104">The AVI Decompressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="688d7-105">Die Anwendung muss den Filter nicht dem Filterdiagramm hinzufügen. Sie wird bei Bedarf automatisch vom Filtergraph-Manager eingezogen.</span><span class="sxs-lookup"><span data-stu-id="688d7-105">The application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span>

<span data-ttu-id="688d7-106">Wenn der Filter graph Manager ein Diagramm zum Rendern einer AVI-Datei aufbaut, überprüft er fourcc im AVI-Header der Datei, um zu bestimmen, ob der Videostream komprimiert ist.</span><span class="sxs-lookup"><span data-stu-id="688d7-106">When the Filter Graph Manager is building a graph to render an AVI file, it checks the FOURCC in the file's AVI header to determine whether the video stream is compressed.</span></span> <span data-ttu-id="688d7-107">In diesem Beispiel fügt der Filter graph-Manager den AVI-Dekomprimor hinzu, der dann in der Registrierung nach einem installierten Dekomprimator sucht, der die Datei verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="688d7-107">If it is, the Filter Graph Manager adds the AVI Decompressor, which then searches the registry for an installed decompressor that can handle the file.</span></span>

> [!Note]  
> <span data-ttu-id="688d7-108">MPEG-Dekomprimierungen werden nie als VCM-Codecs implementiert, sondern nur als native DirectShow-Filter.</span><span class="sxs-lookup"><span data-stu-id="688d7-108">MPEG decompressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 

<span data-ttu-id="688d7-109">An seinem Upstreampin stellt der AVI-Dekomprimator in der Regel eine Verbindung mit dem [AVI-Splitter () auf.](avi-splitter-filter.md)</span><span class="sxs-lookup"><span data-stu-id="688d7-109">On its upstream pin the AVI Decompressor typically connects to the [AVI Splitter](avi-splitter-filter.md).</span></span> <span data-ttu-id="688d7-110">Auf dem Ausgabepin wird in der Regel eine Verbindung mit dem [Videorenderer](video-renderer-filter.md) oder [dem AVI Mux Filter -Filter herstellt.](avi-mux-filter.md)</span><span class="sxs-lookup"><span data-stu-id="688d7-110">On its output pin it typically connects to the [Video Renderer](video-renderer-filter.md) or the [AVI Mux Filter](avi-mux-filter.md).</span></span>



| <span data-ttu-id="688d7-111">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="688d7-111">Label</span></span> | <span data-ttu-id="688d7-112">Wert</span><span class="sxs-lookup"><span data-stu-id="688d7-112">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="688d7-113">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="688d7-113">Filter Interfaces</span></span>                        | [<span data-ttu-id="688d7-114">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="688d7-114">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| <span data-ttu-id="688d7-115">Eingabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="688d7-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="688d7-116">Haupttyp: MEDIATYPE \_ VideoSubtype: Muss dem FOURCC-Code für den Komprimierungstyp entsprechen.</span><span class="sxs-lookup"><span data-stu-id="688d7-116">Major type: MEDIATYPE\_VideoSubtype: Must correspond to the FOURCC code for the compression type.</span></span> <span data-ttu-id="688d7-117">Weitere Informationen finden Sie unter [FOURCC Codes](fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="688d7-117">For more information, see [FOURCC Codes](fourcc-codes.md).</span></span><br/> <span data-ttu-id="688d7-118">Formattyp: FORMAT \_ VideoInfo</span><span class="sxs-lookup"><span data-stu-id="688d7-118">Format type: FORMAT\_VideoInfo</span></span><br/> |
| <span data-ttu-id="688d7-119">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="688d7-119">Input Pin Interfaces</span></span>                     | <span data-ttu-id="688d7-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="688d7-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                             |
| <span data-ttu-id="688d7-121">Ausgabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="688d7-121">Output Pin Media Types</span></span>                   | <span data-ttu-id="688d7-122">MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL, FORMAT \_ VideoInfo</span><span class="sxs-lookup"><span data-stu-id="688d7-122">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL, FORMAT\_VideoInfo</span></span>                                                                                                                                                            |
| <span data-ttu-id="688d7-123">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="688d7-123">Output Pin Interfaces</span></span>                    | <span data-ttu-id="688d7-124">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="688d7-124">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                 |
| <span data-ttu-id="688d7-125">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="688d7-125">Filter CLSID</span></span>                             | <span data-ttu-id="688d7-126">CLSID \_ AVIDec</span><span class="sxs-lookup"><span data-stu-id="688d7-126">CLSID\_AVIDec</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="688d7-127">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="688d7-127">Property Page CLSID</span></span>                      | <span data-ttu-id="688d7-128">Keine Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="688d7-128">No property page.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="688d7-129">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="688d7-129">Executable</span></span>                               | <span data-ttu-id="688d7-130">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="688d7-130">quartz.dll</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="688d7-131">Verdienst</span><span class="sxs-lookup"><span data-stu-id="688d7-131">Merit</span></span>](merit.md)                       | <span data-ttu-id="688d7-132">NORMALER WERT \_</span><span class="sxs-lookup"><span data-stu-id="688d7-132">MERIT\_NORMAL</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="688d7-133">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="688d7-133">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="688d7-134">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="688d7-134">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="688d7-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="688d7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="688d7-136">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="688d7-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




