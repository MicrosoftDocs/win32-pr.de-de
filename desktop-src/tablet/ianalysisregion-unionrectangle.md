---
description: Erweitert den Bereich dieses ianalysisregion auf den Bereich, der durch die zugehörige Union mit dem angegebenen Rechteck erstellt wurde.
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'Ianalysisregion:: unionrechteck-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3a28a60eae95641225dd9c01791d89a9c38ada82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368101"
---
# <a name="ianalysisregionunionrectangle-method"></a><span data-ttu-id="cceb1-103">Ianalysisregion:: unionrechteck-Methode</span><span class="sxs-lookup"><span data-stu-id="cceb1-103">IAnalysisRegion::UnionRectangle method</span></span>

<span data-ttu-id="cceb1-104">Erweitert den Bereich dieses [**ianalysisregion**](ianalysisregion.md) auf den Bereich, der durch die zugehörige Union mit dem angegebenen Rechteck erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="cceb1-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="cceb1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cceb1-105">Syntax</span></span>


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="cceb1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cceb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cceb1-107">*prätangle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cceb1-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cceb1-108">Ein Zeiger auf das Rechteck, mit dem die Kombination in frei Hand Raumkoordinaten kombiniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cceb1-108">A pointer to the rectangle with which to combine, in ink-space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cceb1-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cceb1-109">Return value</span></span>

<span data-ttu-id="cceb1-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cceb1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cceb1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cceb1-111">Remarks</span></span>

<span data-ttu-id="cceb1-112">Die Rechteck Koordinaten befinden sich in HIMETRIC-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="cceb1-112">The rectangle coordinates are in HIMETRIC units.</span></span>

<span data-ttu-id="cceb1-113">Wenn einer der Bereiche unbegrenzt ist, ist der neue Bereich ebenfalls unendlich.</span><span class="sxs-lookup"><span data-stu-id="cceb1-113">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="cceb1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cceb1-114">Requirements</span></span>



| <span data-ttu-id="cceb1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cceb1-115">Requirement</span></span> | <span data-ttu-id="cceb1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cceb1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cceb1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cceb1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cceb1-118">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cceb1-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cceb1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cceb1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cceb1-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cceb1-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cceb1-121">Header</span><span class="sxs-lookup"><span data-stu-id="cceb1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cceb1-122"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cceb1-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cceb1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="cceb1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cceb1-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cceb1-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cceb1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cceb1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cceb1-126">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="cceb1-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="cceb1-127">**Ianalysisregion:: excluderectangle**</span><span class="sxs-lookup"><span data-stu-id="cceb1-127">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="cceb1-128">**Ianalysisregion:: excluderegion-Methode**</span><span class="sxs-lookup"><span data-stu-id="cceb1-128">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="cceb1-129">**Ianalysisregion:: intersectrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="cceb1-129">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="cceb1-130">**Ianalysisregion:: intersectregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="cceb1-130">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="cceb1-131">**Ianalysisregion:: unionregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="cceb1-131">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)
</dt> <dt>

[<span data-ttu-id="cceb1-132">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="cceb1-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




