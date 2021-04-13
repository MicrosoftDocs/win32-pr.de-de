---
description: Bestimmt, ob sich der Bereich des ianalysisregion mit dem angegebenen Rechteck überschneidet.
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'Ianalysisregion:: interseczwith-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 99ff1ce8d3039b04d83f9cdd5c1d6aebe00be407
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526552"
---
# <a name="ianalysisregionintersectswith-method"></a><span data-ttu-id="f81ea-103">Ianalysisregion:: interseczwith-Methode</span><span class="sxs-lookup"><span data-stu-id="f81ea-103">IAnalysisRegion::IntersectsWith method</span></span>

<span data-ttu-id="f81ea-104">Bestimmt, ob sich der Bereich des [**ianalysisregion**](ianalysisregion.md) mit dem angegebenen Rechteck überschneidet.</span><span class="sxs-lookup"><span data-stu-id="f81ea-104">Determines whether the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="f81ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f81ea-105">Syntax</span></span>


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a><span data-ttu-id="f81ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f81ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f81ea-107">*prätangle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f81ea-107">*pRectangle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f81ea-108">Ein Zeiger auf das Rechteck, mit dem in den Freihand Raumkoordinaten verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f81ea-108">A pointer to the rectangle with which to compare, in ink-space coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f81ea-109">*pfisintersecting* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f81ea-109">*pfIsIntersecting* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f81ea-110">**Variant \_ TRUE** , wenn sich der Bereich von [**ianalysisregion**](ianalysisregion.md) mit dem angegebenen Rechteck überschneidet. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="f81ea-110">**VARIANT\_TRUE** if the area of the [**IAnalysisRegion**](ianalysisregion.md) intersects with the specified rectangle; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f81ea-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f81ea-111">Return value</span></span>

<span data-ttu-id="f81ea-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f81ea-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f81ea-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f81ea-113">Remarks</span></span>

<span data-ttu-id="f81ea-114">Der Vergleich erfolgt in freistellungenkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="f81ea-114">The comparison is in ink-space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="f81ea-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f81ea-115">Requirements</span></span>



| <span data-ttu-id="f81ea-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f81ea-116">Requirement</span></span> | <span data-ttu-id="f81ea-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f81ea-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f81ea-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f81ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f81ea-119">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f81ea-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f81ea-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f81ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f81ea-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f81ea-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f81ea-122">Header</span><span class="sxs-lookup"><span data-stu-id="f81ea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f81ea-123"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f81ea-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f81ea-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f81ea-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f81ea-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f81ea-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f81ea-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f81ea-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f81ea-127">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="f81ea-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="f81ea-128">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="f81ea-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




