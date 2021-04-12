---
description: Entfernt einen Analyse Hinweis aus iinkanalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: Iinkanalyzer::D eleteanalysishint-Methode (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129468"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a><span data-ttu-id="62862-103">Iinkanalyzer::D eleteanalysishint-Methode</span><span class="sxs-lookup"><span data-stu-id="62862-103">IInkAnalyzer::DeleteAnalysisHint method</span></span>

<span data-ttu-id="62862-104">Entfernt einen Analyse Hinweis aus [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="62862-104">Removes an analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="62862-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62862-105">Syntax</span></span>


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="62862-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="62862-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62862-107">*phintto DELETE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62862-107">*pHintToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62862-108">Der Analyse Hinweis von [**iinkanalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="62862-108">The analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62862-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62862-109">Return value</span></span>

<span data-ttu-id="62862-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="62862-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="62862-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62862-111">Remarks</span></span>

<span data-ttu-id="62862-112">Durch das Entfernen eines Analyse Hinweises wird der Bereich des Hinweises für die erneute Analyse nicht markiert.</span><span class="sxs-lookup"><span data-stu-id="62862-112">Removing an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="62862-113">Um den Bereich innerhalb des Hinweises für die erneute Analyse zu markieren, verwenden Sie die [**iinkanalyzer:: setdirtyregion-Methode**](iinkanalyzer-setdirtyregion.md) , um den geänderten Bereich auf die Vereinigung des aktuellen geänderten Bereichs und Bereichs des Analyse Hinweises festzulegen.</span><span class="sxs-lookup"><span data-stu-id="62862-113">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="62862-114">Der Hinweis wird aus dem Analyzer entfernt. der [**icontextnode**](icontextnode.md) selbst wird jedoch nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="62862-114">The hint is removed from the analyzer; however, the [**IContextNode**](icontextnode.md) itself is not deleted.</span></span>

<span data-ttu-id="62862-115">Diese Methode gibt einen Fehlercode zurück, wenn ' *phintdedelete* ' ein [**icontextnode**](icontextnode.md) ist, der nicht vom Typ ' AnalysisHint ' ist (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="62862-115">This method returns an error code when *pHintToDelete* is a [**IContextNode**](icontextnode.md) that is not of type AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="62862-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62862-116">Requirements</span></span>



| <span data-ttu-id="62862-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62862-117">Requirement</span></span> | <span data-ttu-id="62862-118">Wert</span><span class="sxs-lookup"><span data-stu-id="62862-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62862-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62862-119">Minimum supported client</span></span><br/> | <span data-ttu-id="62862-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62862-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="62862-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62862-121">Minimum supported server</span></span><br/> | <span data-ttu-id="62862-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="62862-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="62862-123">Header</span><span class="sxs-lookup"><span data-stu-id="62862-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="62862-124"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="62862-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="62862-125">DLL</span><span class="sxs-lookup"><span data-stu-id="62862-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62862-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62862-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="62862-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62862-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62862-128">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="62862-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="62862-129">**Iinkanalyzer:: feateanalysishint-Methode**</span><span class="sxs-lookup"><span data-stu-id="62862-129">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="62862-130">**Iinkanalyzer:: GetAnalysisHints-Methode**</span><span class="sxs-lookup"><span data-stu-id="62862-130">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="62862-131">**Iinkanalyzer:: getanalysishintsbyname-Methode**</span><span class="sxs-lookup"><span data-stu-id="62862-131">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="62862-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="62862-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




