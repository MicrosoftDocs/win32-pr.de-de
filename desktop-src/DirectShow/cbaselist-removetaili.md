---
description: Die removetaili-Methode entfernt das letzte Element in der Liste.
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: Cbaselist. removetaili-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17c4e151426b54667ea3b9e4cb88be9526e2054b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371444"
---
# <a name="cbaselistremovetaili-method"></a><span data-ttu-id="7f919-103">Cbaselist. removetaili-Methode</span><span class="sxs-lookup"><span data-stu-id="7f919-103">CBaseList.RemoveTailI method</span></span>

<span data-ttu-id="7f919-104">Die- `RemoveTailI` Methode entfernt das letzte Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="7f919-104">The `RemoveTailI` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f919-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f919-105">Syntax</span></span>


```C++
void* RemoveTailI();
```



## <a name="parameters"></a><span data-ttu-id="7f919-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f919-106">Parameters</span></span>

<span data-ttu-id="7f919-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7f919-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f919-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f919-108">Return value</span></span>

<span data-ttu-id="7f919-109">Gibt einen Zeiger auf das Element oder **null** zurück, wenn die Liste leer ist.</span><span class="sxs-lookup"><span data-stu-id="7f919-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f919-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f919-110">Remarks</span></span>

<span data-ttu-id="7f919-111">Diese Methode löscht den Listen Knoten, jedoch nicht das Element, das im Knoten enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7f919-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f919-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f919-112">Requirements</span></span>



| <span data-ttu-id="7f919-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f919-113">Requirement</span></span> | <span data-ttu-id="7f919-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7f919-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f919-115">Header</span><span class="sxs-lookup"><span data-stu-id="7f919-115">Header</span></span><br/>  | <dl> <span data-ttu-id="7f919-116"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f919-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7f919-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7f919-117">Library</span></span><br/> | <dl> <span data-ttu-id="7f919-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7f919-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f919-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f919-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f919-120">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7f919-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




