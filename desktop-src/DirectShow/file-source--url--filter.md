---
description: Datei Quellen Filter (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Datei Quellen Filter (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125107"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="7bdb5-103">Datei Quellen Filter (URL)</span><span class="sxs-lookup"><span data-stu-id="7bdb5-103">File Source (URL) Filter</span></span>

<span data-ttu-id="7bdb5-104">Der URL-Quell Filter ist ein generischer asynchroner Quell Filter, der mit einer beliebigen Quelldatei verwendet werden kann, die durch eine Uniform Resource Locator (URL) identifiziert werden kann und deren Haupt Datentyp Stream ist.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="7bdb5-105">Hierzu gehören AVI-, MOV-, MPEG-und WAV-Dateien.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="7bdb5-106">Der downstreamfilter muss ein Parser sein, z. b. der [MPEG-1-streamsplitter](mpeg-1-stream-splitter-filter.md), der [avi-Splitter](avi-splitter-filter.md)oder der QuickTime- [Film Parser](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7bdb5-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bdb5-107">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7bdb5-107">Filter Interfaces</span></span>                        | <span data-ttu-id="7bdb5-108">[**Iamopenprogress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="7bdb5-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="7bdb5-109">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="7bdb5-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="7bdb5-110">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="7bdb5-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="7bdb5-111">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="7bdb5-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="7bdb5-112">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="7bdb5-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="7bdb5-113">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="7bdb5-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="7bdb5-114">MediaType-Daten \_ Strom.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-114">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="7bdb5-115">Der Untertyp hängt vom Medienformat ab.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-115">The subtype depends on the media format.</span></span> <span data-ttu-id="7bdb5-116">(Mediasubtype \_ NULL, wenn der Filter das Format nicht erkennt.)</span><span class="sxs-lookup"><span data-stu-id="7bdb5-116">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="7bdb5-117">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="7bdb5-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="7bdb5-118">[**Iamasynkreadertimestampscaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="7bdb5-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="7bdb5-119">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="7bdb5-119">Filter CLSID</span></span>                             | <span data-ttu-id="7bdb5-120">CLSID- \_ urlreader</span><span class="sxs-lookup"><span data-stu-id="7bdb5-120">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="7bdb5-121">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="7bdb5-121">Property Page CLSID</span></span>                      | <span data-ttu-id="7bdb5-122">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="7bdb5-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="7bdb5-123">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="7bdb5-123">Executable</span></span>                               | <span data-ttu-id="7bdb5-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="7bdb5-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="7bdb5-125">Verdienst</span><span class="sxs-lookup"><span data-stu-id="7bdb5-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="7bdb5-126">nicht \_ wahrscheinlich</span><span class="sxs-lookup"><span data-stu-id="7bdb5-126">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="7bdb5-127">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="7bdb5-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="7bdb5-128">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="7bdb5-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="7bdb5-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bdb5-129">Remarks</span></span>

<span data-ttu-id="7bdb5-130">Dieser Filter verwendet Urlmon und unterstützt Codepages.</span><span class="sxs-lookup"><span data-stu-id="7bdb5-130">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bdb5-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7bdb5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bdb5-132">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="7bdb5-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



