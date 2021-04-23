---
description: Filter für Dateiquelle (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filter für Dateiquelle (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ddfa7282adbf5117bd2c52465c6eb30efbd69e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909238"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="2444a-103">Filter für Dateiquelle (URL)</span><span class="sxs-lookup"><span data-stu-id="2444a-103">File Source (URL) Filter</span></span>

<span data-ttu-id="2444a-104">Der Filter URL-Dateiquelle ist ein generischer asynchroner Quellfilter, der mit jeder Quelldatei funktioniert, die durch eine Uniform Resource Locator (URL) identifiziert werden kann und deren Haupttyp des Mediums stream ist.</span><span class="sxs-lookup"><span data-stu-id="2444a-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="2444a-105">Dies schließt AVI-, MOV-, MPEG- und WAV-Dateien ein.</span><span class="sxs-lookup"><span data-stu-id="2444a-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="2444a-106">Der Downstreamfilter muss ein Parser sein, z. B. der [MPEG-1-Stream Splitter,](mpeg-1-stream-splitter-filter.md)der [AVI-Splitter](avi-splitter-filter.md)oder der [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2444a-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



| <span data-ttu-id="2444a-107">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="2444a-107">Label</span></span> | <span data-ttu-id="2444a-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2444a-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2444a-109">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="2444a-109">Filter Interfaces</span></span>                        | <span data-ttu-id="2444a-110">[**IAMOpenProgress,**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="2444a-110">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="2444a-111">Eingabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="2444a-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="2444a-112">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="2444a-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="2444a-113">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="2444a-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="2444a-114">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="2444a-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="2444a-115">Ausgabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="2444a-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="2444a-116">\_MEDIATYPE-Stream.</span><span class="sxs-lookup"><span data-stu-id="2444a-116">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="2444a-117">Der Untertyp hängt vom Medienformat ab.</span><span class="sxs-lookup"><span data-stu-id="2444a-117">The subtype depends on the media format.</span></span> <span data-ttu-id="2444a-118">(MEDIASUBTYPE \_ NULL, wenn der Filter das Format nicht erkennt.)</span><span class="sxs-lookup"><span data-stu-id="2444a-118">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="2444a-119">Ausgabe-PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2444a-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="2444a-120">[**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="2444a-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="2444a-121">Filtern der CLSID</span><span class="sxs-lookup"><span data-stu-id="2444a-121">Filter CLSID</span></span>                             | <span data-ttu-id="2444a-122">CLSID \_ URLReader</span><span class="sxs-lookup"><span data-stu-id="2444a-122">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="2444a-123">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="2444a-123">Property Page CLSID</span></span>                      | <span data-ttu-id="2444a-124">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="2444a-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="2444a-125">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="2444a-125">Executable</span></span>                               | <span data-ttu-id="2444a-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="2444a-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="2444a-127">Verdienst</span><span class="sxs-lookup"><span data-stu-id="2444a-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="2444a-128">\_UNWAHRSCHEINLICHE WAHRSCHEINLICHKEIT</span><span class="sxs-lookup"><span data-stu-id="2444a-128">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="2444a-129">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="2444a-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="2444a-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="2444a-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="2444a-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2444a-131">Remarks</span></span>

<span data-ttu-id="2444a-132">Dieser Filter verwendet URLMon und unterstützt Codepages.</span><span class="sxs-lookup"><span data-stu-id="2444a-132">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2444a-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2444a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2444a-134">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="2444a-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



