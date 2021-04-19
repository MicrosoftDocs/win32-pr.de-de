---
description: Die Methode "Peer-ID" gibt einen Zeiger auf die Zuweisung der PIN zurück. Die-Methode erhöht nicht den Verweis Zähler für die-Schnittstelle.
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Ctransinplaceoutputpin. Peer-zuordcator-Methode (transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805de37e2df2bf5a198107eea69d9107e799598c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370612"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="f9a5b-104">Ctransinplaceoutputpin. Peer-zuordcator-Methode</span><span class="sxs-lookup"><span data-stu-id="f9a5b-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="f9a5b-105">Die `PeekAllocator` -Methode gibt einen Zeiger auf die Zuweisung der PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="f9a5b-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="f9a5b-106">Die-Methode erhöht nicht den Verweis Zähler für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f9a5b-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a5b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9a5b-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="f9a5b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9a5b-108">Parameters</span></span>

<span data-ttu-id="f9a5b-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f9a5b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f9a5b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9a5b-110">Return value</span></span>

<span data-ttu-id="f9a5b-111">Gibt die [**cbaseoutputpin:: m \_ pallocator**](cbaseoutputpin-m-pallocator.md) -Member-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="f9a5b-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a5b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9a5b-112">Requirements</span></span>



| <span data-ttu-id="f9a5b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9a5b-113">Requirement</span></span> | <span data-ttu-id="f9a5b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f9a5b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a5b-115">Header</span><span class="sxs-lookup"><span data-stu-id="f9a5b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="f9a5b-116"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5b-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f9a5b-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f9a5b-117">Library</span></span><br/> | <dl> <span data-ttu-id="f9a5b-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f9a5b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9a5b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9a5b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a5b-120">**Ctransinplaceoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f9a5b-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




