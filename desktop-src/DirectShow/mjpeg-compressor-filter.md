---
description: MJPEG-Filter
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: MJPEG-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02928df4d09b50c0ac152aed99ed87dc6362fb70
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910008"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="11077-103">MJPEG-Filter</span><span class="sxs-lookup"><span data-stu-id="11077-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="11077-104">Dieser Filter komprimiert einen unkomprimierten Videostream mithilfe der JPEG-Komprimierung für Bewegung.</span><span class="sxs-lookup"><span data-stu-id="11077-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



| <span data-ttu-id="11077-105">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="11077-105">Label</span></span> | <span data-ttu-id="11077-106">Wert</span><span class="sxs-lookup"><span data-stu-id="11077-106">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11077-107">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="11077-107">Filter Interfaces</span></span>                        | <span data-ttu-id="11077-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="11077-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="11077-109">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="11077-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="11077-110">MEDIATYPE \_ VIDEO, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="11077-110">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="11077-111">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="11077-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="11077-112">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="11077-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="11077-113">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="11077-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="11077-114">MEDIATYPE \_ Video, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="11077-114">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="11077-115">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="11077-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="11077-116">[**IAMStreamConfig,**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) [**IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="11077-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="11077-117">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="11077-117">Filter CLSID</span></span>                             | <span data-ttu-id="11077-118">CLSID \_ MJPGEnc</span><span class="sxs-lookup"><span data-stu-id="11077-118">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="11077-119">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="11077-119">Property Page CLSID</span></span>                      | <span data-ttu-id="11077-120">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="11077-120">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="11077-121">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="11077-121">Executable</span></span>                               | <span data-ttu-id="11077-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="11077-122">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="11077-123">Verdienst</span><span class="sxs-lookup"><span data-stu-id="11077-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="11077-124">NICHT \_ \_ VERWENDEN \_</span><span class="sxs-lookup"><span data-stu-id="11077-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="11077-125">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="11077-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="11077-126">CLSID \_ VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="11077-126">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="11077-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11077-127">Remarks</span></span>

<span data-ttu-id="11077-128">Dieser Filter codiert mithilfe des Medienuntertyps MEDIASUBTYPE MJPG, der dem \_ FOURCC-Code "MJPG" entspricht.</span><span class="sxs-lookup"><span data-stu-id="11077-128">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11077-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11077-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11077-130">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="11077-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



