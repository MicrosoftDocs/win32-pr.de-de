---
description: Bestimmt, ob der angegebene ianalysisregion denselben Wert wie das aktuelle ianalysisregion-Objekt enthält.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'Ianalysisregion:: equalsregion-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129524"
---
# <a name="ianalysisregionequalsregion-method"></a><span data-ttu-id="1b34a-103">Ianalysisregion:: equalsregion-Methode</span><span class="sxs-lookup"><span data-stu-id="1b34a-103">IAnalysisRegion::EqualsRegion method</span></span>

<span data-ttu-id="1b34a-104">Bestimmt, ob der angegebene [**ianalysisregion**](ianalysisregion.md) denselben Wert wie das aktuelle **ianalysisregion** -Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="1b34a-104">Determines whether the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current **IAnalysisRegion** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b34a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b34a-105">Syntax</span></span>


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a><span data-ttu-id="1b34a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b34a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b34a-107">*potherregion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b34a-107">*pOtherRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b34a-108">Das [**ianalysisregion**](ianalysisregion.md) -Objekt, das mit dem aktuellen **ianalysisregion** verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b34a-108">The [**IAnalysisRegion**](ianalysisregion.md) object to compare with the current **IAnalysisRegion**.</span></span>

</dd> <dt>

<span data-ttu-id="1b34a-109">*pfregionsequal* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b34a-109">*pfRegionsEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b34a-110">**Variant \_ TRUE** , wenn der angegebene [**ianalysisregion**](ianalysisregion.md) denselben Wert wie der aktuelle ianalysisregion enthält. Andernfalls ist der Wert **\_ false**.</span><span class="sxs-lookup"><span data-stu-id="1b34a-110">**VARIANT\_TRUE** if the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current IAnalysisRegion; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b34a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b34a-111">Return value</span></span>

<span data-ttu-id="1b34a-112">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1b34a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b34a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b34a-113">Requirements</span></span>



| <span data-ttu-id="1b34a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b34a-114">Requirement</span></span> | <span data-ttu-id="1b34a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1b34a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b34a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b34a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1b34a-117">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b34a-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1b34a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b34a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1b34a-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1b34a-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1b34a-120">Header</span><span class="sxs-lookup"><span data-stu-id="1b34a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b34a-121"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1b34a-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1b34a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1b34a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b34a-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b34a-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1b34a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b34a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b34a-125">**Ianalysisregion**</span><span class="sxs-lookup"><span data-stu-id="1b34a-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> </dl>

 

 




