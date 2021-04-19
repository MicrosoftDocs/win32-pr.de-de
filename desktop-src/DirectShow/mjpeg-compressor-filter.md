---
description: MJPEG-Daemon-Filter
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: MJPEG-Daemon-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346200"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="dce35-103">MJPEG-Daemon-Filter</span><span class="sxs-lookup"><span data-stu-id="dce35-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="dce35-104">Dieser Filter komprimiert einen nicht komprimierten Videostream mithilfe der Motion JPEG-Komprimierung.</span><span class="sxs-lookup"><span data-stu-id="dce35-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce35-105">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dce35-105">Filter Interfaces</span></span>                        | <span data-ttu-id="dce35-106">[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="dce35-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="dce35-107">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="dce35-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="dce35-108">MediaType- \_ Video, mediasubtype \_ null</span><span class="sxs-lookup"><span data-stu-id="dce35-108">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="dce35-109">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="dce35-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="dce35-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="dce35-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="dce35-111">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="dce35-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="dce35-112">MediaType- \_ Video, mediasubtype \_ mjpg</span><span class="sxs-lookup"><span data-stu-id="dce35-112">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="dce35-113">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dce35-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="dce35-114">[**Iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="dce35-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="dce35-115">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="dce35-115">Filter CLSID</span></span>                             | <span data-ttu-id="dce35-116">CLSID- \_ mjpgenc</span><span class="sxs-lookup"><span data-stu-id="dce35-116">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="dce35-117">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="dce35-117">Property Page CLSID</span></span>                      | <span data-ttu-id="dce35-118">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="dce35-118">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="dce35-119">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="dce35-119">Executable</span></span>                               | <span data-ttu-id="dce35-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="dce35-120">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="dce35-121">Verdienst</span><span class="sxs-lookup"><span data-stu-id="dce35-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="dce35-122">das Verdienst wird \_ \_ nicht \_ verwendet.</span><span class="sxs-lookup"><span data-stu-id="dce35-122">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="dce35-123">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="dce35-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="dce35-124">CLSID \_ videocompressorcategory</span><span class="sxs-lookup"><span data-stu-id="dce35-124">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="dce35-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dce35-125">Remarks</span></span>

<span data-ttu-id="dce35-126">Dieser Filter codiert mithilfe des Medien Untertyps mediasubtype \_ mjpg, der dem FourCC-Code ' mjpg ' entspricht.</span><span class="sxs-lookup"><span data-stu-id="dce35-126">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dce35-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dce35-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dce35-128">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="dce35-128">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



