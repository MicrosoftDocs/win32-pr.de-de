---
description: Führt eine asynchrone Handschrift Analyse aus.
ms.assetid: 36427b80-5e3b-4c9a-bb49-e6b7f9301cbd
title: 'Iinkanalyzer:: BackgroundAnalyze-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.BackgroundAnalyze
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 606e1444f66884564a6b9f2007adfc26b2eb2ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526504"
---
# <a name="iinkanalyzerbackgroundanalyze-method"></a><span data-ttu-id="22c61-103">Iinkanalyzer:: BackgroundAnalyze-Methode</span><span class="sxs-lookup"><span data-stu-id="22c61-103">IInkAnalyzer::BackgroundAnalyze method</span></span>

<span data-ttu-id="22c61-104">Führt eine asynchrone Handschrift Analyse aus.</span><span class="sxs-lookup"><span data-stu-id="22c61-104">Performs asynchronous ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22c61-105">Syntax</span></span>


```C++
HRESULT BackgroundAnalyze();
```



## <a name="parameters"></a><span data-ttu-id="22c61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22c61-106">Parameters</span></span>

<span data-ttu-id="22c61-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="22c61-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22c61-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22c61-108">Return value</span></span>

<span data-ttu-id="22c61-109">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="22c61-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="22c61-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22c61-110">Remarks</span></span>

<span data-ttu-id="22c61-111">Wenn diese Methode aufgerufen wird, führt [**iinkanalyzer**](iinkanalyzer.md) die Handschrift Analyse in einem Hintergrund Thread aus.</span><span class="sxs-lookup"><span data-stu-id="22c61-111">When this method is called, the [**IInkAnalyzer**](iinkanalyzer.md) performs the ink analysis on a background thread.</span></span>

<span data-ttu-id="22c61-112">Diese Methode gibt **S \_ false** zurück und startet unter den folgenden Umständen keinen neuen Hintergrundanalyse Vorgang.</span><span class="sxs-lookup"><span data-stu-id="22c61-112">This method returns **S\_FALSE** and does not start a new background analysis operation under the following circumstances.</span></span>

-   <span data-ttu-id="22c61-113">[**Iinkanalyzer**](iinkanalyzer.md) führt zurzeit eine Hintergrundanalyse durch.</span><span class="sxs-lookup"><span data-stu-id="22c61-113">The [**IInkAnalyzer**](iinkanalyzer.md) is currently performing background analysis.</span></span>
-   <span data-ttu-id="22c61-114">der geänderte Bereich (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)) stellt einen leeren Bereich dar.</span><span class="sxs-lookup"><span data-stu-id="22c61-114">the dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) represents an empty area.</span></span>

<span data-ttu-id="22c61-115">Der [**iinkanalyzer**](iinkanalyzer.md) analysiert frei Hand Eingaben innerhalb des geänderten Bereichs während eines Aufrufes der [**iinkanalyzer:: Analysis-Methode**](iinkanalyzer-analyze.md) oder der **iinkanalyzer:: BackgroundAnalyze-Methode**.</span><span class="sxs-lookup"><span data-stu-id="22c61-115">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or **IInkAnalyzer::BackgroundAnalyze Method**.</span></span> <span data-ttu-id="22c61-116">Allerdings kann der **iinkanalyzer** den Analyse Vorgang erweitern, um benachbarte Regionen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="22c61-116">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="22c61-117">Diese Methode legt den geänderten Bereich auf einen leeren Bereich fest.</span><span class="sxs-lookup"><span data-stu-id="22c61-117">This method sets the dirty region to an empty region.</span></span>

<span data-ttu-id="22c61-118">Wenn dem [**iinkanalyzer**](iinkanalyzer.md) nach dem Ansichts Vorgang der **iinkanalyzer:: BackgroundAnalyze-Methode** Stroke-Daten hinzugefügt wurden, kann der **iinkanalyzer** den geänderten Bereich während der ababstimmungs Phase der frei Hand Analyse aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="22c61-118">If stroke data was added to the [**IInkAnalyzer**](iinkanalyzer.md) after the call to **IInkAnalyzer::BackgroundAnalyze Method**, the **IInkAnalyzer** may update the dirty region during the reconcile phase of ink analysis.</span></span>

