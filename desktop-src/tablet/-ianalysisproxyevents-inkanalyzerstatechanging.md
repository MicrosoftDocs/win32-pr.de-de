---
description: Tritt auf, bevor die Analyseergebnisse von iinkanalyzer so synchronisiert werden, dass eine Anwendung Daten mit dem iinkanalyzer synchronisieren kann.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: '_IAnalysisProxyEvents:: InkAnalyzerStateChanging-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355731"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a><span data-ttu-id="113d9-103">\_Ianalysisproxyevents:: InkAnalyzerStateChanging-Ereignis</span><span class="sxs-lookup"><span data-stu-id="113d9-103">\_IAnalysisProxyEvents::InkAnalyzerStateChanging event</span></span>

<span data-ttu-id="113d9-104">Tritt auf, bevor die Analyseergebnisse von [**iinkanalyzer**](iinkanalyzer.md) so synchronisiert werden, dass eine Anwendung Daten mit dem **iinkanalyzer** synchronisieren kann.</span><span class="sxs-lookup"><span data-stu-id="113d9-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="113d9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="113d9-105">Syntax</span></span>


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a><span data-ttu-id="113d9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="113d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="113d9-107">*pinkanalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="113d9-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="113d9-108">Der [**iinkanalyzer**](iinkanalyzer.md) , der seine Analyseergebnisse abgleicht.</span><span class="sxs-lookup"><span data-stu-id="113d9-108">The [**IInkAnalyzer**](iinkanalyzer.md) that is about to reconcile its analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="113d9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="113d9-109">Return value</span></span>

<span data-ttu-id="113d9-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="113d9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="113d9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="113d9-111">Remarks</span></span>

<span data-ttu-id="113d9-112">Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="113d9-112">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="113d9-113">Wenn das **iinkanalyzer** -Ereignis dieses Ereignis auslöst, sollte Ihre Anwendung die untergeordneten Knoten des Stamm Knotens der Ink Analyzer Auffüllen (siehe [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) und [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="113d9-113">When the **IInkAnalyzer** raises this event, your application should populate the subnodes of the ink analyzer's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="113d9-114">Das [**iinkanalyzer**](iinkanalyzer.md) -Ereignis löst dieses Ereignis aus, nachdem es das [**\_ ianalysitsvents:: leserytoricile**](-ianalysisevents-readytoreconcile.md) -Ereignis ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="113d9-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event after it raises the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="113d9-115">Dieses Ereignis wird nur ausgelöst, wenn eine Hintergrundanalyse durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="113d9-115">It raises this event only while performing background analysis.</span></span>

<span data-ttu-id="113d9-116">Sperren Sie die Datenstruktur, wenn [**iinkanalyzer**](iinkanalyzer.md) das **\_ ianalysisproxyevents:: InkAnalyzerStateChanging** -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="113d9-116">Lock your data structure when the [**IInkAnalyzer**](iinkanalyzer.md) raises the **\_IAnalysisProxyEvents::InkAnalyzerStateChanging** event.</span></span> <span data-ttu-id="113d9-117">Änderungen an der Datenstruktur während dieser Analysephase können bei der frei Hand Analyse und-Synchronisierung zu Fehlern führen.</span><span class="sxs-lookup"><span data-stu-id="113d9-117">Changes to your data structure during this phase of analysis can cause errors in ink analysis and synchronization.</span></span> <span data-ttu-id="113d9-118">Entsperren Sie Ihre Datenstruktur, wenn **iinkanalyzer** das [**\_ ianalysitsvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) -oder [**\_ ianalysilvents:: results**](-ianalysisevents-results.md) -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="113d9-118">Unlock your data structure when the **IInkAnalyzer** raises the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="113d9-119">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="113d9-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="113d9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="113d9-120">Requirements</span></span>



| <span data-ttu-id="113d9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="113d9-121">Requirement</span></span> | <span data-ttu-id="113d9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="113d9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="113d9-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="113d9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="113d9-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="113d9-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="113d9-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="113d9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="113d9-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="113d9-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="113d9-127">Header</span><span class="sxs-lookup"><span data-stu-id="113d9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="113d9-128"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="113d9-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="113d9-129">DLL</span><span class="sxs-lookup"><span data-stu-id="113d9-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="113d9-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="113d9-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="113d9-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="113d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113d9-132">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="113d9-132">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="113d9-133">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="113d9-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="113d9-134">**Icontextnode**</span><span class="sxs-lookup"><span data-stu-id="113d9-134">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="113d9-135">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="113d9-135">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="113d9-136">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="113d9-136">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="113d9-137">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="113d9-137">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




