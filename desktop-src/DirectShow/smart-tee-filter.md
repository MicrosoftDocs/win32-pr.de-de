---
description: Smart Tee-Filter
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Smart Tee-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c52077066f69e50fbb5218012a402a8d556c15c1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909298"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="589d9-103">Smart Tee-Filter</span><span class="sxs-lookup"><span data-stu-id="589d9-103">Smart Tee Filter</span></span>

<span data-ttu-id="589d9-104">Der Smart Tee-Filter wird in Videoaufnahmediagrammen verwendet, um den Videostream in einen Vorschaustream und einen Erfassungsstream aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="589d9-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="589d9-105">Dies erfolgt ohne zusätzliches Kopieren von Daten.</span><span class="sxs-lookup"><span data-stu-id="589d9-105">This is done without any additional data copying.</span></span> <span data-ttu-id="589d9-106">Die Ausgabepins unterstützen alle Medientypen, die für die Downstreamverbindung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="589d9-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="589d9-107">Der Smart Tee-Filter ist nützlich, wenn ein Videoaufnahmefilter keine separaten Pins für die Erfassung und Vorschau bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="589d9-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="589d9-108">Der Smart Tee-Filter liefert nur Dann Vorschaudaten, wenn dies die Erfassungsleistung nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="589d9-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="589d9-109">Außerdem werden die Zeitstempel aus dem Vorschaustream entfernt.</span><span class="sxs-lookup"><span data-stu-id="589d9-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="589d9-110">Der Generator für Erfassungsgraphen fügt bei Bedarf automatisch den Smart Tee-Filter ein.</span><span class="sxs-lookup"><span data-stu-id="589d9-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="589d9-111">Weitere Informationen finden Sie unter [Kombinieren von Video capture und Preview](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="589d9-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="589d9-112">Die folgende Abbildung zeigt ein typisches Erfassungsdiagramm, das den Smart Tee-Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="589d9-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![Verwenden des Smart Tee-Filters](images/smarttee.png)



| <span data-ttu-id="589d9-114">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="589d9-114">Label</span></span> | <span data-ttu-id="589d9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="589d9-115">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="589d9-116">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="589d9-116">Filter Interfaces</span></span>                        | [<span data-ttu-id="589d9-117">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="589d9-117">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="589d9-118">Eingabe-Stecknadelmedientypen</span><span class="sxs-lookup"><span data-stu-id="589d9-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="589d9-119">MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="589d9-119">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="589d9-120">Eingabe-Pin-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="589d9-120">Input Pin Interfaces</span></span>                     | <span data-ttu-id="589d9-121">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="589d9-121">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="589d9-122">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="589d9-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="589d9-123">MEDIATYPE \_ Video, MEDIASUBTYPE \_ NULL</span><span class="sxs-lookup"><span data-stu-id="589d9-123">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="589d9-124">Ausgabe-PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="589d9-124">Output Pin Interfaces</span></span>                    | <span data-ttu-id="589d9-125">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="589d9-125">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="589d9-126">Filtern der CLSID</span><span class="sxs-lookup"><span data-stu-id="589d9-126">Filter CLSID</span></span>                             | <span data-ttu-id="589d9-127">CLSID \_ SmartTee</span><span class="sxs-lookup"><span data-stu-id="589d9-127">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="589d9-128">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="589d9-128">Property Page CLSID</span></span>                      | <span data-ttu-id="589d9-129">Keine Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="589d9-129">No property page.</span></span>                                                                                              |
| <span data-ttu-id="589d9-130">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="589d9-130">Executable</span></span>                               | <span data-ttu-id="589d9-131">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="589d9-131">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="589d9-132">Verdienst</span><span class="sxs-lookup"><span data-stu-id="589d9-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="589d9-133">NICHT \_ \_ VERWENDEN \_</span><span class="sxs-lookup"><span data-stu-id="589d9-133">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="589d9-134">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="589d9-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="589d9-135">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="589d9-135">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="589d9-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="589d9-136">Remarks</span></span>

<span data-ttu-id="589d9-137">Der Aufnahmepin ist der Ausgabepin 0, und der Vorschaupin ist der Ausgabepin 1.</span><span class="sxs-lookup"><span data-stu-id="589d9-137">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="589d9-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="589d9-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="589d9-139">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="589d9-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



