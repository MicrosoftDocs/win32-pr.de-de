---
description: Ruft das umgebende Rechteck des ianalysisregion-Elements ab.
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'Ianalysisregion:: GetBounds-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751873"
---
# <a name="ianalysisregiongetbounds-method"></a><span data-ttu-id="4d1e4-103">Ianalysisregion:: GetBounds-Methode</span><span class="sxs-lookup"><span data-stu-id="4d1e4-103">IAnalysisRegion::GetBounds method</span></span>

<span data-ttu-id="4d1e4-104">Ruft das umgebende Rechteck des [**ianalysisregion**](ianalysisregion.md)-Elements ab.</span><span class="sxs-lookup"><span data-stu-id="4d1e4-104">Gets the bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d1e4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d1e4-105">Syntax</span></span>


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a><span data-ttu-id="4d1e4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d1e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d1e4-107">*pboundingrechteck* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4d1e4-107">*pBoundingRectangle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d1e4-108">Das umgebende Rechteck von [**ianalysisregion**](ianalysisregion.md) in frei Hand Raumkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="4d1e4-108">The bounding rectangle of the [**IAnalysisRegion**](ianalysisregion.md) in ink space coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d1e4-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d1e4-109">Return value</span></span>

<span data-ttu-id="4d1e4-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="4d1e4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d1e4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d1e4-111">Remarks</span></span>

<span data-ttu-id="4d1e4-112">Die Begrenzungen befinden sich in frei Hand Raumkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="4d1e4-112">The bounds are in ink-space coordinates.</span></span>

<span data-ttu-id="4d1e4-113">Wenn [**ianalysisregion**](ianalysisregion.md) einen unendlichen Bereich darstellt, sind die linken und oberen Begrenzungen **int \_ Min**, und die Rechte und unteren Begrenzungen sind **int \_ Max**.</span><span class="sxs-lookup"><span data-stu-id="4d1e4-113">If the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite area, the left and top bounds are **INT\_MIN**; and the right and bottom bounds are **INT\_MAX**.</span></span>

<span data-ttu-id="4d1e4-114">Wenn [**ianalysisregion**](ianalysisregion.md) einen leeren Bereich darstellt, sind alle Begrenzungen des Rechtecks 0.</span><span class="sxs-lookup"><span data-stu-id="4d1e4-114">If the [**IAnalysisRegion**](ianalysisregion.md) represents an empty area, all the bounds of the rectangle are 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d1e4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4d1e4-115">Requirements</span></span>



| <span data-ttu-id="4d1e4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4d1e4-116">Requirement</span></span> | <span data-ttu-id="4d1e4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4d1e4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1e4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4d1e4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4d1e4-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4d1e4-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4d1e4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4d1e4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4d1e4-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4d1e4-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4d1e4-122">Header</span><span class="sxs-lookup"><span data-stu-id="4d1e4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d1e4-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4d1e4-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4d1e4-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4d1e4-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d1e4-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d1e4-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4d1e4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d1e4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d1e4-127">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="4d1e4-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="4d1e4-128">**Ianalysisregion:: GetRegionScans-Methode**</span><span class="sxs-lookup"><span data-stu-id="4d1e4-128">**IAnalysisRegion::GetRegionScans Method**</span></span>](ianalysisregion-getregionscans.md)
</dt> <dt>

[<span data-ttu-id="4d1e4-129">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="4d1e4-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




