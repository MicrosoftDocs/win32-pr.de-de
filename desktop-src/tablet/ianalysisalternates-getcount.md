---
description: Ruft die Anzahl der ianalysisalternate-Objekte ab, die in der ianalysisalteraten-Auflistung enthalten sind.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'Ianalysisalteraten:: GetCount-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6300ff994d7bd49461e9be39aa433586ecaabc75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360054"
---
# <a name="ianalysisalternatesgetcount-method"></a><span data-ttu-id="7f705-103">Ianalysisalterniert:: GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="7f705-103">IAnalysisAlternates::GetCount method</span></span>

<span data-ttu-id="7f705-104">Ruft die Anzahl der [**ianalysisalternate**](ianalysisalternate.md) -Objekte ab, die in der [**ianalysisalteraten**](ianalysisalternates.md) -Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7f705-104">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f705-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f705-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="7f705-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f705-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f705-107">*pulCount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7f705-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f705-108">Eine Ganzzahl ohne Vorzeichen 32 ohne Vorzeichen, die auf die Anzahl der [**ianalysisalternate**](ianalysisalternate.md) -Objekte festgelegt ist, die in der [**ianalysisalteraten**](ianalysisalternates.md) -Auflistung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7f705-108">An unsigned 32-bit integer that is set to the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f705-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f705-109">Return value</span></span>

<span data-ttu-id="7f705-110">Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7f705-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f705-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f705-111">Requirements</span></span>



| <span data-ttu-id="7f705-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f705-112">Requirement</span></span> | <span data-ttu-id="7f705-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7f705-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f705-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f705-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7f705-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f705-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7f705-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f705-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7f705-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7f705-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7f705-118">Header</span><span class="sxs-lookup"><span data-stu-id="7f705-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f705-119"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7f705-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7f705-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7f705-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f705-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f705-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7f705-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f705-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f705-123">**Ianalysisalteraten**</span><span class="sxs-lookup"><span data-stu-id="7f705-123">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="7f705-124">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="7f705-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




