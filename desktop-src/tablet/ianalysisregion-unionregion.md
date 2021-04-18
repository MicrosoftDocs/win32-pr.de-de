---
description: Erweitert den Bereich dieses ianalysisregion auf den Bereich, der von seiner Union mit dem angegebenen ianalysisregion erstellt wurde.
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'Ianalysisregion:: unionregion-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 587986973c4ae4bebaeed3c031c746bc4f842c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368100"
---
# <a name="ianalysisregionunionregion-method"></a><span data-ttu-id="d6ebc-103">Ianalysisregion:: unionregion-Methode</span><span class="sxs-lookup"><span data-stu-id="d6ebc-103">IAnalysisRegion::UnionRegion method</span></span>

<span data-ttu-id="d6ebc-104">Erweitert den Bereich dieses [**ianalysisregion**](ianalysisregion.md) auf den Bereich, der von seiner Union mit dem angegebenen **ianalysisregion** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-104">Expands the area of this [**IAnalysisRegion**](ianalysisregion.md) to the area created by its union with the specified **IAnalysisRegion**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6ebc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6ebc-105">Syntax</span></span>


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a><span data-ttu-id="d6ebc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6ebc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6ebc-107">*pregionin Union* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d6ebc-107">*pRegionToUnion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6ebc-108">Der [**ianalysisregion**](ianalysisregion.md) , mit dem kombiniert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-108">The [**IAnalysisRegion**](ianalysisregion.md) with which to combine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6ebc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6ebc-109">Return value</span></span>

<span data-ttu-id="d6ebc-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d6ebc-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d6ebc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6ebc-111">Remarks</span></span>

<span data-ttu-id="d6ebc-112">Wenn einer der Bereiche unbegrenzt ist, ist der neue Bereich ebenfalls unendlich.</span><span class="sxs-lookup"><span data-stu-id="d6ebc-112">If either area is infinite, the new area is also infinite.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6ebc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6ebc-113">Requirements</span></span>



| <span data-ttu-id="d6ebc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6ebc-114">Requirement</span></span> | <span data-ttu-id="d6ebc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d6ebc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6ebc-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d6ebc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d6ebc-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d6ebc-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d6ebc-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d6ebc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d6ebc-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d6ebc-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d6ebc-120">Header</span><span class="sxs-lookup"><span data-stu-id="d6ebc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6ebc-121"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d6ebc-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d6ebc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d6ebc-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6ebc-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6ebc-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d6ebc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6ebc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6ebc-125">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="d6ebc-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="d6ebc-126">**Ianalysisregion:: excluderectangle**</span><span class="sxs-lookup"><span data-stu-id="d6ebc-126">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
</dt> <dt>

[<span data-ttu-id="d6ebc-127">**Ianalysisregion:: excluderegion-Methode**</span><span class="sxs-lookup"><span data-stu-id="d6ebc-127">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
</dt> <dt>

[<span data-ttu-id="d6ebc-128">**Ianalysisregion:: intersectrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="d6ebc-128">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[<span data-ttu-id="d6ebc-129">**Ianalysisregion:: intersectregion-Methode**</span><span class="sxs-lookup"><span data-stu-id="d6ebc-129">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
</dt> <dt>

[<span data-ttu-id="d6ebc-130">**Ianalysisregion:: unionrechteck-Methode**</span><span class="sxs-lookup"><span data-stu-id="d6ebc-130">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
</dt> <dt>

[<span data-ttu-id="d6ebc-131">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="d6ebc-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




