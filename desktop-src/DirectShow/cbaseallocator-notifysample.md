---
description: Die notifysample-Methode gibt alle Threads frei, die auf Beispiele warten.
ms.assetid: b09c48a0-9cd5-44a7-9267-d2a11e8cde4c
title: Cbasezucator. notifysample-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.NotifySample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: acaf5e45eac6a630d0589e3c8fad106ae29fa3dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356040"
---
# <a name="cbaseallocatornotifysample-method"></a><span data-ttu-id="41334-103">Cbasezucator. notifysample-Methode</span><span class="sxs-lookup"><span data-stu-id="41334-103">CBaseAllocator.NotifySample method</span></span>

<span data-ttu-id="41334-104">Die- `NotifySample` Methode gibt alle Threads frei, die auf Beispiele warten.</span><span class="sxs-lookup"><span data-stu-id="41334-104">The `NotifySample` method releases any threads that are waiting for samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="41334-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="41334-105">Syntax</span></span>


```C++
void NotifySample();
```



## <a name="parameters"></a><span data-ttu-id="41334-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="41334-106">Parameters</span></span>

<span data-ttu-id="41334-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="41334-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41334-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41334-108">Return value</span></span>

<span data-ttu-id="41334-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="41334-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41334-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41334-110">Remarks</span></span>

<span data-ttu-id="41334-111">Wenn Threads auf Beispiele warten, ist der Wert von [**cbasezucator:: m \_ lwaiting**](cbaseallocator-m-lwaiting.md) größer als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="41334-111">When there are threads waiting for samples, the value of [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) is greater than zero.</span></span> <span data-ttu-id="41334-112">Wenn *m \_ lwaiting* größer als 0 (null) ist, ruft diese Methode die **ReleaseSemaphore** -Funktion auf dem [**cbasezucator:: m \_ hsem**](cbaseallocator-m-hsem.md) -Semaphore auf und aktiviert alle wartenden Threads.</span><span class="sxs-lookup"><span data-stu-id="41334-112">If *m\_lWaiting* is greater than zero, this method calls the **ReleaseSemaphore** function on the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore, activating any waiting threads.</span></span> <span data-ttu-id="41334-113">Außerdem wird *m \_ lwaiting* auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="41334-113">It also resets *m\_lWaiting* to zero.</span></span>

<span data-ttu-id="41334-114">Diese Methode wird innerhalb der [**cbasezucator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) -Methode aufgerufen, wenn eine Stichprobe an die freie Liste zurückgegeben wird. und aus der [**cbasebelegcator::D ecommit**](cbaseallocator-decommit.md) -Methode, wenn für die Zuweisung ein Commit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41334-114">This method is called from within the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method, when a sample is returned to the free list; and from the [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) method, when the allocator is decommitted.</span></span>

## <a name="requirements"></a><span data-ttu-id="41334-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41334-115">Requirements</span></span>



| <span data-ttu-id="41334-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41334-116">Requirement</span></span> | <span data-ttu-id="41334-117">Wert</span><span class="sxs-lookup"><span data-stu-id="41334-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41334-118">Header</span><span class="sxs-lookup"><span data-stu-id="41334-118">Header</span></span><br/>  | <dl> <span data-ttu-id="41334-119"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41334-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="41334-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="41334-120">Library</span></span><br/> | <dl> <span data-ttu-id="41334-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="41334-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41334-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41334-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41334-123">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="41334-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




