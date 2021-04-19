---
description: Schränkt den Bereich von ianalysisregion auf den Bereich ein, der durch die Schnittmenge mit der angegebenen ianalysisregion erstellt wurde.
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'Ianalysisregion:: intersectregion-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7ff3caad382e54f41685f6102edafdeb86b813c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345126"
---
# <a name="ianalysisregionintersectregion-method"></a><span data-ttu-id="e9811-103">Ianalysisregion:: intersectregion-Methode</span><span class="sxs-lookup"><span data-stu-id="e9811-103">IAnalysisRegion::IntersectRegion method</span></span>

<span data-ttu-id="e9811-104">Schränkt den Bereich von [**ianalysisregion**](ianalysisregion.md) auf den Bereich ein, der durch die Schnittmenge mit der angegebenen **ianalysisregion** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e9811-104">Restricts the area of the [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9811-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9811-105">Syntax</span></span>


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a><span data-ttu-id="e9811-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9811-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9811-107">*pregionintersect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9811-107">*pRegionToIntersect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9811-108">Der [**ianalysisregion**](ianalysisregion.md) , mit der die Schnittmenge gebildet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9811-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to intersect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9811-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e9811-109">Return value</span></span>

<span data-ttu-id="e9811-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e9811-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9811-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9811-111">Remarks</span></span>

<span data-ttu-id="e9811-112">Wenn sich die beiden Bereiche nicht überschneiden, ist der neue Bereich leer.</span><span class="sxs-lookup"><span data-stu-id="e9811-112">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9811-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9811-113">Requirements</span></span>



| <span data-ttu-id="e9811-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9811-114">Requirement</span></span> | <span data-ttu-id="e9811-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e9811-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9811-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e9811-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e9811-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e9811-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e9811-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e9811-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e9811-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e9811-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e9811-120">Header</span><span class="sxs-lookup"><span data-stu-id="e9811-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9811-121"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e9811-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e9811-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e9811-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9811-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9811-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e9811-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9811-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9811-125">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="e9811-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="e9811-126">**Ianalysisregion:: excluderectangle**</span><span class="sxs-lookup"><span data-stu-id="e9811-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="e9811-127">**Ianalysisregion:: excluderegion-Methode**</span><span class="sxs-lookup"><span data-stu-id="e9811-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="e9811-128">**Ianalysisregion:: intersectrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="e9811-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="e9811-129">**Ianalysisregion:: unionrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="e9811-129">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="e9811-130">**Ianalysisregion:: unionregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="e9811-130">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="e9811-131">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="e9811-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




