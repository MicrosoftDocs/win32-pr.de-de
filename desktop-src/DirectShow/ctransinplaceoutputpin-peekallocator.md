---
description: 'CTransInPlaceOutputPin.PeekAllocator-Methode: Die PeekAllocator-Methode gibt einen Zeiger auf die Zuweisung des Pins zurück. Die -Methode erhöht den Verweiszähler für die Schnittstelle nicht.'
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: CTransInPlaceOutputPin.PeekAllocator-Methode (Transip.h)
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
ms.openlocfilehash: cba87df1c4b9a3391d60e9458387e7b2bd4afd49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084598"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a><span data-ttu-id="15297-104">CTransInPlaceOutputPin.PeekAllocator-Methode</span><span class="sxs-lookup"><span data-stu-id="15297-104">CTransInPlaceOutputPin.PeekAllocator method</span></span>

<span data-ttu-id="15297-105">Die `PeekAllocator` -Methode gibt einen Zeiger auf die Zuweisung des Pins zurück.</span><span class="sxs-lookup"><span data-stu-id="15297-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="15297-106">Die -Methode erhöht den Verweiszähler für die Schnittstelle nicht.</span><span class="sxs-lookup"><span data-stu-id="15297-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="15297-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="15297-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="15297-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="15297-108">Parameters</span></span>

<span data-ttu-id="15297-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="15297-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15297-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15297-110">Return value</span></span>

<span data-ttu-id="15297-111">Gibt die [**CBaseOutputPin::m \_ pAllocator-Membervariable**](cbaseoutputpin-m-pallocator.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="15297-111">Returns the [**CBaseOutputPin::m\_pAllocator**](cbaseoutputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="15297-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15297-112">Requirements</span></span>



| <span data-ttu-id="15297-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15297-113">Requirement</span></span> | <span data-ttu-id="15297-114">Wert</span><span class="sxs-lookup"><span data-stu-id="15297-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15297-115">Header</span><span class="sxs-lookup"><span data-stu-id="15297-115">Header</span></span><br/>  | <dl> <span data-ttu-id="15297-116"><dt>Transip.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="15297-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15297-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="15297-117">Library</span></span><br/> | <dl> <span data-ttu-id="15297-118"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="15297-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15297-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="15297-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15297-120">**CTransInPlaceOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="15297-120">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




