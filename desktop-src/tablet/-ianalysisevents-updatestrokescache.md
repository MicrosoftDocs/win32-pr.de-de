---
description: Tritt auf, bevor der iinkanalyzer auf Stroke-Daten zugreift.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: '_IAnalysisEvents:: updatestrokescache-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5d16011d8c5fe571d228b632fecb7a973bafcbf5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363045"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a><span data-ttu-id="ef798-103">\_Ianalysil Vents:: updatestrokescache-Ereignis</span><span class="sxs-lookup"><span data-stu-id="ef798-103">\_IAnalysisEvents::UpdateStrokesCache event</span></span>

<span data-ttu-id="ef798-104">Tritt auf, bevor der [**iinkanalyzer**](iinkanalyzer.md) auf Stroke-Daten zugreift.</span><span class="sxs-lookup"><span data-stu-id="ef798-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef798-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef798-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="ef798-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef798-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef798-107">*ulstrokeidscount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef798-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef798-108">Die Anzahl der Stroke-IDs in *plstrokeids*.</span><span class="sxs-lookup"><span data-stu-id="ef798-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="ef798-109">*plstrokeids* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef798-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef798-110">Die Bezeichner der Striche, deren Paketdaten gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="ef798-110">The identifiers of the strokes whose packet data has been cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef798-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef798-111">Return value</span></span>

<span data-ttu-id="ef798-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ef798-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef798-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef798-113">Remarks</span></span>

<span data-ttu-id="ef798-114">Der [**iinkanalyzer**](iinkanalyzer.md) löst dieses Ereignis während der Handschrift Analyse aus, wenn er auf einen oder mehrere Striche zugreift, für die die Paketdaten gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="ef798-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during ink analysis when it accesses one or more strokes for which the packet data has been cleared.</span></span> <span data-ttu-id="ef798-115">Verwenden Sie die [**Methode iinkanalyzer:: UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md) , um die Daten des Stroke-Pakets zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ef798-115">To update the stroke packet data, use the [**IInkAnalyzer::UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) method.</span></span>

<span data-ttu-id="ef798-116">Der [**iinkanalyzer**](iinkanalyzer.md) gibt dieses Ereignis nicht aus, wenn er auf einen teilweise gefüllten frei Hand Blattknoten zugreift, wenn die Position des Knotens nicht durch **iinkanalyzer** festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ef798-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise this event when accessing a partially populated ink leaf node when the location of the node has not been set by the **IInkAnalyzer**.</span></span>

<span data-ttu-id="ef798-117">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ef798-117">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef798-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef798-118">Requirements</span></span>



| <span data-ttu-id="ef798-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef798-119">Requirement</span></span> | <span data-ttu-id="ef798-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ef798-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef798-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef798-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ef798-122">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef798-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ef798-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef798-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ef798-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ef798-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ef798-125">Header</span><span class="sxs-lookup"><span data-stu-id="ef798-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef798-126"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ef798-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ef798-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ef798-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef798-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef798-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ef798-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef798-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef798-130">**\_Ianalysil Vents**</span><span class="sxs-lookup"><span data-stu-id="ef798-130">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="ef798-131">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="ef798-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="ef798-132">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="ef798-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ef798-133">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="ef798-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="ef798-134">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="ef798-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ef798-135">**Iinkanalyzer:: UpdateStrokesData-Methode**</span><span class="sxs-lookup"><span data-stu-id="ef798-135">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="ef798-136">**Icontextnode:: kreatepartiallypopulatedsubnode**</span><span class="sxs-lookup"><span data-stu-id="ef798-136">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="ef798-137">**Icontextnode:: getpartiallyaufgefüllt**</span><span class="sxs-lookup"><span data-stu-id="ef798-137">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="ef798-138">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="ef798-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




