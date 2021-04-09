---
description: Gibt die Strich Bezeichner zurück, die diesem ianalysisalternate-Element zugeordnet sind.
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'Ianalysisalternate:: GetStrokeIds-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862731"
---
# <a name="ianalysisalternategetstrokeids-method"></a><span data-ttu-id="85756-103">Ianalysisalternate:: GetStrokeIds-Methode</span><span class="sxs-lookup"><span data-stu-id="85756-103">IAnalysisAlternate::GetStrokeIds method</span></span>

<span data-ttu-id="85756-104">Gibt die Strich Bezeichner zurück, die diesem [**ianalysisalternate**](ianalysisalternate.md)-Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="85756-104">Returns the stroke identifiers that are associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="85756-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="85756-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="85756-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="85756-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85756-107">*pulstrokeidscount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="85756-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85756-108">Ein Zeiger auf einen **ulong** -Wert, der auf die Anzahl von Strich Bezeichners festgelegt ist, die diesem [**ianalysisalternate**](ianalysisalternate.md)-Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="85756-108">A pointer to a **ULONG** that is set to the number of stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> <dt>

<span data-ttu-id="85756-109">*pplstrokeids* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85756-109">*pplStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85756-110">\[Out, size \_ ist ( \* *pulstrokeidscount* \* sizeof (Long))\]</span><span class="sxs-lookup"><span data-stu-id="85756-110">\[out, size\_is(\**pulStrokeIdsCount* \* sizeof(LONG))\]</span></span>

<span data-ttu-id="85756-111">Ein Array von **Long** der Länge *pulstrokeidscount* , das auf die Strich Bezeichner festgelegt wird, die mit diesem [**ianalysisalternate**](ianalysisalternate.md)verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="85756-111">An array of **LONG** of length *pulStrokeIdsCount* that is set to the stroke identifiers associated with this [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85756-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85756-112">Return value</span></span>

<span data-ttu-id="85756-113">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="85756-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="85756-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85756-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="85756-115">Um einen Speicherplatz zu vermeiden, verwenden Sie " [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher aus \* *pplstrokeids* freizugeben, wenn Sie die Informationen nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="85756-115">To avoid a memory leak, use [CoTaskMemFree](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokeIds* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="85756-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85756-116">Requirements</span></span>



| <span data-ttu-id="85756-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85756-117">Requirement</span></span> | <span data-ttu-id="85756-118">Wert</span><span class="sxs-lookup"><span data-stu-id="85756-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85756-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85756-119">Minimum supported client</span></span><br/> | <span data-ttu-id="85756-120">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85756-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="85756-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85756-121">Minimum supported server</span></span><br/> | <span data-ttu-id="85756-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="85756-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="85756-123">Header</span><span class="sxs-lookup"><span data-stu-id="85756-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="85756-124"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="85756-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="85756-125">DLL</span><span class="sxs-lookup"><span data-stu-id="85756-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85756-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85756-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="85756-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85756-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85756-128">**Ianalysisalternate**</span><span class="sxs-lookup"><span data-stu-id="85756-128">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="85756-129">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="85756-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

