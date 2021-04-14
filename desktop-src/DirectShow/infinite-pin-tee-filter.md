---
description: Filter für unendliche Pin-Tee
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filter für unendliche Pin-Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392738"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="1bc2a-103">Filter für unendliche Pin-Tee</span><span class="sxs-lookup"><span data-stu-id="1bc2a-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="1bc2a-104">Dieser Filter liefert der Eingabe-PIN übergebene Beispiele an eine Variable Anzahl von Ausgabe Pins.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="1bc2a-105">Wenn eine Instanz des Filters erstellt wird, verfügt sie über eine Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="1bc2a-106">Jedes Mal, wenn eine Ausgabepin verbunden ist, erstellt der Filter eine weitere Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="1bc2a-107">Alle Ausgabe Pins haben denselben Medientyp wie die Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="1bc2a-108">Eine Version dieses Filters wird auch als SDK-Beispiel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="1bc2a-109">Siehe [Info Filter Sample](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1bc2a-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc2a-110">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1bc2a-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="1bc2a-111">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="1bc2a-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="1bc2a-112">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1bc2a-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="1bc2a-113">Beliebige Medientyp</span><span class="sxs-lookup"><span data-stu-id="1bc2a-113">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="1bc2a-114">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="1bc2a-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1bc2a-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1bc2a-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="1bc2a-116">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1bc2a-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="1bc2a-117">Ein beliebiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-117">Any media type.</span></span> <span data-ttu-id="1bc2a-118">Der Ausgabetyp stimmt immer mit dem Eingabetyp für alle Ausgabe Pins überein.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-118">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="1bc2a-119">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1bc2a-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="1bc2a-120">[**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1bc2a-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="1bc2a-121">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="1bc2a-121">Filter CLSID</span></span>                             | <span data-ttu-id="1bc2a-122">CLSID \_ -Empfänger</span><span class="sxs-lookup"><span data-stu-id="1bc2a-122">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="1bc2a-123">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="1bc2a-123">Property Page CLSID</span></span>                      | <span data-ttu-id="1bc2a-124">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="1bc2a-124">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="1bc2a-125">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="1bc2a-125">Executable</span></span>                               | <span data-ttu-id="1bc2a-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="1bc2a-126">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="1bc2a-127">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1bc2a-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="1bc2a-128">das Verdienst wird \_ \_ nicht \_ verwendet.</span><span class="sxs-lookup"><span data-stu-id="1bc2a-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="1bc2a-129">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="1bc2a-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1bc2a-130">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="1bc2a-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="1bc2a-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1bc2a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bc2a-132">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="1bc2a-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



