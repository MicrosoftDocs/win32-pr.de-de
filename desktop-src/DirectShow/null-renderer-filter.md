---
description: Der NULL-rendererfilter ist ein Renderer, der alle empfangenen Beispiele verwirft, ohne die Beispiel Daten anzuzeigen oder zu rendern.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: NULL-rendererfilter (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 7ff6c728276ca3fd69c14e304780b1d70c563265
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371418"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="1f1c8-103">NULL-rendererfilter</span><span class="sxs-lookup"><span data-stu-id="1f1c8-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="1f1c8-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="1f1c8-104">\[Deprecated.</span></span> <span data-ttu-id="1f1c8-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="1f1c8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1f1c8-106">Der NULL-rendererfilter ist ein Renderer, der alle empfangenen Beispiele verwirft, ohne die Beispiel Daten anzuzeigen oder zu rendern.</span><span class="sxs-lookup"><span data-stu-id="1f1c8-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



|                                          |                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1c8-107">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1f1c8-107">Filter interfaces</span></span>                        | <span data-ttu-id="1f1c8-108">[**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="1f1c8-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="1f1c8-109">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1f1c8-109">Input pin media types</span></span>                    | <span data-ttu-id="1f1c8-110">Beliebige Medientyp</span><span class="sxs-lookup"><span data-stu-id="1f1c8-110">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="1f1c8-111">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="1f1c8-111">Input pin interfaces</span></span>                     | <span data-ttu-id="1f1c8-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1f1c8-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="1f1c8-113">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="1f1c8-113">Output pin media types</span></span>                   | <span data-ttu-id="1f1c8-114">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="1f1c8-114">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="1f1c8-115">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1f1c8-115">Output pin interfaces</span></span>                    | <span data-ttu-id="1f1c8-116">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="1f1c8-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="1f1c8-117">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="1f1c8-117">Filter CLSID</span></span>                             | <span data-ttu-id="1f1c8-118">CLSID- \_ nullrenderer</span><span class="sxs-lookup"><span data-stu-id="1f1c8-118">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="1f1c8-119">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="1f1c8-119">Property Page CLSID</span></span>                      | <span data-ttu-id="1f1c8-120">Keine Eigenschaften Seite.</span><span class="sxs-lookup"><span data-stu-id="1f1c8-120">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="1f1c8-121">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="1f1c8-121">Executable</span></span>                               | <span data-ttu-id="1f1c8-122">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="1f1c8-122">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="1f1c8-123">Verdienst</span><span class="sxs-lookup"><span data-stu-id="1f1c8-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="1f1c8-124">das Verdienst wird \_ \_ nicht \_ verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f1c8-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="1f1c8-125">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="1f1c8-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1f1c8-126">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="1f1c8-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="1f1c8-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f1c8-127">Remarks</span></span>

<span data-ttu-id="1f1c8-128">Verwenden Sie diesen Filter, wenn eine Ausgabepin im Diagramm eine Downstreamverbindung erfordert, Sie aber nicht möchten, dass die Daten aus dieser Pin rendertet werden.</span><span class="sxs-lookup"><span data-stu-id="1f1c8-128">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="1f1c8-129">Indem Sie die Ausgabe-PIN mit dem NULL-Renderer verbinden, vervollständigen Sie die Verbindung, ohne die Daten zu rendern.</span><span class="sxs-lookup"><span data-stu-id="1f1c8-129">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="1f1c8-130">Obwohl dieser Filter keine Beispiele renderei, wartet er auf die Präsentationszeit der einzelnen Beispiele, bevor das Beispiel verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="1f1c8-130">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="1f1c8-131">Daher wird das Diagramm mit dem normalen Satz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1f1c8-131">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="1f1c8-132">Wenn Sie möchten, dass das Diagramm so schnell wie möglich ausgeführt wird, legen Sie die Referenzuhr auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="1f1c8-132">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="1f1c8-133">Weitere Informationen finden Sie unter [Festlegen der diagrammuhr](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="1f1c8-133">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f1c8-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f1c8-134">Requirements</span></span>



| <span data-ttu-id="1f1c8-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f1c8-135">Requirement</span></span> | <span data-ttu-id="1f1c8-136">Wert</span><span class="sxs-lookup"><span data-stu-id="1f1c8-136">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1c8-137">Header</span><span class="sxs-lookup"><span data-stu-id="1f1c8-137">Header</span></span><br/> | <dl> <span data-ttu-id="1f1c8-138"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1f1c8-138"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f1c8-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f1c8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1c8-140">DirectShow-Bearbeitungs Dienste-Objekte</span><span class="sxs-lookup"><span data-stu-id="1f1c8-140">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




