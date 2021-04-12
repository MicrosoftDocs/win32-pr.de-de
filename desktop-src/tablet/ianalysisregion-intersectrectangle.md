---
description: Schränkt den Bereich dieses ianalysisregion auf den Bereich ein, der durch die Schnittmenge mit dem angegebenen Rechteck erstellt wurde.
ms.assetid: de6b565f-34c1-4551-ab92-db6bacb8608d
title: 'Ianalysisregion:: intersectrechteck-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4ce0e514b24aba0331d9ea604333680db1c67c8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526555"
---
# <a name="ianalysisregionintersectrectangle-method"></a><span data-ttu-id="22101-103">Ianalysisregion:: intersectrechteck-Methode</span><span class="sxs-lookup"><span data-stu-id="22101-103">IAnalysisRegion::IntersectRectangle method</span></span>

<span data-ttu-id="22101-104">Schränkt den Bereich dieses [**ianalysisregion**](ianalysisregion.md) auf den Bereich ein, der durch die Schnittmenge mit dem angegebenen Rechteck erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="22101-104">Restricts the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its intersection with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="22101-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="22101-105">Syntax</span></span>


```C++
HRESULT IntersectRectangle(
  [in] RECT *pIntersectingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="22101-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="22101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22101-107">*pintersectingrechteck* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22101-107">*pIntersectingRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22101-108">Ein Zeiger auf das Rechteck, mit dem die Schnittmenge in Freihand Raumkoordinaten gebildet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22101-108">A pointer to the rectangle with which to intersect, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22101-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22101-109">Return value</span></span>

<span data-ttu-id="22101-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="22101-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="22101-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22101-111">Remarks</span></span>

<span data-ttu-id="22101-112">Die Rechteck Koordinaten befinden sich in HIMETRIC-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="22101-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="22101-113">Wenn sich die beiden Bereiche nicht überschneiden, ist der neue Bereich leer.</span><span class="sxs-lookup"><span data-stu-id="22101-113">If the two areas do not intersect, the new area is empty.</span></span>

## <a name="requirements"></a><span data-ttu-id="22101-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22101-114">Requirements</span></span>



| <span data-ttu-id="22101-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22101-115">Requirement</span></span> | <span data-ttu-id="22101-116">Wert</span><span class="sxs-lookup"><span data-stu-id="22101-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22101-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22101-117">Minimum supported client</span></span><br/> | <span data-ttu-id="22101-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22101-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="22101-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22101-119">Minimum supported server</span></span><br/> | <span data-ttu-id="22101-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="22101-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="22101-121">Header</span><span class="sxs-lookup"><span data-stu-id="22101-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="22101-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="22101-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="22101-123">DLL</span><span class="sxs-lookup"><span data-stu-id="22101-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22101-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22101-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="22101-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22101-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22101-126">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="22101-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="22101-127">**Ianalysisregion:: excluderectangle**</span><span class="sxs-lookup"><span data-stu-id="22101-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="22101-128">**Ianalysisregion:: excluderegion-Methode**</span><span class="sxs-lookup"><span data-stu-id="22101-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="22101-129">**Ianalysisregion:: intersectregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="22101-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="22101-130">**Ianalysisregion:: unionrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="22101-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="22101-131">**Ianalysisregion:: unionregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="22101-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="22101-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="22101-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