<span data-ttu-id="22c61-119">Die Einstellung für die Analyse Modi (siehe [**iinkanalyzer:: getanalysismodes-Methode**](iinkanalyzer-getanalysismodes.md)) gibt an, wie [**iinkanalyzer**](iinkanalyzer.md) eine Hintergrundanalyse ausführt.</span><span class="sxs-lookup"><span data-stu-id="22c61-119">The analysis modes setting (see [**IInkAnalyzer::GetAnalysisModes Method**](iinkanalyzer-getanalysismodes.md)) specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs background analysis.</span></span> <span data-ttu-id="22c61-120">Weitere Informationen zur frei Hand Analyse finden Sie unter Übersicht über die Handschrift [Analyse](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="22c61-120">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

<span data-ttu-id="22c61-121">Diese Methode gibt unter den folgenden Umständen einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="22c61-121">This method returns an error code under the following circumstances.</span></span>

-   <span data-ttu-id="22c61-122">Die Anwendung hat den [**AnalysisModes**](analysismodes.md) -Wert **AnalysisModes \_** in der [**iinkanalyzer**](iinkanalyzer.md) -Methode festgelegt (siehe [**iinkanalyzer:: setanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md)) und behandelt nicht das [**\_ ianalysisevents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="22c61-122">Your application has set [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_IntermediateResults** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) event.</span></span>
-   <span data-ttu-id="22c61-123">Die Anwendung hat den [**AnalysisModes**](analysismodes.md) -Wert **AnalysisModes \_ automatikreversöhnung** in [**iinkanalyzer**](iinkanalyzer.md) gelöscht (siehe [**iinkanalyzer:: setanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md)) und behandelt nicht das [**\_ ianalysisevents:: Read ytoreconcile**](-ianalysisevents-readytoreconcile.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="22c61-123">Your application has cleared [**AnalysisModes**](analysismodes.md) value **AnalysisModes\_AutomaticReconciliation** in the [**IInkAnalyzer**](iinkanalyzer.md) (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md)) and does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span>
-   <span data-ttu-id="22c61-124">Das [**\_ ianalysisevents:: results**](-ianalysisevents-results.md) -Ereignis wird von der Anwendung nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="22c61-124">Your application does not handle the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>
-   <span data-ttu-id="22c61-125">Das [**\_ ianalysisevents:: updatestrokescache**](-ianalysisevents-updatestrokescache.md) -Ereignis wird von der Anwendung nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="22c61-125">Your application does not handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span>

## <a name="examples"></a><span data-ttu-id="22c61-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="22c61-126">Examples</span></span>

<span data-ttu-id="22c61-127">Im folgenden Beispiel wird der geänderte Bereich der Ink Analyzer überprüft und dann die Hintergrund-Ink-Analyse initiiert, wenn der geänderte Bereich nicht leer ist.</span><span class="sxs-lookup"><span data-stu-id="22c61-127">The following example checks the ink analyzer's dirty region, and then initiates background ink analysis if the dirty region is not empty.</span></span>


```C++
// Check that the ink analyzer's dirty region is not empty.
IAnalysisRegion *pDirtyRegion;
hr = this->m_spIInkAnalyzer->GetDirtyRegion(&pDirtyRegion);

if (SUCCEEDED(hr))
{
    VARIANT_BOOL bIsEmpty;
    hr = pDirtyRegion->IsEmpty(&bIsEmpty);

    if (SUCCEEDED(hr))
    {
        if (!bIsEmpty)
        {
            // Insert code that prepares the application for background
            // ink analysis here.

            // Start background ink analysis. The _IAnalysisEvents::Results
            // event signals when background ink analysis is complete.
            hr = this->m_spIInkAnalyzer->BackgroundAnalyze();
        }
    }
}

// Free the memory for the dirty region.
if (pDirtyRegion != NULL)
{
    pDirtyRegion->Release();
}
```



## <a name="requirements"></a><span data-ttu-id="22c61-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22c61-128">Requirements</span></span>



| <span data-ttu-id="22c61-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22c61-129">Requirement</span></span> | <span data-ttu-id="22c61-130">Wert</span><span class="sxs-lookup"><span data-stu-id="22c61-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22c61-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22c61-131">Minimum supported client</span></span><br/> | <span data-ttu-id="22c61-132">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22c61-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="22c61-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22c61-133">Minimum supported server</span></span><br/> | <span data-ttu-id="22c61-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="22c61-134">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="22c61-135">Header</span><span class="sxs-lookup"><span data-stu-id="22c61-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="22c61-136"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="22c61-136"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="22c61-137">DLL</span><span class="sxs-lookup"><span data-stu-id="22c61-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22c61-138"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22c61-138"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="22c61-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22c61-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c61-140">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="22c61-140">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="22c61-141">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="22c61-141">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="22c61-142">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="22c61-142">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="22c61-143">**Iinkanalyzer:: getanalysismodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="22c61-143">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="22c61-144">**Iinkanalyzer:: abtanalysismodes-Methode**</span><span class="sxs-lookup"><span data-stu-id="22c61-144">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="22c61-145">**Iinkanalyzer:: getdirtyregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="22c61-145">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="22c61-146">**Iinkanalyzer:: setdirtyregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="22c61-146">**IInkAnalyzer::SetDirtyRegion Method**</span></span>](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="22c61-147">**Iinkanalyzer:: GetRootNode-Methode**</span><span class="sxs-lookup"><span data-stu-id="22c61-147">**IInkAnalyzer::GetRootNode Method**</span></span>](iinkanalyzer-getrootnode.md)
</dt> <dt>

[<span data-ttu-id="22c61-148">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="22c61-148">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




