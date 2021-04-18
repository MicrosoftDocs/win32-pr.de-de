---
description: Ruft einen Wert ab, der angibt, ob ianalysisregion einen leeren Bereich darstellt.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'Ianalysisregion:: IsEmpty-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345740"
---
# <a name="ianalysisregionisempty-method"></a><span data-ttu-id="cdc7c-103">Ianalysisregion:: IsEmpty-Methode</span><span class="sxs-lookup"><span data-stu-id="cdc7c-103">IAnalysisRegion::IsEmpty method</span></span>

<span data-ttu-id="cdc7c-104">Ruft einen Wert ab, der angibt, ob [**ianalysisregion**](ianalysisregion.md) einen leeren Bereich darstellt.</span><span class="sxs-lookup"><span data-stu-id="cdc7c-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an empty region.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc7c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdc7c-105">Syntax</span></span>


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a><span data-ttu-id="cdc7c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdc7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdc7c-107">*pfimpmpty* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cdc7c-107">*pfIsEmpty* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdc7c-108">**Variant \_ TRUE** , wenn der dargestellte Bereich leer ist. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="cdc7c-108">**VARIANT\_TRUE** if the represented region is empty; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdc7c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdc7c-109">Return value</span></span>

<span data-ttu-id="cdc7c-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cdc7c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdc7c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdc7c-111">Requirements</span></span>



| <span data-ttu-id="cdc7c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdc7c-112">Requirement</span></span> | <span data-ttu-id="cdc7c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="cdc7c-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc7c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdc7c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cdc7c-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cdc7c-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cdc7c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdc7c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cdc7c-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cdc7c-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cdc7c-118">Header</span><span class="sxs-lookup"><span data-stu-id="cdc7c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdc7c-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cdc7c-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cdc7c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="cdc7c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdc7c-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdc7c-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cdc7c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdc7c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdc7c-123">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="cdc7c-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="cdc7c-124">**Ianalysisregion:: IsInfinite-Methode**</span><span class="sxs-lookup"><span data-stu-id="cdc7c-124">**IAnalysisRegion::IsInfinite Method**</span></span>](ianalysisregion-isinfinite.md)
</dt> <dt>

[<span data-ttu-id="cdc7c-125">**Ianalysisregion:: MakeEmpty-Methode**</span><span class="sxs-lookup"><span data-stu-id="cdc7c-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="cdc7c-126">**Ianalysisregion:: MakeInfinite-Methode**</span><span class="sxs-lookup"><span data-stu-id="cdc7c-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="cdc7c-127">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="cdc7c-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




