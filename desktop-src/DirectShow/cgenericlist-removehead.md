---
description: Die RemoveHead-Methode entfernt das erste Element in der Liste.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Cgenericlist. RemoveHead-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370191"
---
# <a name="cgenericlistremovehead-method"></a><span data-ttu-id="89646-103">Cgenericlist. RemoveHead-Methode</span><span class="sxs-lookup"><span data-stu-id="89646-103">CGenericList.RemoveHead method</span></span>

<span data-ttu-id="89646-104">Die- `RemoveHead` Methode entfernt das erste Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="89646-104">The `RemoveHead` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="89646-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="89646-105">Syntax</span></span>


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a><span data-ttu-id="89646-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="89646-106">Parameters</span></span>

<span data-ttu-id="89646-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="89646-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="89646-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89646-108">Return value</span></span>

<span data-ttu-id="89646-109">Gibt einen Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp) oder **null** zurück, wenn die Liste leer ist.</span><span class="sxs-lookup"><span data-stu-id="89646-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="89646-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="89646-110">Remarks</span></span>

<span data-ttu-id="89646-111">Diese Methode löscht den Listen Knoten, jedoch nicht das Element, das der Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="89646-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="89646-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89646-112">Requirements</span></span>



| <span data-ttu-id="89646-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89646-113">Requirement</span></span> | <span data-ttu-id="89646-114">Wert</span><span class="sxs-lookup"><span data-stu-id="89646-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89646-115">Header</span><span class="sxs-lookup"><span data-stu-id="89646-115">Header</span></span><br/>  | <dl> <span data-ttu-id="89646-116"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89646-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="89646-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="89646-117">Library</span></span><br/> | <dl> <span data-ttu-id="89646-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="89646-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89646-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89646-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89646-120">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="89646-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




