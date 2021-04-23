---
description: Filter für unendliche Pin-Tees
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filter für unendliche Pin-Tees
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909228"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="8624b-103">Filter für unendliche Pin-Tees</span><span class="sxs-lookup"><span data-stu-id="8624b-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="8624b-104">Dieser Filter liefert Beispiele, die an den Eingabepin übermittelt werden, an eine variable Anzahl von Ausgabepins.</span><span class="sxs-lookup"><span data-stu-id="8624b-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="8624b-105">Wenn eine Instanz des Filters erstellt wird, verfügt sie über einen Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="8624b-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="8624b-106">Jedes Mal, wenn ein Ausgabepin verbunden wird, erstellt der Filter einen weiteren Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="8624b-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="8624b-107">Alle Ausgabepins haben denselben Medientyp wie der Eingabepin.</span><span class="sxs-lookup"><span data-stu-id="8624b-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="8624b-108">Eine Version dieses Filters wird auch als SDK-Beispiel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8624b-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="8624b-109">Weitere Informationen finden Sie [unter InfTee-Filterbeispiel.](inftee-filter-sample.md)</span><span class="sxs-lookup"><span data-stu-id="8624b-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



| <span data-ttu-id="8624b-110">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="8624b-110">Label</span></span> | <span data-ttu-id="8624b-111">Wert</span><span class="sxs-lookup"><span data-stu-id="8624b-111">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8624b-112">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="8624b-112">Filter Interfaces</span></span>                        | [<span data-ttu-id="8624b-113">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="8624b-113">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="8624b-114">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="8624b-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="8624b-115">Beliebiger Medientyp</span><span class="sxs-lookup"><span data-stu-id="8624b-115">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="8624b-116">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8624b-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="8624b-117">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8624b-117">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="8624b-118">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="8624b-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="8624b-119">Ein beliebiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="8624b-119">Any media type.</span></span> <span data-ttu-id="8624b-120">Der Ausgabetyp stimmt für alle Ausgabepins immer mit dem Eingabetyp überein.</span><span class="sxs-lookup"><span data-stu-id="8624b-120">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="8624b-121">Ausgabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8624b-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="8624b-122">[**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="8624b-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="8624b-123">Filtern der CLSID</span><span class="sxs-lookup"><span data-stu-id="8624b-123">Filter CLSID</span></span>                             | <span data-ttu-id="8624b-124">CLSID \_ InfTee</span><span class="sxs-lookup"><span data-stu-id="8624b-124">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="8624b-125">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="8624b-125">Property Page CLSID</span></span>                      | <span data-ttu-id="8624b-126">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="8624b-126">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="8624b-127">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="8624b-127">Executable</span></span>                               | <span data-ttu-id="8624b-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="8624b-128">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="8624b-129">Verdienst</span><span class="sxs-lookup"><span data-stu-id="8624b-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="8624b-130">NICHT \_ \_ VERWENDEN \_</span><span class="sxs-lookup"><span data-stu-id="8624b-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="8624b-131">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="8624b-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="8624b-132">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="8624b-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="8624b-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8624b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8624b-134">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="8624b-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



