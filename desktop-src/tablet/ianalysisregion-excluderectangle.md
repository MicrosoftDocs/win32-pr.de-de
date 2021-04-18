---
description: Schränkt den Bereich von ianalysisregion auf den Teil des Bereichs ein, der das angegebene Rechteck nicht überschneidet.
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'Ianalysisregion:: excluderectangle-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347200"
---
# <a name="ianalysisregionexcluderectangle-method"></a><span data-ttu-id="b4352-103">Ianalysisregion:: excluderectangle-Methode</span><span class="sxs-lookup"><span data-stu-id="b4352-103">IAnalysisRegion::ExcludeRectangle method</span></span>

<span data-ttu-id="b4352-104">Schränkt den Bereich von [**ianalysisregion**](ianalysisregion.md) auf den Teil des Bereichs ein, der das angegebene Rechteck nicht überschneidet.</span><span class="sxs-lookup"><span data-stu-id="b4352-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4352-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4352-105">Syntax</span></span>


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="b4352-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4352-107">*pexcludingrechteck* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4352-107">*pExcludingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4352-108">Das Rechteck, das aus diesem [**ianalysisregion**](ianalysisregion.md)ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4352-108">The rectangle to exclude from this [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4352-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b4352-109">Return value</span></span>

<span data-ttu-id="b4352-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b4352-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4352-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b4352-111">Remarks</span></span>

<span data-ttu-id="b4352-112">Die Rechteck Koordinaten befinden sich in HIMETRIC-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="b4352-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="b4352-113">Wenn sich die beiden Bereiche nicht überschneiden, ist [**ianalysisregion**](ianalysisregion.md) unverändert.</span><span class="sxs-lookup"><span data-stu-id="b4352-113">If the two areas do not intersect, the [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4352-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4352-114">Requirements</span></span>



| <span data-ttu-id="b4352-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4352-115">Requirement</span></span> | <span data-ttu-id="b4352-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b4352-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4352-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b4352-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b4352-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b4352-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b4352-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b4352-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b4352-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b4352-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b4352-121">Header</span><span class="sxs-lookup"><span data-stu-id="b4352-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4352-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b4352-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b4352-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b4352-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4352-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4352-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b4352-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4352-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4352-126">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="b4352-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="b4352-127">**Ianalysisregion:: excluderegion-Methode**</span><span class="sxs-lookup"><span data-stu-id="b4352-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="b4352-128">**Ianalysisregion:: intersectrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="b4352-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="b4352-129">**Ianalysisregion:: intersectregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="b4352-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="b4352-130">**Ianalysisregion:: unionrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="b4352-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="b4352-131">**Ianalysisregion:: unionregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="b4352-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="b4352-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="b4352-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




