---
description: Bricht den aktuellen Analyse Vorgang ab.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: 'Iinkanalyzer:: Abort-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eac96809bfbe41e7d6a070782da3ffd0f6407c60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349013"
---
# <a name="iinkanalyzerabort-method"></a><span data-ttu-id="0af84-103">Iinkanalyzer:: Abort-Methode</span><span class="sxs-lookup"><span data-stu-id="0af84-103">IInkAnalyzer::Abort method</span></span>

<span data-ttu-id="0af84-104">Bricht den aktuellen Analyse Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="0af84-104">Cancels the current analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0af84-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0af84-105">Syntax</span></span>


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="0af84-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0af84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0af84-107">*ppabortedregion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0af84-107">*ppAbortedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0af84-108">Ein Zeiger auf einen [**ianalysisregion**](ianalysisregion.md) , der den geänderten Bereich darstellt (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)) des aktuellen Analyse Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0af84-108">A pointer to an [**IAnalysisRegion**](ianalysisregion.md) that represents the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) of the current analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0af84-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0af84-109">Return value</span></span>

<span data-ttu-id="0af84-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0af84-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0af84-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0af84-111">Remarks</span></span>

<span data-ttu-id="0af84-112">Nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppabortedregion* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="0af84-112">Call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAbortedRegion* when you no longer need to use the object.</span></span>

<span data-ttu-id="0af84-113">Mit dieser Methode wird der aktuelle Analyse Vorgang abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="0af84-113">This method cancels the current analysis operation.</span></span>

<span data-ttu-id="0af84-114">Wenn *ppabortedregion* den Wert **null** hat, führt diese Methode den Abbruch wie üblich aus, da dies darauf hinweist, dass der Aufrufer keinen Interesse am Rückgabewert hat.</span><span class="sxs-lookup"><span data-stu-id="0af84-114">When *ppAbortedRegion* is **NULL**, this method performs the abort as normal, because this indicates that the caller has no interest in the return value.</span></span>

<span data-ttu-id="0af84-115">Die **iinkanalyzer:: Abort-Methode** deaktiviert die [**\_ ianalysisevents:: results**](-ianalysisevents-results.md) -und [**\_ ianalysisevents:: Activity**](-ianalysisevents-activity.md) -Ereignisse für den aktuellen Analyse Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0af84-115">**IInkAnalyzer::Abort Method** silences the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::Activity**](-ianalysisevents-activity.md) events for the current analysis operation.</span></span>

<span data-ttu-id="0af84-116">Die **iinkanalyzer:: Abort-Methode** wird asynchron ausgeführt, bis der aktuelle Hintergrundanalyse Vorgang abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="0af84-116">**IInkAnalyzer::Abort Method** runs asynchronously until the current background analysis operation is canceled.</span></span> <span data-ttu-id="0af84-117">Da der abbruchprozess asynchron ist, kann die Anwendung andere Aufgaben ausführen, während die aktuellen Analyse Operations abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="0af84-117">Because the cancellation process is asynchronous, the application can perform other tasks while the current analysis opertions is canceled.</span></span>

<span data-ttu-id="0af84-118">Wenn keine Analyse Vorgänge ausgeführt werden, gibt diese Methode einen leeren Analysebereich zurück.</span><span class="sxs-lookup"><span data-stu-id="0af84-118">If no analysis operations are in progress, this method returns an empty analysis region.</span></span>

<span data-ttu-id="0af84-119">Wenn ein Analyse Vorgang ausgeführt wird, bricht diese Methode den Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="0af84-119">If one analysis operation is in progress, this method cancels the operation.</span></span>

<span data-ttu-id="0af84-120">Wenn synchrone und asynchrone Analyse Vorgänge ausgeführt werden, bricht diese Methode den synchronen Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="0af84-120">If both synchronous and asynchronous analysis operations are in progress, this method cancels the synchronous operation.</span></span>

<span data-ttu-id="0af84-121">Wenn diese Methode mehrmals für denselben Analyse Vorgang aufgerufen wird, gibt der erste Aufruf den geänderten Bereich für den Vorgang zurück, und die nachfolgenden Aufrufe geben einen leeren Bereich zurück.</span><span class="sxs-lookup"><span data-stu-id="0af84-121">If this method is called more than once for the same analysis operation, the first call returns the dirty region for the operation, and the subsequent calls return an empty region.</span></span>

<span data-ttu-id="0af84-122">Wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert ist, kann durch das Aufrufen der **iinkanalyzer:: Abort-Methode** das Dokument mit partiellen Ergebnissen belassen werden.</span><span class="sxs-lookup"><span data-stu-id="0af84-122">If your application maintains its own data structure that is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md), calling **IInkAnalyzer::Abort Method** can leave your document with partial results.</span></span> <span data-ttu-id="0af84-123">Um dies zu vermeiden, müssen Sie die **iinkanalyzer:: Abort-Methode** nicht zwischen dem Zeitpunkt aufrufen, an dem der **iinkanalyzer** das [**\_ ianalysisproxyevents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) -Ereignis empfängt, und dem Zeitpunkt, an dem **iinkanalyzer** das [**\_ ianalysitsvents::**](-ianalysisevents-intermediateresults.md) - [**\_ results**](-ianalysisevents-results.md) -Ereignis empfängt.</span><span class="sxs-lookup"><span data-stu-id="0af84-123">To avoid this, do not call **IInkAnalyzer::Abort Method** between the time the **IInkAnalyzer** receives the [**\_IAnalysisProxyEvents::InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) event and the time the **IInkAnalyzer** receives the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) or [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

<span data-ttu-id="0af84-124">Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit der Ink Analyzer finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0af84-124">For more information about synchronizing your application data with the ink analyzer, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0af84-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0af84-125">Requirements</span></span>



| <span data-ttu-id="0af84-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0af84-126">Requirement</span></span> | <span data-ttu-id="0af84-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0af84-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0af84-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0af84-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0af84-129">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0af84-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0af84-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0af84-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0af84-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0af84-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0af84-132">Header</span><span class="sxs-lookup"><span data-stu-id="0af84-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0af84-133"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0af84-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0af84-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0af84-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0af84-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0af84-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0af84-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0af84-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0af84-137">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="0af84-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="0af84-138">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="0af84-138">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="0af84-139">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="0af84-139">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="0af84-140">**Iinkanalyzer:: getdirtyregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="0af84-140">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="0af84-141">**Iinkanalyzer:: setdirtyregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="0af84-141">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="0af84-142">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="0af84-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

