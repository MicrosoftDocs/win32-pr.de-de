---
description: MIDI-Parser-Filter
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: MIDI-Parser-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957733"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="d30de-103">MIDI-Parser-Filter</span><span class="sxs-lookup"><span data-stu-id="d30de-103">MIDI Parser Filter</span></span>

<span data-ttu-id="d30de-104">Der MIDI-Parser-Filter liest die in gefundenen Daten in. Mid und. RMI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="d30de-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="d30de-105">Der Filter akzeptiert einen Stream aus den Quell Filtern der asynchronen [Datei Quelle](file-source--async--filter.md) oder der [URL-Datei](file-source--url--filter.md) und gibt die für die Wiedergabe verwendeten MIDI-Beispiele an den [**MIDI-Renderer**](midi-renderer-filter.md)</span><span class="sxs-lookup"><span data-stu-id="d30de-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d30de-106">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d30de-106">Filter Interfaces</span></span>                        | <span data-ttu-id="d30de-107">[**Iammediacontent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="d30de-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="d30de-108">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="d30de-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="d30de-109">MediaType \_ Stream, mediasubtype \_ MIDI</span><span class="sxs-lookup"><span data-stu-id="d30de-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="d30de-110">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="d30de-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="d30de-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d30de-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="d30de-112">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="d30de-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="d30de-113">MediaType \_ MIDI, mediasubtype \_ null</span><span class="sxs-lookup"><span data-stu-id="d30de-113">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="d30de-114">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d30de-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="d30de-115">[**Imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="d30de-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="d30de-116">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="d30de-116">Filter CLSID</span></span>                             | <span data-ttu-id="d30de-117">CLSID- \_ midiparser</span><span class="sxs-lookup"><span data-stu-id="d30de-117">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="d30de-118">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="d30de-118">Property Page CLSID</span></span>                      | <span data-ttu-id="d30de-119">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="d30de-119">No property page</span></span>                                                                                         |
| <span data-ttu-id="d30de-120">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="d30de-120">Executable</span></span>                               | <span data-ttu-id="d30de-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="d30de-121">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="d30de-122">Verdienst</span><span class="sxs-lookup"><span data-stu-id="d30de-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="d30de-123">nicht \_ wahrscheinlich</span><span class="sxs-lookup"><span data-stu-id="d30de-123">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="d30de-124">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="d30de-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d30de-125">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="d30de-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="d30de-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d30de-126">Remarks</span></span>

<span data-ttu-id="d30de-127">Weitere Informationen finden Sie unter [**MIDI-Renderer**](midi-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="d30de-127">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d30de-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d30de-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d30de-129">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="d30de-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



