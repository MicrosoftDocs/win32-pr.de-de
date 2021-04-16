---
description: MJPEG-Debug-Filter
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: MJPEG-Debug-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522456"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="1dd7d-103">MJPEG-Debug-Filter</span><span class="sxs-lookup"><span data-stu-id="1dd7d-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="1dd7d-104">Dieser Filter decodiert einen Videostream von Motion JPEG in unkomprimiertes Video.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="1dd7d-105">Einige digitale Videokameras entwickeln einen Videodaten Strom in Motion JPEG.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd7d-106">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1dd7d-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="1dd7d-107">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="1dd7d-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="1dd7d-108">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1dd7d-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="1dd7d-109">MediaType- \_ Video, mediasubtype \_ mjpg</span><span class="sxs-lookup"><span data-stu-id="1dd7d-109">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="1dd7d-110">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="1dd7d-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1dd7d-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1dd7d-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="1dd7d-112">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1dd7d-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="1dd7d-113">MediaType- \_ Video, mediasubtype \_ null</span><span class="sxs-lookup"><span data-stu-id="1dd7d-113">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="1dd7d-114">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1dd7d-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="1dd7d-115">[**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1dd7d-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="1dd7d-116">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="1dd7d-116">Filter CLSID</span></span>                             | <span data-ttu-id="1dd7d-117">CLSID- \_ mjpgdec</span><span class="sxs-lookup"><span data-stu-id="1dd7d-117">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="1dd7d-118">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="1dd7d-118">Property Page CLSID</span></span>                      | <span data-ttu-id="1dd7d-119">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="1dd7d-119">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="1dd7d-120">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="1dd7d-120">Executable</span></span>                               | <span data-ttu-id="1dd7d-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1dd7d-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="1dd7d-122">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1dd7d-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="1dd7d-123">Verdienst \_ Normal</span><span class="sxs-lookup"><span data-stu-id="1dd7d-123">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="1dd7d-124">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="1dd7d-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1dd7d-125">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="1dd7d-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="1dd7d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dd7d-126">Remarks</span></span>

<span data-ttu-id="1dd7d-127">Dieser Filter ist kompatibel mit dem Motion JPEG-Video, das den FourCC-Code "mjpg" verwendet.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-127">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="1dd7d-128">Andere Varianten von Motion JPEG können nicht decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-128">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="1dd7d-129">Hierzu müssen Sie einen Drittanbieter-Decoder-Filter verwenden.</span><span class="sxs-lookup"><span data-stu-id="1dd7d-129">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dd7d-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1dd7d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dd7d-131">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="1dd7d-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



