---
description: Ruft den Bereich ab, der seit dem letzten Analyse Vorgang geändert wurde.
ms.assetid: 0cd62775-59c6-41f5-957e-709a53a8c257
title: 'Iinkanalyzer:: getdirtyregion-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 56f980189e22f50bb832be904933ef0b26d9b54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214661"
---
# <a name="iinkanalyzergetdirtyregion-method"></a><span data-ttu-id="a1f42-103">Iinkanalyzer:: getdirtyregion-Methode</span><span class="sxs-lookup"><span data-stu-id="a1f42-103">IInkAnalyzer::GetDirtyRegion method</span></span>

<span data-ttu-id="a1f42-104">Ruft den Bereich ab, der seit dem letzten Analyse Vorgang geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a1f42-104">Retrieves the area that has changed since the last analysis operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f42-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1f42-105">Syntax</span></span>


```C++
HRESULT GetDirtyRegion(
  [out] IAnalysisRegion **ppDirtyRegion
);
```



## <a name="parameters"></a><span data-ttu-id="a1f42-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1f42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1f42-107">*ppdirtyregion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a1f42-107">*ppDirtyRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1f42-108">Eine [**ianalysisregion**](ianalysisregion.md) , die den Bereich beschreibt, der seit dem letzten Analyse Vorgang geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a1f42-108">An [**IAnalysisRegion**](ianalysisregion.md) that describes the area that has changed since the last analysis operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1f42-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1f42-109">Return value</span></span>

<span data-ttu-id="a1f42-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a1f42-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1f42-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1f42-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a1f42-112">Um einen Speicherfehler zu vermeiden, nennen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppdirtyregion* , wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="a1f42-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppDirtyRegion* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="a1f42-113">Mit dieser Methode werden die Bereiche identifiziert, die analysiert oder erneut analysiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a1f42-113">This method identifies the areas that need to be analyzed or reanalyzed.</span></span> <span data-ttu-id="a1f42-114">Alle [**iinkanalyzer**](iinkanalyzer.md) -Methoden, die Strich Daten hinzufügen, aktualisieren oder entfernen, aktualisieren den geänderten Bereich.</span><span class="sxs-lookup"><span data-stu-id="a1f42-114">All of the [**IInkAnalyzer**](iinkanalyzer.md) methods that add, update, or remove stroke data update the dirty region.</span></span> <span data-ttu-id="a1f42-115">So markieren Sie einen Bereich manuell für eine erneute Analyse:</span><span class="sxs-lookup"><span data-stu-id="a1f42-115">To manually mark an area for reanalysis:</span></span>

1.  <span data-ttu-id="a1f42-116">Der geänderte Bereich wird mithilfe der **iinkanalyzer:: getdirtyregion-Methode abgerufen**.</span><span class="sxs-lookup"><span data-stu-id="a1f42-116">Get the dirty region using **IInkAnalyzer::GetDirtyRegion Method**.</span></span>
2.  <span data-ttu-id="a1f42-117">Verwenden Sie die [**ianalysisregion:: unionregion-Methode**](ianalysisregion-unionregion.md) oder die [**ianalysisregion:: unionrechteck-Methode**](ianalysisregion-unionrectangle.md) , um den Bereich aus Schritt 1 dem Bereich hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a1f42-117">Use [**IAnalysisRegion::UnionRegion Method**](ianalysisregion-unionregion.md) or [**IAnalysisRegion::UnionRectangle Method**](ianalysisregion-unionrectangle.md) to add the area to the region from step 1.</span></span>
3.  <span data-ttu-id="a1f42-118">Verwenden Sie die [**iinkanalyzer:: setdirtyregion-Methode**](iinkanalyzer-setdirtyregion.md) , um den geänderten Bereich zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a1f42-118">Use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to update the dirty region.</span></span>

<span data-ttu-id="a1f42-119">Der [**iinkanalyzer**](iinkanalyzer.md) analysiert frei Hand Eingaben innerhalb des geänderten Bereichs während eines Aufrufes der [**iinkanalyzer:: Analysis-Methode**](iinkanalyzer-analyze.md) oder der [**iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="a1f42-119">The [**IInkAnalyzer**](iinkanalyzer.md) analyzes ink within its dirty region during a call to [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span> <span data-ttu-id="a1f42-120">Allerdings kann der **iinkanalyzer** den Analyse Vorgang erweitern, um benachbarte Regionen einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="a1f42-120">However, the **IInkAnalyzer** may expand the analysis operation to include neighboring regions.</span></span>

<span data-ttu-id="a1f42-121">Diese Eigenschaft kann nicht benachbarte Bereiche enthalten.</span><span class="sxs-lookup"><span data-stu-id="a1f42-121">This property may contain nonadjacent areas.</span></span>

<span data-ttu-id="a1f42-122">Verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher aus dem *ppdirtyregion* -Array freizugeben, wenn Sie damit fertig sind.</span><span class="sxs-lookup"><span data-stu-id="a1f42-122">Use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to free the memory from the *ppDirtyRegion* array when you are finished with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1f42-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1f42-123">Requirements</span></span>



| <span data-ttu-id="a1f42-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1f42-124">Requirement</span></span> | <span data-ttu-id="a1f42-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a1f42-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f42-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a1f42-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a1f42-127">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a1f42-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a1f42-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a1f42-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a1f42-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a1f42-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a1f42-130">Header</span><span class="sxs-lookup"><span data-stu-id="a1f42-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1f42-131"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a1f42-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a1f42-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a1f42-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1f42-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1f42-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a1f42-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1f42-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f42-135">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="a1f42-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="a1f42-136">**Iinkanalyzer:: analysierungsmethode**</span><span class="sxs-lookup"><span data-stu-id="a1f42-136">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="a1f42-137">**Iinkanalyzer:: BackgroundAnalyze-Methode**</span><span class="sxs-lookup"><span data-stu-id="a1f42-137">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="a1f42-138">**Iinkanalyzer:: AddStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="a1f42-138">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="a1f42-139">**Iinkanalyzer:: addstrokeforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="a1f42-139">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a1f42-140">**Iinkanalyzer:: AddStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="a1f42-140">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="a1f42-141">**Iinkanalyzer:: addstrokesforlanguage-Methode**</span><span class="sxs-lookup"><span data-stu-id="a1f42-141">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="a1f42-142">**Iinkanalyzer:: RemoveStroke-Methode**</span><span class="sxs-lookup"><span data-stu-id="a1f42-142">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="a1f42-143">**Iinkanalyzer:: RemoveStrokes-Methode**</span><span class="sxs-lookup"><span data-stu-id="a1f42-143">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="a1f42-144">**Iinkanalyzer:: UpdateStrokesData-Methode**</span><span class="sxs-lookup"><span data-stu-id="a1f42-144">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="a1f42-145">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="a1f42-145">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

