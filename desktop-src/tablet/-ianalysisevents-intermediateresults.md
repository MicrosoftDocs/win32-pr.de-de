---
description: Tritt auf, wenn die aktuelle zwischen Analysephase abgeschlossen ist.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: '_IAnalysisEvents:: IntermediateResults-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355732"
---
# <a name="_ianalysiseventsintermediateresults-event"></a><span data-ttu-id="a8f33-103">\_Ianalysilvents:: IntermediateResults-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a8f33-103">\_IAnalysisEvents::IntermediateResults event</span></span>

<span data-ttu-id="a8f33-104">Tritt auf, wenn die aktuelle zwischen Analysephase abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a8f33-104">Occurs when the current intermediate analysis stage is finished.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f33-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8f33-105">Syntax</span></span>


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a8f33-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8f33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f33-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8f33-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f33-108">Der [**iinkanalyzer**](iinkanalyzer.md) , der die Analyse ausführt.</span><span class="sxs-lookup"><span data-stu-id="a8f33-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is performing the analysis.</span></span>

</dd> <dt>

<span data-ttu-id="a8f33-109">*panalysisstatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8f33-109">*pAnalysisStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f33-110">Das [**ianalysisstatus**](ianalysisstatus.md) -Objekt, das den Status der Zwischenergebnisse darstellt.</span><span class="sxs-lookup"><span data-stu-id="a8f33-110">The [**IAnalysisStatus**](ianalysisstatus.md) object representing the status of the intermediate results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f33-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8f33-111">Return value</span></span>

<span data-ttu-id="a8f33-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a8f33-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f33-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8f33-113">Remarks</span></span>

<span data-ttu-id="a8f33-114">Das [**iinkanalyzer**](iinkanalyzer.md) -Ereignis löst dieses Ereignis aus, nachdem es die Zwischenergebnisse für die aktuelle Analysephase abgestimmt hat.</span><span class="sxs-lookup"><span data-stu-id="a8f33-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it has reconciled the intermediate results for the current analysis stage.</span></span>

<span data-ttu-id="a8f33-115">Wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird, weist dieses Ereignis darauf hin, dass der **iinkanalyzer** seine internen Daten für diese Analysephase geändert hat.</span><span class="sxs-lookup"><span data-stu-id="a8f33-115">If your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), this event indicates that the **IInkAnalyzer** has finished making changes to its internal data for this analysis stage.</span></span>

<span data-ttu-id="a8f33-116">Sperren Sie die Datenstruktur, wenn [**iinkanalyzer**](iinkanalyzer.md) das [**\_ ianalysisproxyevents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="a8f33-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span> <span data-ttu-id="a8f33-117">Änderungen an der Datenstruktur während dieser Analysephase können bei der frei Hand Analyse und-Synchronisierung zu Fehlern führen.</span><span class="sxs-lookup"><span data-stu-id="a8f33-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="a8f33-118">Sie können ihre Datenstruktur entsperren, wenn **iinkanalyzer** das **\_ ianalysitsvents:: IntermediateResults** -oder [**\_ ianalysilvents:: results**](-ianalysisevents-results.md) -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="a8f33-118">You can unlock your data structure when the **IInkAnalyzer** raises the **\_IAnalysisEvents::IntermediateResults** or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="a8f33-119">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a8f33-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="a8f33-120">Der [**iinkanalyzer**](iinkanalyzer.md) generiert nur dann Zwischenergebnisse, wenn für den Analysemodus das **AnalysisModes-Flag " \_ IntermediateResults** " festgelegt ist (siehe [**iinkanalyzer:: getanalysismodes-Methode**](iinkanalyzer-getanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="a8f33-120">The [**IInkAnalyzer**](iinkanalyzer.md) generates intermediate results only when its analysis modes has the **AnalysisModes\_IntermediateResults** flag set (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f33-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8f33-121">Requirements</span></span>



| <span data-ttu-id="a8f33-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8f33-122">Requirement</span></span> | <span data-ttu-id="a8f33-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a8f33-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f33-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8f33-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f33-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8f33-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a8f33-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8f33-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f33-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a8f33-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a8f33-128">Header</span><span class="sxs-lookup"><span data-stu-id="a8f33-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8f33-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a8f33-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a8f33-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a8f33-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8f33-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8f33-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a8f33-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8f33-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f33-133">**\_Ianalysil Vents**</span><span class="sxs-lookup"><span data-stu-id="a8f33-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="a8f33-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="a8f33-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="a8f33-135">**\_Ianalysil Vents:: results**</span><span class="sxs-lookup"><span data-stu-id="a8f33-135">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="a8f33-136">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="a8f33-136">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="a8f33-137">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="a8f33-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a8f33-138">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="a8f33-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="a8f33-139">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="a8f33-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="a8f33-140">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="a8f33-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>
