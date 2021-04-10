---
description: Ruft einen Wert ab, der angibt, ob ianalysisregion einen unendlichen Bereich darstellt.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'Ianalysisregion:: IsInfinite-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214681"
---
# <a name="ianalysisregionisinfinite-method"></a><span data-ttu-id="9555e-103">Ianalysisregion:: IsInfinite-Methode</span><span class="sxs-lookup"><span data-stu-id="9555e-103">IAnalysisRegion::IsInfinite method</span></span>

<span data-ttu-id="9555e-104">Ruft einen Wert ab, der angibt, ob [**ianalysisregion**](ianalysisregion.md) einen unendlichen Bereich darstellt.</span><span class="sxs-lookup"><span data-stu-id="9555e-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite region.</span></span>

## <a name="syntax"></a><span data-ttu-id="9555e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9555e-105">Syntax</span></span>


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a><span data-ttu-id="9555e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9555e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9555e-107">*pfisinfinite* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9555e-107">*pfIsInfinite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9555e-108">**Variant \_ TRUE** , wenn der dargestellte Bereich unendlich ist. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="9555e-108">**VARIANT\_TRUE** if the represented region is infinite; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9555e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9555e-109">Return value</span></span>

<span data-ttu-id="9555e-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="9555e-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9555e-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9555e-111">Requirements</span></span>



| <span data-ttu-id="9555e-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9555e-112">Requirement</span></span> | <span data-ttu-id="9555e-113">Wert</span><span class="sxs-lookup"><span data-stu-id="9555e-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9555e-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9555e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="9555e-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9555e-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9555e-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9555e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="9555e-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9555e-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9555e-118">Header</span><span class="sxs-lookup"><span data-stu-id="9555e-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="9555e-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9555e-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9555e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9555e-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9555e-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9555e-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9555e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9555e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9555e-123">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="9555e-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="9555e-124">**Ianalysisregion:: IsEmpty-Methode**</span><span class="sxs-lookup"><span data-stu-id="9555e-124">**IAnalysisRegion::IsEmpty Method**</span></span>](ianalysisregion-isempty.md)
</dt> <dt>

[<span data-ttu-id="9555e-125">**Ianalysisregion:: MakeEmpty-Methode**</span><span class="sxs-lookup"><span data-stu-id="9555e-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="9555e-126">**Ianalysisregion:: MakeInfinite-Methode**</span><span class="sxs-lookup"><span data-stu-id="9555e-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="9555e-127">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="9555e-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




