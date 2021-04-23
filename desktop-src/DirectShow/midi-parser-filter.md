---
description: PARSE-Parserfilter
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: PARSE-Parserfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ce659559852497b8ec55709e77f9510a1deaf2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908428"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="33186-103">PARSE-Parserfilter</span><span class="sxs-lookup"><span data-stu-id="33186-103">MIDI Parser Filter</span></span>

<span data-ttu-id="33186-104">Der PARSER-Filter liest DIE IN-Daten, die in gefunden werden. MID und . RMI-Dateien.</span><span class="sxs-lookup"><span data-stu-id="33186-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="33186-105">Der Filter akzeptiert einen Stream aus den Filtern [asynchrone Dateiquelle](file-source--async--filter.md) oder [URL-Dateiquelle](file-source--url--filter.md) und gibt FÜR-Beispiele für die Wiedergabe an den [**RENDERer VON RENDERER**](midi-renderer-filter.md) aus.</span><span class="sxs-lookup"><span data-stu-id="33186-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



| <span data-ttu-id="33186-106">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="33186-106">Label</span></span> | <span data-ttu-id="33186-107">Wert</span><span class="sxs-lookup"><span data-stu-id="33186-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33186-108">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="33186-108">Filter Interfaces</span></span>                        | <span data-ttu-id="33186-109">[**IAMMediaContent,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="33186-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="33186-110">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="33186-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="33186-111">MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Streams</span><span class="sxs-lookup"><span data-stu-id="33186-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="33186-112">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="33186-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="33186-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="33186-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="33186-114">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="33186-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="33186-115">\_MEDIATYPE- Und MEDIASUBTYPE \_ NULL-Werte</span><span class="sxs-lookup"><span data-stu-id="33186-115">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="33186-116">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="33186-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="33186-117">[**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="33186-117">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="33186-118">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="33186-118">Filter CLSID</span></span>                             | <span data-ttu-id="33186-119">\_CLSID-DATEIPARSER</span><span class="sxs-lookup"><span data-stu-id="33186-119">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="33186-120">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="33186-120">Property Page CLSID</span></span>                      | <span data-ttu-id="33186-121">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="33186-121">No property page</span></span>                                                                                         |
| <span data-ttu-id="33186-122">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="33186-122">Executable</span></span>                               | <span data-ttu-id="33186-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="33186-123">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="33186-124">Verdienst</span><span class="sxs-lookup"><span data-stu-id="33186-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="33186-125">WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH</span><span class="sxs-lookup"><span data-stu-id="33186-125">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="33186-126">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="33186-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="33186-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="33186-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="33186-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33186-128">Remarks</span></span>

<span data-ttu-id="33186-129">Weitere Informationen finden Sie unter [**RENDERING-Renderer**](midi-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="33186-129">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="33186-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33186-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33186-131">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="33186-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



