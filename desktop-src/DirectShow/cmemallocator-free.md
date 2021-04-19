---
description: Die Free-Methode wird während eines Decommit-Vorgangs aufgerufen.
ms.assetid: 71a84730-ca71-4418-bf76-52fd42fc7a5a
title: Cmemzuzucator. Free-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Free
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b707bb5b2a35466c47d05690a0f57f278d784542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362147"
---
# <a name="cmemallocatorfree-method"></a><span data-ttu-id="df5a8-103">Cmemzuzucator. Free-Methode</span><span class="sxs-lookup"><span data-stu-id="df5a8-103">CMemAllocator.Free method</span></span>

<span data-ttu-id="df5a8-104">Die- `Free` Methode wird während eines Decommit-Vorgangs aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="df5a8-104">The `Free` method is called during a decommit operation.</span></span> <span data-ttu-id="df5a8-105">Diese Methode implementiert die reine virtuelle [**cbasezuordcator:: Free**](cbaseallocator-free.md) -Methode, bewirkt aber nichts.</span><span class="sxs-lookup"><span data-stu-id="df5a8-105">This method implements the pure virtual [**CBaseAllocator::Free**](cbaseallocator-free.md) method, but does nothing.</span></span> <span data-ttu-id="df5a8-106">Der Puffer Arbeitsspeicher wird erst freigegeben, wenn das **cmemzuordcator** -Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="df5a8-106">The buffer memory is not actually released until the **CMemAllocator** object is destroyed.</span></span> <span data-ttu-id="df5a8-107">Die dekonstruktormethode ruft [**cmembelegcator:: reallyfree**](cmemallocator-reallyfree.md) auf, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="df5a8-107">The destructor method calls [**CMemAllocator::ReallyFree**](cmemallocator-reallyfree.md) to release the memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="df5a8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="df5a8-108">Syntax</span></span>


```C++
void Free();
```



## <a name="parameters"></a><span data-ttu-id="df5a8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="df5a8-109">Parameters</span></span>

<span data-ttu-id="df5a8-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="df5a8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="df5a8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df5a8-111">Return value</span></span>

<span data-ttu-id="df5a8-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="df5a8-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="df5a8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df5a8-113">Requirements</span></span>



| <span data-ttu-id="df5a8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df5a8-114">Requirement</span></span> | <span data-ttu-id="df5a8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="df5a8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df5a8-116">Header</span><span class="sxs-lookup"><span data-stu-id="df5a8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="df5a8-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df5a8-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="df5a8-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df5a8-118">Library</span></span><br/> | <dl> <span data-ttu-id="df5a8-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="df5a8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df5a8-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df5a8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df5a8-121">**Cmemzuordcator-Klasse**</span><span class="sxs-lookup"><span data-stu-id="df5a8-121">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




