---
description: Schränkt den Bereich von ianalysisregion auf den Teil des Bereichs ein, der den angegebenen ianalysisregion nicht überschneidet.
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'Ianalysisregion:: excluderegion-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 13324d872a76a9184e6ea67b227dbd7444684bb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526558"
---
# <a name="ianalysisregionexcluderegion-method"></a><span data-ttu-id="50cb9-103">Ianalysisregion:: excluderegion-Methode</span><span class="sxs-lookup"><span data-stu-id="50cb9-103">IAnalysisRegion::ExcludeRegion method</span></span>

<span data-ttu-id="50cb9-104">Schränkt den Bereich von [**ianalysisregion**](ianalysisregion.md) auf den Teil des Bereichs ein, der den angegebenen **ianalysisregion** nicht überschneidet.</span><span class="sxs-lookup"><span data-stu-id="50cb9-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="50cb9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50cb9-105">Syntax</span></span>


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a><span data-ttu-id="50cb9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50cb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50cb9-107">*pregionto Exclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50cb9-107">*pRegionToExclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50cb9-108">Der [**ianalysisregion**](ianalysisregion.md) , der aus dieser **ianalysisregion** ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="50cb9-108">The [**IAnalysisRegion**](ianalysisregion.md) to exclude from this **IAnalysisRegion**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50cb9-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50cb9-109">Return value</span></span>

<span data-ttu-id="50cb9-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="50cb9-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="50cb9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50cb9-111">Remarks</span></span>

<span data-ttu-id="50cb9-112">Wenn sich die beiden Bereiche nicht überschneiden, wird dieser [**ianalysisregion**](ianalysisregion.md) unverändert.</span><span class="sxs-lookup"><span data-stu-id="50cb9-112">If the two areas do not intersect, this [**IAnalysisRegion**](ianalysisregion.md) is unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="50cb9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50cb9-113">Requirements</span></span>



| <span data-ttu-id="50cb9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50cb9-114">Requirement</span></span> | <span data-ttu-id="50cb9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="50cb9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50cb9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50cb9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="50cb9-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50cb9-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="50cb9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50cb9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="50cb9-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="50cb9-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="50cb9-120">Header</span><span class="sxs-lookup"><span data-stu-id="50cb9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="50cb9-121"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="50cb9-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="50cb9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="50cb9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50cb9-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50cb9-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="50cb9-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50cb9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50cb9-125">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="50cb9-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="50cb9-126">**Ianalysisregion:: excluderectangle**</span><span class="sxs-lookup"><span data-stu-id="50cb9-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="50cb9-127">**Ianalysisregion:: intersectrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="50cb9-127">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="50cb9-128">**Ianalysisregion:: intersectregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="50cb9-128">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="50cb9-129">**Ianalysisregion:: unionrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="50cb9-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="50cb9-130">**Ianalysisregion:: unionregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="50cb9-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="50cb9-131">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="50cb9-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




