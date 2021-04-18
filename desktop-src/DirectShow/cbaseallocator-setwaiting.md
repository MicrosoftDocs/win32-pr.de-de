---
description: Die setwaiting-Methode erhöht die Anzahl der wartenden Threads.
ms.assetid: 4aec6177-fb32-44be-a58e-41a4f4aaf4f2
title: Cbasezucator. setwaiting-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetWaiting
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92cba22e128a76f7884050d74a7819142c696dc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372228"
---
# <a name="cbaseallocatorsetwaiting-method"></a><span data-ttu-id="0c152-103">Cbasezucator. setwaiting-Methode</span><span class="sxs-lookup"><span data-stu-id="0c152-103">CBaseAllocator.SetWaiting method</span></span>

<span data-ttu-id="0c152-104">Die- `SetWaiting` Methode erhöht die Anzahl der wartenden Threads.</span><span class="sxs-lookup"><span data-stu-id="0c152-104">The `SetWaiting` method increments the count of waiting threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c152-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c152-105">Syntax</span></span>


```C++
void SetWaiting();
```



## <a name="parameters"></a><span data-ttu-id="0c152-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c152-106">Parameters</span></span>

<span data-ttu-id="0c152-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0c152-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c152-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c152-108">Return value</span></span>

<span data-ttu-id="0c152-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0c152-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c152-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c152-110">Remarks</span></span>

<span data-ttu-id="0c152-111">Diese Methode erhöht die Member-Variable [**cbasezucator:: m \_ lwaiting**](cbaseallocator-m-lwaiting.md) .</span><span class="sxs-lookup"><span data-stu-id="0c152-111">This method increments the [**CBaseAllocator::m\_lWaiting**](cbaseallocator-m-lwaiting.md) member variable.</span></span> <span data-ttu-id="0c152-112">Wenn ein Thread in der [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode blockiert ist, ruft die Zuweisung auf `SetWaiting` und wartet dann darauf, dass das [**cbasezucator:: m \_ hsem**](cbaseallocator-m-hsem.md) -Semaphor signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0c152-112">If a thread is blocked in the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method, the allocator calls `SetWaiting` and then waits for the [**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md) semaphore to be signaled.</span></span> <span data-ttu-id="0c152-113">Die [**cbasezucator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) -Methode signalisiert dem Semaphor und legt *m \_ lwaiting* auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="0c152-113">The [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method signals the semaphore and sets *m\_lWaiting* back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c152-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c152-114">Requirements</span></span>



| <span data-ttu-id="0c152-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c152-115">Requirement</span></span> | <span data-ttu-id="0c152-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0c152-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c152-117">Header</span><span class="sxs-lookup"><span data-stu-id="0c152-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0c152-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c152-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0c152-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c152-119">Library</span></span><br/> | <dl> <span data-ttu-id="0c152-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0c152-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c152-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c152-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c152-122">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0c152-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




