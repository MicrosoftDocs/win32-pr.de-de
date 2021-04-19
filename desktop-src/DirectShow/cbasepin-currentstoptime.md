---
description: 'Die currentstoptime-Methode ruft die Endzeit des Segments ab, die von der cbasepin:: newsegment-Methode festgelegt wird.'
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Cbasepin. currentstoptime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74fb25184bbcd0778268f74a4c40ccfb0722287f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370698"
---
# <a name="cbasepincurrentstoptime-method"></a><span data-ttu-id="ae77c-103">Cbasepin. currentstoptime-Methode</span><span class="sxs-lookup"><span data-stu-id="ae77c-103">CBasePin.CurrentStopTime method</span></span>

<span data-ttu-id="ae77c-104">Die- `CurrentStopTime` Methode ruft die Endzeit des Segments ab, die von der [**cbasepin:: newsegment**](cbasepin-newsegment.md) -Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ae77c-104">The `CurrentStopTime` method retrieves the segment stop time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae77c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae77c-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a><span data-ttu-id="ae77c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae77c-106">Parameters</span></span>

<span data-ttu-id="ae77c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ae77c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae77c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae77c-108">Return value</span></span>

<span data-ttu-id="ae77c-109">Gibt den Wert von [**cbasepin:: m \_ thalte**](cbasepin-m-tstop.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="ae77c-109">Returns the value of [**CBasePin::m\_tStop**](cbasepin-m-tstop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae77c-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae77c-110">Requirements</span></span>



| <span data-ttu-id="ae77c-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae77c-111">Requirement</span></span> | <span data-ttu-id="ae77c-112">Wert</span><span class="sxs-lookup"><span data-stu-id="ae77c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae77c-113">Header</span><span class="sxs-lookup"><span data-stu-id="ae77c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="ae77c-114"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae77c-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ae77c-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ae77c-115">Library</span></span><br/> | <dl> <span data-ttu-id="ae77c-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ae77c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae77c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae77c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae77c-118">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ae77c-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




