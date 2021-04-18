---
description: Ruft ein Array von Rechtecke ab, das den Bereich von ianalysisregion definiert.
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'Ianalysisregion:: GetRegionScans-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6cb8db60b5818f5bc2bc38892912e9ec40af1eb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347199"
---
# <a name="ianalysisregiongetregionscans-method"></a><span data-ttu-id="d003d-103">Ianalysisregion:: GetRegionScans-Methode</span><span class="sxs-lookup"><span data-stu-id="d003d-103">IAnalysisRegion::GetRegionScans method</span></span>

<span data-ttu-id="d003d-104">Ruft ein Array von Rechtecke ab, das den Bereich von [**ianalysisregion**](ianalysisregion.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="d003d-104">Retrieves an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d003d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d003d-105">Syntax</span></span>


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a><span data-ttu-id="d003d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d003d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d003d-107">*pulCount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d003d-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d003d-108">Die Anzahl der in *pregionscans* zurückgegebenen Rechtecke.</span><span class="sxs-lookup"><span data-stu-id="d003d-108">The number of rectangles returned in *pRegionScans*.</span></span>

</dd> <dt>

<span data-ttu-id="d003d-109">*pregionscans* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d003d-109">*pRegionScans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d003d-110">Ein Zeiger auf ein Array von Rechtecke, das den Bereich von [**ianalysisregion**](ianalysisregion.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="d003d-110">A pointer to an array of rectangles that defines the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d003d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d003d-111">Return value</span></span>

<span data-ttu-id="d003d-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d003d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d003d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d003d-113">Remarks</span></span>

<span data-ttu-id="d003d-114">Wenn *pregionscans* als **null**-Werte übergangen werden, gibt die **GetRegionScans** -Methode **S \_ OK** zurück, und die Anzahl der Rechtecke wird in *pulCount* zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d003d-114">If *pRegionScans* is passed as **NULL**, the **GetRegionScans** method returns **S\_OK** and the number of rectangles is returned in *pulCount*.</span></span>

> [!Caution]  
> <span data-ttu-id="d003d-115">Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *pregionscans* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="d003d-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pRegionScans* when you no longer need the information.</span></span>

 

<span data-ttu-id="d003d-116">Die Begrenzungen der Rechtecke befinden sich in frei Hand Raumkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="d003d-116">The bounds of the rectangles are in ink-space coordinates.</span></span>

<span data-ttu-id="d003d-117">Die Vereinigung der zurückgegebenen Rechtecke stellt den Bereich von [**ianalysisregion**](ianalysisregion.md)dar.</span><span class="sxs-lookup"><span data-stu-id="d003d-117">The union of the returned rectangles represents the area of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d003d-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d003d-118">Examples</span></span>

<span data-ttu-id="d003d-119">Im folgenden Beispiel wird gezeigt, wie Sie die Rechtecke, die den Bereich von [**ianalysisregion**](ianalysisregion.md)definieren, `region` und nur die Anzahl der Rechtecke erhalten.</span><span class="sxs-lookup"><span data-stu-id="d003d-119">The following example shows how to get the rectangles that define the area of the [**IAnalysisRegion**](ianalysisregion.md), `region` and how to get only the number of rectangles.</span></span>


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



## <a name="requirements"></a><span data-ttu-id="d003d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d003d-120">Requirements</span></span>



| <span data-ttu-id="d003d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d003d-121">Requirement</span></span> | <span data-ttu-id="d003d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d003d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d003d-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d003d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d003d-124">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d003d-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d003d-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d003d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d003d-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d003d-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d003d-127">Header</span><span class="sxs-lookup"><span data-stu-id="d003d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d003d-128"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d003d-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d003d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d003d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d003d-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d003d-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d003d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d003d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d003d-132">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="d003d-132">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="d003d-133">**Ianalysisregion:: GetBounds-Methode**</span><span class="sxs-lookup"><span data-stu-id="d003d-133">**IAnalysisRegion::GetBounds Method**</span></span>](ianalysisregion-getbounds.md)
</dt> <dt>

[<span data-ttu-id="d003d-134">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="d003d-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

