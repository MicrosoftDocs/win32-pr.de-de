---
description: VGA-Filter mit 16 Farben ditherer
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: VGA-Filter mit 16 Farben ditherer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042555"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="d9be0-103">VGA-Filter mit 16 Farben ditherer</span><span class="sxs-lookup"><span data-stu-id="d9be0-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="d9be0-104">Der Modus für die VGA-Auflösung von 16 Farben wird von einem RGB-Farbtyp in eine 4-Bit-Farbanzeige konvertiert, sodass AVI-und MPEG-Videostreams auf älteren 16-farbigen Monitoren angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="d9be0-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="d9be0-105">Dieser Filter wird im Diagramm zwischen einem Debug-Filter und einem Videorendererfilter eingefügt.</span><span class="sxs-lookup"><span data-stu-id="d9be0-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9be0-106">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d9be0-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="d9be0-107">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="d9be0-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="d9be0-108">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="d9be0-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="d9be0-109">MediaType \_ Video, mediasubtype \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="d9be0-109">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="d9be0-110">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="d9be0-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="d9be0-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d9be0-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="d9be0-112">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="d9be0-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="d9be0-113">MediaType \_ Video, mediasubtype \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="d9be0-113">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="d9be0-114">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="d9be0-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="d9be0-115">[**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="d9be0-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="d9be0-116">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="d9be0-116">Filter CLSID</span></span>                             | <span data-ttu-id="d9be0-117">CLSID- \_ Dither</span><span class="sxs-lookup"><span data-stu-id="d9be0-117">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="d9be0-118">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="d9be0-118">Property Page CLSID</span></span>                      | <span data-ttu-id="d9be0-119">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="d9be0-119">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="d9be0-120">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="d9be0-120">Executable</span></span>                               | <span data-ttu-id="d9be0-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="d9be0-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="d9be0-122">Verdienst</span><span class="sxs-lookup"><span data-stu-id="d9be0-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="d9be0-123">nicht \_ wahrscheinlich</span><span class="sxs-lookup"><span data-stu-id="d9be0-123">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="d9be0-124">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="d9be0-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="d9be0-125">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="d9be0-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="d9be0-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d9be0-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9be0-127">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="d9be0-127">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



