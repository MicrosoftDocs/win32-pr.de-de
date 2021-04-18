---
description: Die removetail-Methode entfernt das letzte Element in der Liste.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Cgenericlist. removetail-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371406"
---
# <a name="cgenericlistremovetail-method"></a><span data-ttu-id="39a64-103">Cgenericlist. removetail-Methode</span><span class="sxs-lookup"><span data-stu-id="39a64-103">CGenericList.RemoveTail method</span></span>

<span data-ttu-id="39a64-104">Die- `RemoveTail` Methode entfernt das letzte Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="39a64-104">The `RemoveTail` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a64-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="39a64-105">Syntax</span></span>


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a><span data-ttu-id="39a64-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39a64-106">Parameters</span></span>

<span data-ttu-id="39a64-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="39a64-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39a64-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39a64-108">Return value</span></span>

<span data-ttu-id="39a64-109">Gibt einen Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp) oder **null** zurück, wenn die Liste leer ist.</span><span class="sxs-lookup"><span data-stu-id="39a64-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="39a64-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39a64-110">Remarks</span></span>

<span data-ttu-id="39a64-111">Diese Methode löscht den Listen Knoten, jedoch nicht das Element, das im Knoten enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="39a64-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="39a64-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39a64-112">Requirements</span></span>



| <span data-ttu-id="39a64-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39a64-113">Requirement</span></span> | <span data-ttu-id="39a64-114">Wert</span><span class="sxs-lookup"><span data-stu-id="39a64-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a64-115">Header</span><span class="sxs-lookup"><span data-stu-id="39a64-115">Header</span></span><br/>  | <dl> <span data-ttu-id="39a64-116"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39a64-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="39a64-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="39a64-117">Library</span></span><br/> | <dl> <span data-ttu-id="39a64-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="39a64-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39a64-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39a64-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a64-120">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="39a64-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




