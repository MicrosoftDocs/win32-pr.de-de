---
description: Die Decommit-Methode hebt die Zuordnung der Zuweisung auf. Diese Methode implementiert die imemzuzucator::D ecommit-Methode.
ms.assetid: 0c8d44e0-17ea-4f7f-be44-f9ae2e34fbef
title: Cbasezucator. Decommit-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Decommit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 613af805f1c04a7bf375755ff8f3adba7b70be18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364976"
---
# <a name="cbaseallocatordecommit-method"></a><span data-ttu-id="936cf-104">Cbasezucator. Decommit-Methode</span><span class="sxs-lookup"><span data-stu-id="936cf-104">CBaseAllocator.Decommit method</span></span>

<span data-ttu-id="936cf-105">Die-Methode führt einen Commit für `Decommit` die Zuweisung aus.</span><span class="sxs-lookup"><span data-stu-id="936cf-105">The `Decommit` method decommits the allocator.</span></span> <span data-ttu-id="936cf-106">Diese Methode implementiert die [**imemzuzucator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) -Methode.</span><span class="sxs-lookup"><span data-stu-id="936cf-106">This method implements the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="936cf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="936cf-107">Syntax</span></span>


```C++
HRESULT Decommit();
```



## <a name="parameters"></a><span data-ttu-id="936cf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="936cf-108">Parameters</span></span>

<span data-ttu-id="936cf-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="936cf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="936cf-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="936cf-110">Return value</span></span>

<span data-ttu-id="936cf-111">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="936cf-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="936cf-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="936cf-112">Remarks</span></span>

<span data-ttu-id="936cf-113">Nachdem diese Methode aufgerufen wurde, können Aufrufe der [**cbasezucator:: GetBuffer**](cbaseallocator-getbuffer.md) -Methode nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="936cf-113">After this method is called, calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method will fail.</span></span> <span data-ttu-id="936cf-114">Wenn Beispiele veröffentlicht werden, werden Sie an die kostenlose Liste zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="936cf-114">As samples are released, they get returned to the free list.</span></span> <span data-ttu-id="936cf-115">Wenn das letzte Beispiel zurückgegeben wird, ruft die Zuweisung die [**cbasezucator:: Free**](cbaseallocator-free.md) -Methode auf, die den belegten Arbeitsspeicher freigibt.</span><span class="sxs-lookup"><span data-stu-id="936cf-115">When the last sample is returned, the allocator calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method, which releases the allocated memory.</span></span> <span data-ttu-id="936cf-116">(In der Basisklasse ist **Free** eine rein virtuelle Methode.)</span><span class="sxs-lookup"><span data-stu-id="936cf-116">(In the base class, **Free** is a pure virtual method.)</span></span>

<span data-ttu-id="936cf-117">Außerdem werden von dieser Methode alle Threads freigegeben, die bei **GetBuffer** -Aufrufen blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="936cf-117">In addition, this method releases any threads that are blocked on **GetBuffer** calls.</span></span> <span data-ttu-id="936cf-118">Der Aufruf von **GetBuffer** schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="936cf-118">The calls to **GetBuffer** fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="936cf-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="936cf-119">Requirements</span></span>



| <span data-ttu-id="936cf-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="936cf-120">Requirement</span></span> | <span data-ttu-id="936cf-121">Wert</span><span class="sxs-lookup"><span data-stu-id="936cf-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="936cf-122">Header</span><span class="sxs-lookup"><span data-stu-id="936cf-122">Header</span></span><br/>  | <dl> <span data-ttu-id="936cf-123"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="936cf-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="936cf-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="936cf-124">Library</span></span><br/> | <dl> <span data-ttu-id="936cf-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="936cf-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="936cf-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="936cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936cf-127">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="936cf-127">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




