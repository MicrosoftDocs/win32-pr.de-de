---
description: 'CTransInPlaceInputPin.PeekAllocator-Methode: Die PeekAllocator-Methode gibt einen Zeiger auf die Zuweisung des Pins zurück. Die -Methode erhöht den Verweiszähler für die Schnittstelle nicht.'
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: CTransInPlaceInputPin.PeekAllocator-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7a5f7cb0fbe754890b1d7930bb54c6fca47afa5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084668"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="b2988-104">CTransInPlaceInputPin.PeekAllocator-Methode</span><span class="sxs-lookup"><span data-stu-id="b2988-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="b2988-105">Die `PeekAllocator` -Methode gibt einen Zeiger auf die Zuweisung des Pins zurück.</span><span class="sxs-lookup"><span data-stu-id="b2988-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="b2988-106">Die -Methode erhöht den Verweiszähler für die Schnittstelle nicht.</span><span class="sxs-lookup"><span data-stu-id="b2988-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2988-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2988-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="b2988-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b2988-108">Parameters</span></span>

<span data-ttu-id="b2988-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b2988-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b2988-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b2988-110">Return value</span></span>

<span data-ttu-id="b2988-111">Gibt die [**CBaseInputPin::m \_ pAllocator-Membervariable**](cbaseinputpin-m-pallocator.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="b2988-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2988-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2988-112">Requirements</span></span>



| <span data-ttu-id="b2988-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2988-113">Requirement</span></span> | <span data-ttu-id="b2988-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b2988-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2988-115">Header</span><span class="sxs-lookup"><span data-stu-id="b2988-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b2988-116"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2988-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2988-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b2988-117">Library</span></span><br/> | <dl> <span data-ttu-id="b2988-118"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b2988-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2988-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b2988-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2988-120">**CTransInPlaceInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b2988-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




