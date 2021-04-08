---
description: AVI-Debug-Filter
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: AVI-Debug-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b6fcff61dd867c598e793fb5aa8fbff67dc6cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746921"
---
# <a name="avi-decompressor-filter"></a><span data-ttu-id="5904c-103">AVI-Debug-Filter</span><span class="sxs-lookup"><span data-stu-id="5904c-103">AVI Decompressor Filter</span></span>

<span data-ttu-id="5904c-104">Der AVI-Debug-Filter ermöglicht VCM-Codecs (Video Compression Manager) zum Verknüpfen eines Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="5904c-104">The AVI Decompressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="5904c-105">Die Anwendung muss den Filter nicht zum Filter Diagramm hinzufügen. Sie wird automatisch vom Filter Graph-Manager abgerufen, wenn dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5904c-105">The application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span>

<span data-ttu-id="5904c-106">Wenn der Filter Graph-Manager ein Diagramm zum Rendering einer AVI-Datei aufbaut, überprüft er den FourCC im AVI-Header der Datei, um zu bestimmen, ob der Videostream komprimiert ist.</span><span class="sxs-lookup"><span data-stu-id="5904c-106">When the Filter Graph Manager is building a graph to render an AVI file, it checks the FOURCC in the file's AVI header to determine whether the video stream is compressed.</span></span> <span data-ttu-id="5904c-107">Wenn dies der Fall ist, fügt der Filter Graph-Manager den AVI Dekompressor hinzu, der dann in der Registrierung nach einem installierten Dekompressor sucht, der die Datei verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="5904c-107">If it is, the Filter Graph Manager adds the AVI Decompressor, which then searches the registry for an installed decompressor that can handle the file.</span></span>

> [!Note]  
> <span data-ttu-id="5904c-108">MPEG-Debug werden nie als VCM-Codecs implementiert, sondern nur als Native DirectShow-Filter.</span><span class="sxs-lookup"><span data-stu-id="5904c-108">MPEG decompressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 

<span data-ttu-id="5904c-109">In der upstreampin stellt der AVI-Debug in der Regel eine Verbindung mit dem [avi-Splitter](avi-splitter-filter.md)her.</span><span class="sxs-lookup"><span data-stu-id="5904c-109">On its upstream pin the AVI Decompressor typically connects to the [AVI Splitter](avi-splitter-filter.md).</span></span> <span data-ttu-id="5904c-110">Bei der Ausgabe-PIN stellt Sie in der Regel eine Verbindung mit dem [Videorenderer](video-renderer-filter.md) oder dem [AVI MUX-Filter](avi-mux-filter.md)her.</span><span class="sxs-lookup"><span data-stu-id="5904c-110">On its output pin it typically connects to the [Video Renderer](video-renderer-filter.md) or the [AVI Mux Filter](avi-mux-filter.md).</span></span>



|                                          |                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5904c-111">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5904c-111">Filter Interfaces</span></span>                        | [<span data-ttu-id="5904c-112">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="5904c-112">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| <span data-ttu-id="5904c-113">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="5904c-113">Input Pin Media Types</span></span>                    | <span data-ttu-id="5904c-114">Haupttyp: MediaType \_ videosubtype: muss dem FourCC-Code für den Komprimierungstyp entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5904c-114">Major type: MEDIATYPE\_VideoSubtype: Must correspond to the FOURCC code for the compression type.</span></span> <span data-ttu-id="5904c-115">Weitere Informationen finden Sie unter [FOURCC Codes](fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5904c-115">For more information, see [FOURCC Codes](fourcc-codes.md).</span></span><br/> <span data-ttu-id="5904c-116">Formattyp: \_ Video Info formatieren</span><span class="sxs-lookup"><span data-stu-id="5904c-116">Format type: FORMAT\_VideoInfo</span></span><br/> |
| <span data-ttu-id="5904c-117">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="5904c-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="5904c-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5904c-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                             |
| <span data-ttu-id="5904c-119">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="5904c-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="5904c-120">MediaType- \_ Video, mediasubtype \_ NULL, \_ Video Info formatieren</span><span class="sxs-lookup"><span data-stu-id="5904c-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL, FORMAT\_VideoInfo</span></span>                                                                                                                                                            |
| <span data-ttu-id="5904c-121">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5904c-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="5904c-122">[**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="5904c-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                 |
| <span data-ttu-id="5904c-123">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="5904c-123">Filter CLSID</span></span>                             | <span data-ttu-id="5904c-124">CLSID- \_ avidec</span><span class="sxs-lookup"><span data-stu-id="5904c-124">CLSID\_AVIDec</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="5904c-125">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="5904c-125">Property Page CLSID</span></span>                      | <span data-ttu-id="5904c-126">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="5904c-126">No property page.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="5904c-127">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="5904c-127">Executable</span></span>                               | <span data-ttu-id="5904c-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="5904c-128">quartz.dll</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="5904c-129">Verdienst</span><span class="sxs-lookup"><span data-stu-id="5904c-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="5904c-130">Verdienst \_ Normal</span><span class="sxs-lookup"><span data-stu-id="5904c-130">MERIT\_NORMAL</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="5904c-131">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="5904c-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="5904c-132">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="5904c-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="5904c-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5904c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5904c-134">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="5904c-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




