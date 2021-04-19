---
description: Führt synchrone frei Hand Eingaben aus.
ms.assetid: 957845f3-96b4-4184-aaec-e266cbe47e46
title: 'Iinkanalyzer:: Analysis-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Analyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2867064067b902105508a7742c6fec88fdcd58be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345738"
---
# <a name="iinkanalyzeranalyze-method"></a><span data-ttu-id="02d1e-103">Iinkanalyzer:: analysierungsmethode</span><span class="sxs-lookup"><span data-stu-id="02d1e-103">IInkAnalyzer::Analyze method</span></span>

<span data-ttu-id="02d1e-104">Führt synchrone frei Hand Eingaben aus.</span><span class="sxs-lookup"><span data-stu-id="02d1e-104">Performs synchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d1e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02d1e-105">Syntax</span></span>


```C++
HRESULT Analyze(
  [out] IAnalysisStatus **ppStatus
);
```



## <a name="parameters"></a><span data-ttu-id="02d1e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="02d1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02d1e-107">*ppstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="02d1e-107">*ppStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02d1e-108">Ein Zeiger auf einen [**ianalysisstatus**](ianalysisstatus.md) , der den Status des Analyse Vorgangs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="02d1e-108">A pointer to an [**IAnalysisStatus**](ianalysisstatus.md) that describes the status of the analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02d1e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02d1e-109">Return value</span></span>

<span data-ttu-id="02d1e-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="02d1e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="02d1e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02d1e-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="02d1e-112">Um einen Speicherplatz zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppstatus* , wenn Sie den Analyse Status nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="02d1e-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppStatus* when you no longer need to use the analysis status.</span></span>

 

<span data-ttu-id="02d1e-113">Diese Methode startet einen Vorgang für die synchrone frei Hand Eingabe.</span><span class="sxs-lookup"><span data-stu-id="02d1e-113">This method starts a synchronous ink analysis operation.</span></span> <span data-ttu-id="02d1e-114">Die frei Hand Analyse umfasst layoutanalysen, schreiben und Zeichnen von Klassifizierungen und Handschrifterkennung.</span><span class="sxs-lookup"><span data-stu-id="02d1e-114">Ink analysis includes layout analysis, writing and drawing classification, and handwriting recognition.</span></span> <span data-ttu-id="02d1e-115">Diese Methode gibt zurück, nachdem der Analyse Vorgang beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="02d1e-115">This method returns after the analysis operation is complete.</span></span>

<span data-ttu-id="02d1e-116">Diese Methode gibt einen **E- \_ Zeiger** zurück, wenn *ppstatus* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="02d1e-116">This method returns **E\_POINTER** if *ppStatus* is **NULL**.</span></span>

<span data-ttu-id="02d1e-117">Während eines Aufrufens der **iinkanalyzer:: Analysis-Methode** oder der [**iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)analysiert [**iinkanalyzer**](iinkanalyzer.md) frei Hand Eingaben innerhalb des geänderten Bereichs (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="02d1e-117">During a call to **IInkAnalyzer::Analyze Method** or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md), the [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span> <span data-ttu-id="02d1e-118">Allerdings kann der **iinkanalyzer** den Analyse Vorgang erweitern, um benachbarte Regionen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="02d1e-118">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="02d1e-119">Diese Methode legt den geänderten Bereich des [**iinkanalyzer**](iinkanalyzer.md) -Objekts auf einen leeren Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="02d1e-119">This method sets the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region to an empty region.</span></span> <span data-ttu-id="02d1e-120">Wenn von einem anderen Thread noch nicht analysierte Stroke-Daten hinzugefügt wurden, fügt **iinkanalyzer** das umgebende Feld der nicht analysierten Striche während der ababstimmungs Phase der Analyse dem geänderten Bereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="02d1e-120">If another thread has added stroke data that has not been analyzed, the **IInkAnalyzer** adds the bounding box of the unanalyzed strokes to its dirty region during the reconcile phase of the analysis.</span></span>

<span data-ttu-id="02d1e-121">Diese Methode gibt einen Fehler zurück, wenn die Anwendung das [**\_ ianalysisevents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md) -Ereignis nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="02d1e-121">This method returns an error if your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

<span data-ttu-id="02d1e-122">Der [**iinkanalyzer**](iinkanalyzer.md) gibt nicht die [**\_ ianalysitsvents:: results**](-ianalysisevents-results.md) -und [**\_ ianalysitsvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) -Ereignisse als Reaktion auf diese Methode aus.</span><span class="sxs-lookup"><span data-stu-id="02d1e-122">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) and [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) events in response to this method.</span></span>

<span data-ttu-id="02d1e-123">Verwenden Sie die [**iinkanalyzer:: setanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md), um die Art der Datenflussanalyse zu ändern</span><span class="sxs-lookup"><span data-stu-id="02d1e-123">To modify the way ink analysis is performed, use [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md).</span></span>

<span data-ttu-id="02d1e-124">Weitere Informationen zur frei Hand Analyse finden Sie unter Übersicht über die Handschrift [Analyse](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="02d1e-124">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="02d1e-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02d1e-125">Examples</span></span>

<span data-ttu-id="02d1e-126">Das folgende Beispiel führt eine Vordergrund-Ink-Analyse durch</span><span class="sxs-lookup"><span data-stu-id="02d1e-126">The following example performs foreground ink analysis.</span></span>


```C++
// Perform synchronous ink analysis.
IAnalysisStatus *pAnalysisStatus = NULL;
hr = this->m_spIInkAnalyzer->Analyze(&pAnalysisStatus);

if (SUCCEEDED(hr))
{
    // Insert code that processes the analysis results.
}

// Release this reference to the analysis status.
if (pAnalysisStatus != NULL)
{
    pAnalysisStatus->Release();
    pAnalysisStatus = NULL;
}
```



## <a name="requirements"></a><span data-ttu-id="02d1e-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02d1e-127">Requirements</span></span>



| <span data-ttu-id="02d1e-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02d1e-128">Requirement</span></span> | <span data-ttu-id="02d1e-129">Wert</span><span class="sxs-lookup"><span data-stu-id="02d1e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02d1e-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02d1e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="02d1e-131">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02d1e-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="02d1e-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02d1e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="02d1e-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="02d1e-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="02d1e-134">Header</span><span class="sxs-lookup"><span data-stu-id="02d1e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="02d1e-135"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="02d1e-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="02d1e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="02d1e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02d1e-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02d1e-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="02d1e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02d1e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d1e-139">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="02d1e-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="02d1e-140">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="02d1e-140">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="02d1e-141">**Iinkanalyzer:: getdirtyregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="02d1e-141">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="02d1e-142">**Iinkanalyzer:: setdirtyregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="02d1e-142">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="02d1e-143">**Iinkanalyzer:: GetRootNode-Methode**</span><span class="sxs-lookup"><span data-stu-id="02d1e-143">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="02d1e-144">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="02d1e-144">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> </dl>

 

