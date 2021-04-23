---
description: VGA 16 Color Ditherer Filter
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: VGA 16 Color Ditherer Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908678"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="35a3f-103">VGA 16 Color Ditherer Filter</span><span class="sxs-lookup"><span data-stu-id="35a3f-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="35a3f-104">Der VGA 16 Color Ditherer-Filter konvertiert von einem RGB-Farbtyp in eine 4-Bit-Farbanzeige, sodass AVI- und MPEG-Videostreams auf älteren Monitoren mit 16 Farben angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="35a3f-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="35a3f-105">Dieser Filter wird in das Diagramm zwischen einem Dekomprimiererfilter und einem Videorendererfilter eingefügt.</span><span class="sxs-lookup"><span data-stu-id="35a3f-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



| <span data-ttu-id="35a3f-106">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="35a3f-106">Label</span></span> | <span data-ttu-id="35a3f-107">Wert</span><span class="sxs-lookup"><span data-stu-id="35a3f-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35a3f-108">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="35a3f-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="35a3f-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="35a3f-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="35a3f-110">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="35a3f-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="35a3f-111">MEDIATYPE \_ Video, MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="35a3f-111">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="35a3f-112">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="35a3f-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="35a3f-113">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="35a3f-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="35a3f-114">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="35a3f-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="35a3f-115">MEDIATYPE \_ Video, MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="35a3f-115">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="35a3f-116">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="35a3f-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="35a3f-117">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="35a3f-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="35a3f-118">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="35a3f-118">Filter CLSID</span></span>                             | <span data-ttu-id="35a3f-119">CLSID \_ Dither</span><span class="sxs-lookup"><span data-stu-id="35a3f-119">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="35a3f-120">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="35a3f-120">Property Page CLSID</span></span>                      | <span data-ttu-id="35a3f-121">Keine Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="35a3f-121">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="35a3f-122">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="35a3f-122">Executable</span></span>                               | <span data-ttu-id="35a3f-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="35a3f-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="35a3f-124">Verdienst</span><span class="sxs-lookup"><span data-stu-id="35a3f-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="35a3f-125">WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH</span><span class="sxs-lookup"><span data-stu-id="35a3f-125">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="35a3f-126">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="35a3f-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="35a3f-127">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="35a3f-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="35a3f-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35a3f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35a3f-129">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="35a3f-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



