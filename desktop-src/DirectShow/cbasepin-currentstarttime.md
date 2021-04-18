---
description: 'Die currentstarttime-Methode ruft die Segment Start Zeit ab, die von der cbasepin:: newsegment-Methode festgelegt wird.'
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: Cbasepin. currentstarttime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f413419992d66f8de3a28bb7e39368564ce0803
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358799"
---
# <a name="cbasepincurrentstarttime-method"></a><span data-ttu-id="3bb69-103">Cbasepin. currentstarttime-Methode</span><span class="sxs-lookup"><span data-stu-id="3bb69-103">CBasePin.CurrentStartTime method</span></span>

<span data-ttu-id="3bb69-104">Die- `CurrentStartTime` Methode ruft die Segment Start Zeit ab, die von der [**cbasepin:: newsegment**](cbasepin-newsegment.md) -Methode festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="3bb69-104">The `CurrentStartTime` method retrieves the segment start time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb69-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3bb69-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a><span data-ttu-id="3bb69-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3bb69-106">Parameters</span></span>

<span data-ttu-id="3bb69-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3bb69-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3bb69-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3bb69-108">Return value</span></span>

<span data-ttu-id="3bb69-109">Gibt den Wert von [**cbasepin:: m \_ tSTART**](cbasepin-m-tstart.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="3bb69-109">Returns the value of [**CBasePin::m\_tStart**](cbasepin-m-tstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb69-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3bb69-110">Requirements</span></span>



| <span data-ttu-id="3bb69-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3bb69-111">Requirement</span></span> | <span data-ttu-id="3bb69-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3bb69-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb69-113">Header</span><span class="sxs-lookup"><span data-stu-id="3bb69-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3bb69-114"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3bb69-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3bb69-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3bb69-115">Library</span></span><br/> | <dl> <span data-ttu-id="3bb69-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3bb69-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bb69-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3bb69-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb69-118">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3bb69-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




