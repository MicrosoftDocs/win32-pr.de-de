---
description: Dateiquellenfilter (asynchron)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Dateiquellenfilter (asynchron)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909698"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="d239e-103">Dateiquellenfilter (asynchron)</span><span class="sxs-lookup"><span data-stu-id="d239e-103">File Source (Async) Filter</span></span>

<span data-ttu-id="d239e-104">Der Filter Asynchrone Dateiquelle wird geöffnet und liest lokale Dateien mit vielen verschiedenen Datenformaten und übergibt die Daten an einen Parserfilter.</span><span class="sxs-lookup"><span data-stu-id="d239e-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="d239e-105">Verwenden Sie zum Herunterladen von Mediendateien aus dem Web über HTTP den Filter Dateiquelle [(URL).](file-source--url--filter.md)</span><span class="sxs-lookup"><span data-stu-id="d239e-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="d239e-106">Verwenden Sie zum Lesen von ASF-Dateien den [WM ASF-Readerfilter.](wm-asf-reader-filter.md)</span><span class="sxs-lookup"><span data-stu-id="d239e-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



| <span data-ttu-id="d239e-107">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d239e-107">Label</span></span> | <span data-ttu-id="d239e-108">Wert</span><span class="sxs-lookup"><span data-stu-id="d239e-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d239e-109">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="d239e-109">Filter Interfaces</span></span>                        | <span data-ttu-id="d239e-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="d239e-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="d239e-111">Eingabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="d239e-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="d239e-112">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="d239e-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="d239e-113">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="d239e-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="d239e-114">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="d239e-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="d239e-115">Ausgabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="d239e-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="d239e-116">**MEDIATYPE \_ Streamen Sie**.</span><span class="sxs-lookup"><span data-stu-id="d239e-116">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="d239e-117">Der Untertyp hängt vom Medienformat ab.</span><span class="sxs-lookup"><span data-stu-id="d239e-117">The subtype depends on the media format.</span></span> <span data-ttu-id="d239e-118">(**MEDIASUBTYPE \_ NULL,** wenn der Filter das Format nicht erkennt.)</span><span class="sxs-lookup"><span data-stu-id="d239e-118">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="d239e-119">Ausgabe-PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d239e-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="d239e-120">[**IAMAsyncReaderTimestampScaling,**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling) [**IAsyncReader,**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="d239e-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="d239e-121">Filtern der CLSID</span><span class="sxs-lookup"><span data-stu-id="d239e-121">Filter CLSID</span></span>                             | <span data-ttu-id="d239e-122">**CLSID \_ AsyncReader**</span><span class="sxs-lookup"><span data-stu-id="d239e-122">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="d239e-123">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="d239e-123">Property Page CLSID</span></span>                      | <span data-ttu-id="d239e-124">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="d239e-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="d239e-125">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="d239e-125">Executable</span></span>                               | <span data-ttu-id="d239e-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="d239e-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="d239e-127">Verdienst</span><span class="sxs-lookup"><span data-stu-id="d239e-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="d239e-128">**\_UNWAHRSCHEINLICHE WAHRSCHEINLICHKEIT**</span><span class="sxs-lookup"><span data-stu-id="d239e-128">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="d239e-129">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="d239e-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d239e-130">**CLSID \_ LegacyAmFilterCategory**</span><span class="sxs-lookup"><span data-stu-id="d239e-130">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="d239e-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d239e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d239e-132">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="d239e-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



