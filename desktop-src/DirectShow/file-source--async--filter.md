---
description: Filter für Datei Quelle (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filter für Datei Quelle (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481646"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="df7d5-103">Filter für Datei Quelle (Async)</span><span class="sxs-lookup"><span data-stu-id="df7d5-103">File Source (Async) Filter</span></span>

<span data-ttu-id="df7d5-104">Der asynchrone Datei Quellen Filter öffnet und liest lokale Dateien vieler verschiedener Datenformate und übergibt die Daten an einen Parserfilter.</span><span class="sxs-lookup"><span data-stu-id="df7d5-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="df7d5-105">Um Mediendateien über HTTP aus dem Internet herunterzuladen, verwenden Sie den Filter für die [Datei Quelle (URL)](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="df7d5-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="df7d5-106">Verwenden Sie zum Lesen von ASF-Dateien den [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter.</span><span class="sxs-lookup"><span data-stu-id="df7d5-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df7d5-107">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="df7d5-107">Filter Interfaces</span></span>                        | <span data-ttu-id="df7d5-108">[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="df7d5-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="df7d5-109">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="df7d5-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="df7d5-110">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="df7d5-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="df7d5-111">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="df7d5-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="df7d5-112">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="df7d5-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="df7d5-113">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="df7d5-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="df7d5-114">**MediaType \_ Stream**.</span><span class="sxs-lookup"><span data-stu-id="df7d5-114">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="df7d5-115">Der Untertyp hängt vom Medienformat ab.</span><span class="sxs-lookup"><span data-stu-id="df7d5-115">The subtype depends on the media format.</span></span> <span data-ttu-id="df7d5-116">(**Mediasubtype \_ null** , wenn der Filter das Format nicht erkennt).</span><span class="sxs-lookup"><span data-stu-id="df7d5-116">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="df7d5-117">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="df7d5-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="df7d5-118">[**Iamasynkreadertimestampscaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="df7d5-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="df7d5-119">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="df7d5-119">Filter CLSID</span></span>                             | <span data-ttu-id="df7d5-120">**CLSID- \_ asynshader**</span><span class="sxs-lookup"><span data-stu-id="df7d5-120">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="df7d5-121">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="df7d5-121">Property Page CLSID</span></span>                      | <span data-ttu-id="df7d5-122">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="df7d5-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="df7d5-123">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="df7d5-123">Executable</span></span>                               | <span data-ttu-id="df7d5-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="df7d5-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="df7d5-125">Verdienst</span><span class="sxs-lookup"><span data-stu-id="df7d5-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="df7d5-126">**nicht \_ wahrscheinlich**</span><span class="sxs-lookup"><span data-stu-id="df7d5-126">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="df7d5-127">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="df7d5-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="df7d5-128">**CLSID \_ legacyamfiltercategory**</span><span class="sxs-lookup"><span data-stu-id="df7d5-128">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="df7d5-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df7d5-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df7d5-130">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="df7d5-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



