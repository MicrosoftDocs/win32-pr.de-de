---
description: Die Methode "Peer-ID" gibt einen Zeiger auf die Zuweisung der PIN zurück. Die-Methode erhöht nicht den Verweis Zähler für die-Schnittstelle.
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Ctransinplaceinputpin. Peer-zuordcator-Methode (transip. h)
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
ms.openlocfilehash: 22358dd776a0536cfbae819ec7cace02dd1775a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366945"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="03145-104">Ctransinplaceinputpin. Peer-zuordcator-Methode</span><span class="sxs-lookup"><span data-stu-id="03145-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="03145-105">Die `PeekAllocator` -Methode gibt einen Zeiger auf die Zuweisung der PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="03145-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="03145-106">Die-Methode erhöht nicht den Verweis Zähler für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="03145-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="03145-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="03145-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="03145-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="03145-108">Parameters</span></span>

<span data-ttu-id="03145-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="03145-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03145-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03145-110">Return value</span></span>

<span data-ttu-id="03145-111">Gibt die [**cbaseingeputpin:: m \_ pallocator**](cbaseinputpin-m-pallocator.md) -Member-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="03145-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="03145-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03145-112">Requirements</span></span>



| <span data-ttu-id="03145-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03145-113">Requirement</span></span> | <span data-ttu-id="03145-114">Wert</span><span class="sxs-lookup"><span data-stu-id="03145-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03145-115">Header</span><span class="sxs-lookup"><span data-stu-id="03145-115">Header</span></span><br/>  | <dl> <span data-ttu-id="03145-116"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03145-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03145-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="03145-117">Library</span></span><br/> | <dl> <span data-ttu-id="03145-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="03145-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03145-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03145-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03145-120">**Ctransinplaceinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="03145-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




