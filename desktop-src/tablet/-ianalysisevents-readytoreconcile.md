---
description: Tritt auf, wenn iinkanalyzer bereit ist, die Ergebnisse der Hintergrundanalyse mit dem aktuellen Zustand abzustimmen.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: '_IAnalysisEvents:: Read ytor econcile-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219049"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a><span data-ttu-id="a82a8-103">\_Ianalysissevents:: lesereitor-Ereignis</span><span class="sxs-lookup"><span data-stu-id="a82a8-103">\_IAnalysisEvents::ReadyToReconcile event</span></span>

<span data-ttu-id="a82a8-104">Tritt auf, wenn [**iinkanalyzer**](iinkanalyzer.md) bereit ist, die Ergebnisse der Hintergrundanalyse mit dem aktuellen Zustand abzustimmen.</span><span class="sxs-lookup"><span data-stu-id="a82a8-104">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a82a8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a82a8-105">Syntax</span></span>


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a><span data-ttu-id="a82a8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a82a8-106">Parameters</span></span>

<span data-ttu-id="a82a8-107">Dieses Ereignis weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="a82a8-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a82a8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a82a8-108">Return value</span></span>

<span data-ttu-id="a82a8-109">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a82a8-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a82a8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a82a8-110">Remarks</span></span>

<span data-ttu-id="a82a8-111">Der [**iinkanalyzer**](iinkanalyzer.md) führt eine automatische Abstimmung durch, wenn das Flag " **\_ automatisismodes automatianvermittlungs** " des Ink Analyzer festgelegt ist (siehe [**iinkanalyzer:: setanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="a82a8-111">The [**IInkAnalyzer**](iinkanalyzer.md) performs automatic reconciliation when the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag is set (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)).</span></span> <span data-ttu-id="a82a8-112">Wenn das **AnalysisModes \_ automatikreversöhnung** -Flag nicht festgelegt ist, muss Ihre Anwendung die Ergebnisse der Hintergrundanalyse manuell abstimmen.</span><span class="sxs-lookup"><span data-stu-id="a82a8-112">When the **AnalysisModes\_AutomaticReconciliation** flag is not set, your application needs to reconcile background analysis results manually.</span></span>

<span data-ttu-id="a82a8-113">Führen Sie die folgenden Schritte aus, um die manuelle Abstimmung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="a82a8-113">To perform manual reconciliation, follow these steps.</span></span>

1.  <span data-ttu-id="a82a8-114">Löschen Sie das Flag " **automatisismodes \_ automatikredelegat** " der Ink Analyzer.</span><span class="sxs-lookup"><span data-stu-id="a82a8-114">Clear the ink analyzer's **AnalysisModes\_AutomaticReconciliation** flag.</span></span>
2.  <span data-ttu-id="a82a8-115">Behandeln Sie das **\_ ianalysissevents:: leserytoreconcile** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a82a8-115">Handle the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>
3.  <span data-ttu-id="a82a8-116">Um die Analyseergebnisse abzugleichen, müssen Sie die [**Methoden Methode iinkanalyzer::**](iinkanalyzer-reconcile.md) abgestimmt aus dem Ereignishandler für das **\_ ianalysisevents:: Read ytoreconcile** -Ereignis abrufen.</span><span class="sxs-lookup"><span data-stu-id="a82a8-116">To reconcile the analysis results, call the [**IInkAnalyzer::Reconcile Method**](iinkanalyzer-reconcile.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span> <span data-ttu-id="a82a8-117">Um den aktuellen Hintergrundanalyse Vorgang abzubrechen, rufen Sie die [**iinkanalyzer:: Abort-Methoden**](iinkanalyzer-abort.md) Methode aus dem Ereignishandler für das **\_ ianalysisevents:: leserytoreconcile** -Ereignis auf.</span><span class="sxs-lookup"><span data-stu-id="a82a8-117">To cancel the current background analysis operation, call the [**IInkAnalyzer::Abort Method**](iinkanalyzer-abort.md) method from the event handler for the **\_IAnalysisEvents::ReadyToReconcile** event.</span></span>

<span data-ttu-id="a82a8-118">Der [**iinkanalyzer**](iinkanalyzer.md) löst dieses Ereignis aus, bevor es das [**\_ ianalysisproxyevents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="a82a8-118">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event before it raises the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event.</span></span>

<span data-ttu-id="a82a8-119">Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a82a8-119">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="a82a8-120">Der [**iinkanalyzer**](iinkanalyzer.md) löst dieses Ereignis während der Hintergrundanalyse aus.</span><span class="sxs-lookup"><span data-stu-id="a82a8-120">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during background analysis.</span></span>

## <a name="requirements"></a><span data-ttu-id="a82a8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a82a8-121">Requirements</span></span>



| <span data-ttu-id="a82a8-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a82a8-122">Requirement</span></span> | <span data-ttu-id="a82a8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a82a8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a82a8-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a82a8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a82a8-125">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a82a8-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a82a8-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a82a8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a82a8-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a82a8-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a82a8-128">Header</span><span class="sxs-lookup"><span data-stu-id="a82a8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a82a8-129"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a82a8-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a82a8-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a82a8-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a82a8-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a82a8-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a82a8-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a82a8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a82a8-133">**\_Ianalysil Vents**</span><span class="sxs-lookup"><span data-stu-id="a82a8-133">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="a82a8-134">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="a82a8-134">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="a82a8-135">**\_Ianalysisproxyevents**</span><span class="sxs-lookup"><span data-stu-id="a82a8-135">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="a82a8-136">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="a82a8-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a82a8-137">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="a82a8-137">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="a82a8-138">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="a82a8-138">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="a82a8-139">**Iinkanalyzer:: abgestimmt-Methode**</span><span class="sxs-lookup"><span data-stu-id="a82a8-139">**IInkAnalyzer::Reconcile Method**</span></span>](iinkanalyzer-reconcile.md)
</dt> <dt>

[<span data-ttu-id="a82a8-140">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="a82a8-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




