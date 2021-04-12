---
description: Ändert den Bereich, der seit dem letzten Analyse Vorgang geändert wurde.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'Iinkanalyzer:: setdirtyregion-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 72278dd9fe1d772d4ef340d25694d42f9c48ed7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129440"
---
# <a name="iinkanalyzersetdirtyregion-method"></a><span data-ttu-id="5f1b5-103">Iinkanalyzer:: setdirtyregion-Methode</span><span class="sxs-lookup"><span data-stu-id="5f1b5-103">IInkAnalyzer::SetDirtyRegion method</span></span>

<span data-ttu-id="5f1b5-104">Ändert den Bereich, der seit dem letzten Analyse Vorgang geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f1b5-104">Modifies the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f1b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f1b5-105">Syntax</span></span>


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="5f1b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f1b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f1b5-107">*pdirtyregion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f1b5-107">*pDirtyRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f1b5-108">Eine [**ianalysisregion**](ianalysisregion.md) , die den Bereich beschreibt, der seit dem letzten Analyse Vorgang geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5f1b5-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f1b5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f1b5-109">Return value</span></span>

<span data-ttu-id="5f1b5-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5f1b5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5f1b5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f1b5-111">Remarks</span></span>

<span data-ttu-id="5f1b5-112">Mit dieser Methode werden die Bereiche identifiziert, die analysiert oder erneut analysiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5f1b5-112">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="5f1b5-113">Alle [**iinkanalyzer**](iinkanalyzer.md) -Methoden, die Strich Daten hinzufügen, aktualisieren oder entfernen, aktualisieren den geänderten Bereich.</span><span class="sxs-lookup"><span data-stu-id="5f1b5-113">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="5f1b5-114">So markieren Sie einen Bereich manuell für eine erneute Analyse:</span><span class="sxs-lookup"><span data-stu-id="5f1b5-114">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="5f1b5-115">Der geänderte Bereich wird mithilfe der [**iinkanalyzer:: getdirtyregion-Methode abgerufen**](iinkanalyzer-getdirtyregion.md).</span><span class="sxs-lookup"><span data-stu-id="5f1b5-115">Get the dirty region using [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md).</span></span>
2.  <span data-ttu-id="5f1b5-116">Verwenden Sie die [**ianalysisregion:: unionregion-Methode**](ianalysisregion-unionregion.md) oder die [**ianalysisregion:: unionrechteck-Methode**](ianalysisregion-unionrectangle.md) , um den Bereich aus Schritt 1 dem Bereich hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5f1b5-116">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="5f1b5-117">Verwenden Sie die **iinkanalyzer:: setdirtyregion-Methode** , um den geänderten Bereich zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5f1b5-117">Use **IInkAnalyzer::SetDirtyRegion Method** to update the dirty region.</span></span>

<span data-ttu-id="5f1b5-118">Der [**iinkanalyzer**](iinkanalyzer.md) analysiert frei Hand Eingaben innerhalb des geänderten Bereichs während eines Aufrufes der [**iinkanalyzer:: Analysis-Methode**](iinkanalyzer-analyze.md) oder der [**iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="5f1b5-118">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="5f1b5-119">Allerdings kann der **iinkanalyzer** den Analyse Vorgang erweitern, um benachbarte Regionen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="5f1b5-119">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f1b5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f1b5-120">Requirements</span></span>



| <span data-ttu-id="5f1b5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f1b5-121">Requirement</span></span> | <span data-ttu-id="5f1b5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5f1b5-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1b5-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5f1b5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5f1b5-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5f1b5-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5f1b5-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5f1b5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5f1b5-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5f1b5-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5f1b5-127">Header</span><span class="sxs-lookup"><span data-stu-id="5f1b5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f1b5-128"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5f1b5-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5f1b5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5f1b5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f1b5-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f1b5-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5f1b5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f1b5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f1b5-132">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="5f1b5-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5f1b5-133">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="5f1b5-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="5f1b5-134">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="5f1b5-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="5f1b5-135">**Iinkanalyzer:: AddStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="5f1b5-135">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="5f1b5-136">**Iinkanalyzer:: addstrokeforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="5f1b5-136">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="5f1b5-137">**Iinkanalyzer:: AddStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="5f1b5-137">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="5f1b5-138">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="5f1b5-138">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="5f1b5-139">**Iinkanalyzer:: RemoveStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="5f1b5-139">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="5f1b5-140">**Iinkanalyzer:: RemoveStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="5f1b5-140">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="5f1b5-141">**Iinkanalyzer:: UpdateStrokesData-Methode**</span><span class="sxs-lookup"><span data-stu-id="5f1b5-141">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="5f1b5-142">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="5f1b5-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




