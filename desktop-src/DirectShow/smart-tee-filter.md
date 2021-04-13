---
description: Smart Tee-Filter
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Smart Tee-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647e04ef2a24bde43c9d02b7986fd8a645a6b60c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482299"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="1ade5-103">Smart Tee-Filter</span><span class="sxs-lookup"><span data-stu-id="1ade5-103">Smart Tee Filter</span></span>

<span data-ttu-id="1ade5-104">Der Smart Tee-Filter wird in Video Erfassungs Diagrammen verwendet, um den Videostream in einen Vorschau Datenstrom und einen Aufzeichnungsdaten Strom aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="1ade5-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="1ade5-105">Dies erfolgt ohne zusätzliches Kopieren von Daten.</span><span class="sxs-lookup"><span data-stu-id="1ade5-105">This is done without any additional data copying.</span></span> <span data-ttu-id="1ade5-106">Die Ausgabe Pins unterstützen alle Medientypen, die von der Downstream-Verbindung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1ade5-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="1ade5-107">Der Smart Tee-Filter ist nützlich, wenn ein Video Erfassungs Filter keine separaten Pins für Erfassung und Vorschau bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="1ade5-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="1ade5-108">Der Smart Tee-Filter liefert nur die Vorschau Daten, wenn dies die Leistungs Erfassung nicht beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="1ade5-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="1ade5-109">Außerdem werden die Zeitstempel aus dem Vorschau Datenstrom entfernt.</span><span class="sxs-lookup"><span data-stu-id="1ade5-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="1ade5-110">Der Erfassungs Diagramm-Generator fügt bei Bedarf automatisch den intelligenten Tee-Filter ein.</span><span class="sxs-lookup"><span data-stu-id="1ade5-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="1ade5-111">Weitere Informationen finden Sie unter [Kombinieren von Video Erfassung und Vorschau](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="1ade5-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="1ade5-112">Die folgende Abbildung zeigt ein typisches Erfassungs Diagramm, das den intelligenten Tee-Filter verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ade5-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![Verwenden des Smart Tee-Filters](images/smarttee.png)



|                                          |                                                                                                                |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ade5-114">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ade5-114">Filter Interfaces</span></span>                        | [<span data-ttu-id="1ade5-115">**Ibasefilter**</span><span class="sxs-lookup"><span data-stu-id="1ade5-115">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="1ade5-116">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1ade5-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="1ade5-117">MediaType- \_ Video, mediasubtype \_ null</span><span class="sxs-lookup"><span data-stu-id="1ade5-117">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="1ade5-118">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ade5-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1ade5-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1ade5-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="1ade5-120">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1ade5-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="1ade5-121">MediaType- \_ Video, mediasubtype \_ null</span><span class="sxs-lookup"><span data-stu-id="1ade5-121">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="1ade5-122">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1ade5-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="1ade5-123">[**Iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1ade5-123">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="1ade5-124">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="1ade5-124">Filter CLSID</span></span>                             | <span data-ttu-id="1ade5-125">CLSID- \_ smarttee</span><span class="sxs-lookup"><span data-stu-id="1ade5-125">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="1ade5-126">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="1ade5-126">Property Page CLSID</span></span>                      | <span data-ttu-id="1ade5-127">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="1ade5-127">No property page.</span></span>                                                                                              |
| <span data-ttu-id="1ade5-128">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="1ade5-128">Executable</span></span>                               | <span data-ttu-id="1ade5-129">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="1ade5-129">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="1ade5-130">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1ade5-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="1ade5-131">das Verdienst wird \_ \_ nicht \_ verwendet.</span><span class="sxs-lookup"><span data-stu-id="1ade5-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="1ade5-132">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="1ade5-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1ade5-133">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="1ade5-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="1ade5-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ade5-134">Remarks</span></span>

<span data-ttu-id="1ade5-135">Die Erfassungs-PIN ist die Ausgabe-PIN 0, und die Vorschau-PIN lautet Ausgabe-PIN 1.</span><span class="sxs-lookup"><span data-stu-id="1ade5-135">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ade5-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ade5-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ade5-137">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="1ade5-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



