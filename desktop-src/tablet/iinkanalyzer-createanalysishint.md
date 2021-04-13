---
description: Fügt dem iinkanalyzer einen neuen Analyse Hinweis Knoten mit einem unendlichen Bereich hinzu.
ms.assetid: 4cc592c4-456f-4aa5-9a87-d9427de487f3
title: 'Iinkanalyzer:: feateanalysishint-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 041dc1a60c1eeb18d6896a6a23537ac9ebccd321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343708"
---
# <a name="iinkanalyzercreateanalysishint-method"></a><span data-ttu-id="4fa67-103">Iinkanalyzer:: feateanalysishint-Methode</span><span class="sxs-lookup"><span data-stu-id="4fa67-103">IInkAnalyzer::CreateAnalysisHint method</span></span>

<span data-ttu-id="4fa67-104">Fügt dem [**iinkanalyzer**](iinkanalyzer.md)einen neuen Analyse Hinweis Knoten mit einem unendlichen Bereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="4fa67-104">Adds a new analysis hint node with an infinite area to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa67-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fa67-105">Syntax</span></span>


```C++
HRESULT CreateAnalysisHint(
  [out] IContextNode **ppAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="4fa67-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fa67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fa67-107">*ppanalysishint* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4fa67-107">*ppAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fa67-108">Der neue Analyse Hinweis Knoten.</span><span class="sxs-lookup"><span data-stu-id="4fa67-108">The new analysis hint node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fa67-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fa67-109">Return value</span></span>

<span data-ttu-id="4fa67-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md) .</span><span class="sxs-lookup"><span data-stu-id="4fa67-110">See [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md) for a description of the return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fa67-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fa67-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="4fa67-112">Um einen Speicherplatz zu vermeiden, müssen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppanalysishint* aufrufen, wenn Sie das-Objekt nicht mehr verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="4fa67-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHint* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="4fa67-113">Um zusätzliche Kontextinformationen für [**iinkanalyzer**](iinkanalyzer.md)bereitzustellen, können Sie der Ink Analyzer Analyse Hinweise hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4fa67-113">To provide extra context information for the [**IInkAnalyzer**](iinkanalyzer.md), you can add analysis hints to the ink analyzer.</span></span> <span data-ttu-id="4fa67-114">Analyse Hinweise können die Erkennungsgenauigkeit verbessern.</span><span class="sxs-lookup"><span data-stu-id="4fa67-114">Analysis hints can improve recognition accuracy.</span></span> <span data-ttu-id="4fa67-115">Beispielsweise können Sie die Informationen zu "Faktoid" und "Guide" für Felder in einer Formular Anwendung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4fa67-115">For example, you can add factoid and guide information for fields in a form application.</span></span>

<span data-ttu-id="4fa67-116">Diese Methode erstellt einen neuen [**icontextnode**](icontextnode.md) mit dem Kontext Knotentyp AnalysisHint (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)) und fügt den neuen Hinweis als untergeordneten Knoten des Stamm Knotens des [**iinkanalyzer**](iinkanalyzer.md) -Objekts hinzu (siehe [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) und [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md)).</span><span class="sxs-lookup"><span data-stu-id="4fa67-116">This method creates a new [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)) and adds the new hint as a subnode of the [**IInkAnalyzer**](iinkanalyzer.md) object's root node (see [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md) and [**IInkAnalyzer::GetRootNode Method**](iinkanalyzer-getrootnode.md)).</span></span>

<span data-ttu-id="4fa67-117">Wenn Sie dem Hinweis Kontextinformationen hinzufügen möchten, verwenden Sie [**icontextnode:: AddPropertyData**](icontextnode-addpropertydata.md) mit dem Parameter *ppropertydataid* , der auf eine der Eigenschaften Konstanten von [Analysis Hint](analysis-hint-properties.md) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4fa67-117">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="4fa67-118">Wenn ein Hinweis einem unendlichen Bereich zugewiesen wird, der als globaler Hinweis bezeichnet wird, wendet [**iinkanalyzer**](iinkanalyzer.md) den Kontext des Hinweises auf alle frei Hand Eingaben an, die sich nicht im Bereich eines anderen Hinweises befinden.</span><span class="sxs-lookup"><span data-stu-id="4fa67-118">If a hint is assigned an infinite area, termed a global hint, the [**IInkAnalyzer**](iinkanalyzer.md) applies the hint's context to all ink that is not within another hint's area.</span></span> <span data-ttu-id="4fa67-119">An einen einzelnen **iinkanalyzer** können mehrere Hinweise angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4fa67-119">Multiple hints may be attached to a single **IInkAnalyzer**.</span></span> <span data-ttu-id="4fa67-120">Es kann jedoch nur ein globaler Hinweis an einen einzelnen Ink Analyzer angefügt werden, und es können keine nicht globalen Hinweise überlappen.</span><span class="sxs-lookup"><span data-stu-id="4fa67-120">However, only one global hint can be attached to a single ink analyzer, and no non-global hints can overlap.</span></span> <span data-ttu-id="4fa67-121">Weitere Informationen zu den Typen von Kontextinformationen, die von einem Hinweis bereitgestellt werden können, finden Sie unter [Analysis Hint Properties](analysis-hint-properties.md).</span><span class="sxs-lookup"><span data-stu-id="4fa67-121">For more information about the types of context information that a hint can provide, see [Analysis Hint Properties](analysis-hint-properties.md).</span></span>

<span data-ttu-id="4fa67-122">Durch das Hinzufügen eines Analyse Hinweises wird der Bereich des Hinweises für die erneute Analyse nicht markiert.</span><span class="sxs-lookup"><span data-stu-id="4fa67-122">Adding an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="4fa67-123">Um den Bereich innerhalb des Hinweises für die erneute Analyse zu markieren, verwenden Sie die [**iinkanalyzer:: setdirtyregion-Methode**](iinkanalyzer-setdirtyregion.md) , um den geänderten Bereich auf die Vereinigung des aktuellen geänderten Bereichs und Bereichs des Analyse Hinweises festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4fa67-123">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="4fa67-124">Wenn Sie Hinweise für eine Formular Anwendung verwenden, sollte die Anwendung die Mischung aus Text Kontext und Freihand in Formularen vermeiden.</span><span class="sxs-lookup"><span data-stu-id="4fa67-124">When using hints for a form application, the application should avoid mixing text context with ink in the forms.</span></span> <span data-ttu-id="4fa67-125">Dies bedeutet beispielsweise, dass Text Feldnamen nicht in der Analyse Struktur erstellt werden sollten.</span><span class="sxs-lookup"><span data-stu-id="4fa67-125">This means for example that text field names should not be created in the analysis tree.</span></span> <span data-ttu-id="4fa67-126">Hinweise dienen dazu, die frei Hand Eingaben den Bereichen auf Seiten zuzuordnen. Jeder Text Kontext beeinträchtigt diese Ink-to-Hint-Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="4fa67-126">Hints are meant to associate the ink to areas on pages; any text context interferes with this ink-to-hint association.</span></span> <span data-ttu-id="4fa67-127">Der Analyse Vorgang kann die frei Hand Eingabe und den Text Kontext in demselben Schreibbereich zusammenführen, wodurch verhindert wird, dass die frei Hand Eingaben dem Hinweis Bereich zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="4fa67-127">The analysis operation may merge the ink and the text context in the same writing region which would prevent the ink from being associated with the hint area.</span></span>

<span data-ttu-id="4fa67-128">Weitere Informationen zur frei Hand Analyse finden Sie unter Übersicht über die Handschrift [Analyse](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4fa67-128">For more information about ink analysis, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fa67-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fa67-129">Requirements</span></span>



| <span data-ttu-id="4fa67-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fa67-130">Requirement</span></span> | <span data-ttu-id="4fa67-131">Wert</span><span class="sxs-lookup"><span data-stu-id="4fa67-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa67-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fa67-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4fa67-133">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fa67-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4fa67-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fa67-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4fa67-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4fa67-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4fa67-136">Header</span><span class="sxs-lookup"><span data-stu-id="4fa67-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fa67-137"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa67-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4fa67-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4fa67-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fa67-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fa67-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4fa67-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fa67-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa67-141">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="4fa67-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="4fa67-142">**Icontextnode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="4fa67-142">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="4fa67-143">**Iinkanalyzer::D eleteanalysishint-Methode**</span><span class="sxs-lookup"><span data-stu-id="4fa67-143">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="4fa67-144">**Iinkanalyzer:: GetAnalysisHints-Methode**</span><span class="sxs-lookup"><span data-stu-id="4fa67-144">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="4fa67-145">**Iinkanalyzer:: getanalysishintsbyname-Methode**</span><span class="sxs-lookup"><span data-stu-id="4fa67-145">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="4fa67-146">Eigenschaften des Analyse Hinweises</span><span class="sxs-lookup"><span data-stu-id="4fa67-146">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="4fa67-147">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="4fa67-147">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

