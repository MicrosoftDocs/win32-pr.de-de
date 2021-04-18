---
description: Die isbeendete-Methode bestimmt, ob der Filter, der diese PIN enthält, angehalten wird.
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: Cbasepin. isbeendete-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365798"
---
# <a name="cbasepinisstopped-method"></a><span data-ttu-id="7ffaa-103">Cbasepin. isbeendet-Methode</span><span class="sxs-lookup"><span data-stu-id="7ffaa-103">CBasePin.IsStopped method</span></span>

<span data-ttu-id="7ffaa-104">Die- `IsStopped` Methode bestimmt, ob der Filter, der diese PIN enthält, angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-104">The `IsStopped` method determines whether the filter containing this pin is stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ffaa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ffaa-105">Syntax</span></span>


```C++
BOOL IsStopped();
```



## <a name="parameters"></a><span data-ttu-id="7ffaa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ffaa-106">Parameters</span></span>

<span data-ttu-id="7ffaa-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ffaa-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ffaa-108">Return value</span></span>

<span data-ttu-id="7ffaa-109">Gibt " **true** " zurück, wenn der Filter beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-109">Returns **TRUE** if the filter is stopped.</span></span> <span data-ttu-id="7ffaa-110">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ffaa-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ffaa-111">Remarks</span></span>

<span data-ttu-id="7ffaa-112">Nennen Sie diese Methode nicht innerhalb der **cbasepin** -Konstruktormethode, da der Filter möglicherweise noch nicht initialisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7ffaa-112">Do not call this method from within in the **CBasePin** constructor method, because the filter might not be initialized yet.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ffaa-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ffaa-113">Requirements</span></span>



| <span data-ttu-id="7ffaa-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ffaa-114">Requirement</span></span> | <span data-ttu-id="7ffaa-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7ffaa-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ffaa-116">Header</span><span class="sxs-lookup"><span data-stu-id="7ffaa-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7ffaa-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ffaa-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7ffaa-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7ffaa-118">Library</span></span><br/> | <dl> <span data-ttu-id="7ffaa-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7ffaa-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ffaa-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ffaa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ffaa-121">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7ffaa-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




