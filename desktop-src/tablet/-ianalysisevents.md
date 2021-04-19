---
description: Gibt Ereignisse an, die den Analyse Schritten eines iinkanalyzer-Objekts zugeordnet sind.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: _IAnalysisEvents-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360681"
---
# <a name="_ianalysisevents-interface"></a><span data-ttu-id="5d5f9-103">\_Ianalysil Vents-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5d5f9-103">\_IAnalysisEvents interface</span></span>

<span data-ttu-id="5d5f9-104">Gibt Ereignisse an, die den Analyse Schritten eines [**iinkanalyzer**](iinkanalyzer.md) -Objekts zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="5d5f9-104">Specifies events associated with the analysis steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="5d5f9-105">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5d5f9-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="5d5f9-106">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="5d5f9-106">Events</span></span>

<span data-ttu-id="5d5f9-107">Die **\_ ianalysil Vents** -Schnittstelle enthält diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="5d5f9-107">The **\_IAnalysisEvents** interface has these events.</span></span>



| <span data-ttu-id="5d5f9-108">Ereignis</span><span class="sxs-lookup"><span data-stu-id="5d5f9-108">Event</span></span>                                                               | <span data-ttu-id="5d5f9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d5f9-109">Description</span></span>                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d5f9-110">**Aktivität**</span><span class="sxs-lookup"><span data-stu-id="5d5f9-110">**Activity**</span></span>](-ianalysisevents-activity.md)                       | <span data-ttu-id="5d5f9-111">Tritt bei Aufrufen der [**iinkanalyzer:: Analysis-Methode**](iinkanalyzer-analyze.md) oder der [**iinkanalyzer:: BackgroundAnalyze-Methoden**](iinkanalyzer-backgroundanalyze.md) Methode auf.</span><span class="sxs-lookup"><span data-stu-id="5d5f9-111">Occurs during calls to the [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method.</span></span><br/> |
| [<span data-ttu-id="5d5f9-112">**IntermediateResults**</span><span class="sxs-lookup"><span data-stu-id="5d5f9-112">**IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md) | <span data-ttu-id="5d5f9-113">Tritt auf, wenn die aktuelle zwischen Analysephase abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5d5f9-113">Occurs when the current intermediate analysis stage is finished.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="5d5f9-114">**"Read ytor econcile"**</span><span class="sxs-lookup"><span data-stu-id="5d5f9-114">**ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)       | <span data-ttu-id="5d5f9-115">Tritt auf, wenn [**iinkanalyzer**](iinkanalyzer.md) bereit ist, die Ergebnisse der Hintergrundanalyse mit dem aktuellen Zustand abzustimmen.</span><span class="sxs-lookup"><span data-stu-id="5d5f9-115">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span><br/>                                                  |
| [<span data-ttu-id="5d5f9-116">**Ergebnisse**</span><span class="sxs-lookup"><span data-stu-id="5d5f9-116">**Results**</span></span>](-ianalysisevents-results.md)                         | <span data-ttu-id="5d5f9-117">Tritt auf, wenn die abschließende Analysephase abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5d5f9-117">Occurs when the final analysis stage is finished.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="5d5f9-118">**Updatestrokescache**</span><span class="sxs-lookup"><span data-stu-id="5d5f9-118">**UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)   | <span data-ttu-id="5d5f9-119">Tritt auf, bevor der [**iinkanalyzer**](iinkanalyzer.md) auf Stroke-Daten zugreift.</span><span class="sxs-lookup"><span data-stu-id="5d5f9-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span><br/>                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="5d5f9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d5f9-120">Requirements</span></span>



| <span data-ttu-id="5d5f9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d5f9-121">Requirement</span></span> | <span data-ttu-id="5d5f9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5d5f9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="5d5f9-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d5f9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5d5f9-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d5f9-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5d5f9-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d5f9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5d5f9-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5d5f9-126">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="5d5f9-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d5f9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d5f9-128">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="5d5f9-128">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="5d5f9-129">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="5d5f9-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5d5f9-130">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="5d5f9-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="5d5f9-131">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="5d5f9-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="5d5f9-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="5d5f9-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

