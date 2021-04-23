---
description: MJPEG-Dekomprimierungsfilter
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: MJPEG-Dekomprimierungsfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910018"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="d802c-103">MJPEG-Dekomprimierungsfilter</span><span class="sxs-lookup"><span data-stu-id="d802c-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="d802c-104">Dieser Filter decodiert einen Videostream von motion JPEG in unkomprimiertes Video.</span><span class="sxs-lookup"><span data-stu-id="d802c-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="d802c-105">Einige digitale Videokameras erzeugen einen JPEG-Videostream mit Bewegung.</span><span class="sxs-lookup"><span data-stu-id="d802c-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



| <span data-ttu-id="d802c-106">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="d802c-106">Label</span></span> | <span data-ttu-id="d802c-107">Wert</span><span class="sxs-lookup"><span data-stu-id="d802c-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d802c-108">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="d802c-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="d802c-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="d802c-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="d802c-110">Eingabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="d802c-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="d802c-111">\_MEDIATYPE-Video, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="d802c-111">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="d802c-112">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="d802c-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="d802c-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d802c-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="d802c-114">Ausgabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="d802c-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="d802c-115">MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="d802c-115">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="d802c-116">Ausgabe-PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d802c-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="d802c-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d802c-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="d802c-118">Filtern der CLSID</span><span class="sxs-lookup"><span data-stu-id="d802c-118">Filter CLSID</span></span>                             | <span data-ttu-id="d802c-119">CLSID \_ MjpegDec</span><span class="sxs-lookup"><span data-stu-id="d802c-119">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="d802c-120">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="d802c-120">Property Page CLSID</span></span>                      | <span data-ttu-id="d802c-121">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="d802c-121">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="d802c-122">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="d802c-122">Executable</span></span>                               | <span data-ttu-id="d802c-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="d802c-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="d802c-124">Verdienst</span><span class="sxs-lookup"><span data-stu-id="d802c-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="d802c-125">NORMALER WERT \_</span><span class="sxs-lookup"><span data-stu-id="d802c-125">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="d802c-126">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="d802c-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d802c-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="d802c-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="d802c-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d802c-128">Remarks</span></span>

<span data-ttu-id="d802c-129">Dieser Filter ist mit jpeg-Bewegungsvideos kompatibel, die den FOURCC-Code "MJPG" verwenden.</span><span class="sxs-lookup"><span data-stu-id="d802c-129">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="d802c-130">Andere Arten von Motion JPEG können nicht decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="d802c-130">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="d802c-131">Für diese müssen Sie einen Drittanbieter-Decoderfilter verwenden.</span><span class="sxs-lookup"><span data-stu-id="d802c-131">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d802c-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d802c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d802c-133">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="d802c-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



