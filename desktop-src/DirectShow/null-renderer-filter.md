---
description: Der Nullrendererfilter ist ein Renderer, der jedes empfangene Beispiel verwirft, ohne die Beispieldaten anzuzeigen oder zu rendern.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: NULL-Rendererfilter (Qedit.h)
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
ms.openlocfilehash: 64647cbcbcc836c400890fb173a29c76f8723029
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908808"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="2a4f0-103">NULL-Rendererfilter</span><span class="sxs-lookup"><span data-stu-id="2a4f0-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="2a4f0-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="2a4f0-104">\[Deprecated.</span></span> <span data-ttu-id="2a4f0-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="2a4f0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2a4f0-106">Der Nullrendererfilter ist ein Renderer, der jedes empfangene Beispiel verwirft, ohne die Beispieldaten anzuzeigen oder zu rendern.</span><span class="sxs-lookup"><span data-stu-id="2a4f0-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



| <span data-ttu-id="2a4f0-107">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="2a4f0-107">Label</span></span> | <span data-ttu-id="2a4f0-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2a4f0-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a4f0-109">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="2a4f0-109">Filter interfaces</span></span>                        | <span data-ttu-id="2a4f0-110">[**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="2a4f0-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="2a4f0-111">Eingabepinmedientypen</span><span class="sxs-lookup"><span data-stu-id="2a4f0-111">Input pin media types</span></span>                    | <span data-ttu-id="2a4f0-112">Beliebiger Medientyp</span><span class="sxs-lookup"><span data-stu-id="2a4f0-112">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="2a4f0-113">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="2a4f0-113">Input pin interfaces</span></span>                     | <span data-ttu-id="2a4f0-114">[**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="2a4f0-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="2a4f0-115">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="2a4f0-115">Output pin media types</span></span>                   | <span data-ttu-id="2a4f0-116">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="2a4f0-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="2a4f0-117">Ausgabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="2a4f0-117">Output pin interfaces</span></span>                    | <span data-ttu-id="2a4f0-118">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="2a4f0-118">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="2a4f0-119">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="2a4f0-119">Filter CLSID</span></span>                             | <span data-ttu-id="2a4f0-120">CLSID \_ NullRenderer</span><span class="sxs-lookup"><span data-stu-id="2a4f0-120">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="2a4f0-121">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="2a4f0-121">Property Page CLSID</span></span>                      | <span data-ttu-id="2a4f0-122">Keine Eigenschaftenseite.</span><span class="sxs-lookup"><span data-stu-id="2a4f0-122">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="2a4f0-123">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="2a4f0-123">Executable</span></span>                               | <span data-ttu-id="2a4f0-124">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="2a4f0-124">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="2a4f0-125">Verdienst</span><span class="sxs-lookup"><span data-stu-id="2a4f0-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="2a4f0-126">NICHT \_ \_ VERWENDEN \_</span><span class="sxs-lookup"><span data-stu-id="2a4f0-126">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="2a4f0-127">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="2a4f0-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="2a4f0-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="2a4f0-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="2a4f0-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a4f0-129">Remarks</span></span>

<span data-ttu-id="2a4f0-130">Verwenden Sie diesen Filter, wenn ein Ausgabepin im Diagramm eine Downstreamverbindung erfordert, Sie die Daten jedoch nicht von diesem Pin rendern möchten.</span><span class="sxs-lookup"><span data-stu-id="2a4f0-130">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="2a4f0-131">Indem Sie den Ausgabepin mit dem NULL-Renderer verbinden, schließen Sie die Verbindung ab, ohne die Daten zu rendern.</span><span class="sxs-lookup"><span data-stu-id="2a4f0-131">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="2a4f0-132">Obwohl dieser Filter keine Stichproben rendert, wartet er auf die Präsentationszeit der einzelnen Stichproben, bevor das Beispiel verworfen wird.</span><span class="sxs-lookup"><span data-stu-id="2a4f0-132">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="2a4f0-133">Daher wird das Diagramm mit der normalen Rate ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a4f0-133">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="2a4f0-134">Wenn das Diagramm so schnell wie möglich ausgeführt werden soll, legen Sie die Referenzuhr auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="2a4f0-134">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="2a4f0-135">Weitere Informationen finden Sie unter [Setting the Graph Clock](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="2a4f0-135">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a4f0-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a4f0-136">Requirements</span></span>



| <span data-ttu-id="2a4f0-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a4f0-137">Requirement</span></span> | <span data-ttu-id="2a4f0-138">Wert</span><span class="sxs-lookup"><span data-stu-id="2a4f0-138">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a4f0-139">Header</span><span class="sxs-lookup"><span data-stu-id="2a4f0-139">Header</span></span><br/> | <dl> <span data-ttu-id="2a4f0-140"><dt>Qedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="2a4f0-140"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a4f0-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a4f0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a4f0-142">DirectShow Editing Services Objects</span><span class="sxs-lookup"><span data-stu-id="2a4f0-142">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




