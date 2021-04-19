---
description: Die Free-Methode gibt den gesamten Puffer Arbeitsspeicher frei. Diese Methode wird aufgerufen, wenn der besitzende Filter die Zuweisung aufhebt, nachdem das letzte Medien Beispiel freigegeben wurde.
ms.assetid: dd1e6c4d-762a-4caf-902b-015c6c9fdb4d
title: Cbasezucator. Free-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3534eac01a6769e090c8c808f16cc6ad5c6b84c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361925"
---
# <a name="cbaseallocatorfree-method"></a><span data-ttu-id="a0212-104">Cbasezucator. Free-Methode</span><span class="sxs-lookup"><span data-stu-id="a0212-104">CBaseAllocator.Free method</span></span>

<span data-ttu-id="a0212-105">Die- `Free` Methode gibt den gesamten Puffer Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="a0212-105">The `Free` method releases all of the buffer memory.</span></span> <span data-ttu-id="a0212-106">Diese Methode wird aufgerufen, wenn der besitzende Filter die Zuweisung aufhebt, nachdem das letzte Medien Beispiel freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a0212-106">This method is called when the owning filter decommits the allocator, after the last media sample is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0212-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0212-107">Syntax</span></span>


```C++
virtual void Free() = 0;
```



## <a name="parameters"></a><span data-ttu-id="a0212-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0212-108">Parameters</span></span>

<span data-ttu-id="a0212-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a0212-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0212-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a0212-110">Return value</span></span>

<span data-ttu-id="a0212-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a0212-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0212-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0212-112">Remarks</span></span>

<span data-ttu-id="a0212-113">Nachdem die [**Decommit**](cbaseallocator-decommit.md) -Methode aufgerufen wurde, ruft die Zuweisung diese Methode auf, wenn Sie das letzte Medien Beispiel freigibt.</span><span class="sxs-lookup"><span data-stu-id="a0212-113">After the [**Decommit**](cbaseallocator-decommit.md) method is called, the allocator calls this method when it releases the last media sample.</span></span> <span data-ttu-id="a0212-114">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0212-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0212-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a0212-115">Requirements</span></span>



| <span data-ttu-id="a0212-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a0212-116">Requirement</span></span> | <span data-ttu-id="a0212-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a0212-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0212-118">Header</span><span class="sxs-lookup"><span data-stu-id="a0212-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a0212-119"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0212-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a0212-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a0212-120">Library</span></span><br/> | <dl> <span data-ttu-id="a0212-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a0212-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0212-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0212-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0212-123">**Cbasezucator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a0212-123">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




