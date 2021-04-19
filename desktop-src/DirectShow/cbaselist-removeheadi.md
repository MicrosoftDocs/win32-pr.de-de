---
description: Die removeheadi-Methode entfernt das erste Element in der Liste.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Cbaselist. removeheadi-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d9b99dbac1d99587145aa2eba293ffa7ace959c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368641"
---
# <a name="cbaselistremoveheadi-method"></a><span data-ttu-id="9bb37-103">Cbaselist. removeheadi-Methode</span><span class="sxs-lookup"><span data-stu-id="9bb37-103">CBaseList.RemoveHeadI method</span></span>

<span data-ttu-id="9bb37-104">Die- `RemoveHeadI` Methode entfernt das erste Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="9bb37-104">The `RemoveHeadI` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bb37-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bb37-105">Syntax</span></span>


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a><span data-ttu-id="9bb37-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bb37-106">Parameters</span></span>

<span data-ttu-id="9bb37-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9bb37-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9bb37-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bb37-108">Return value</span></span>

<span data-ttu-id="9bb37-109">Gibt einen Zeiger auf das Element oder **null** zurück, wenn die Liste leer ist.</span><span class="sxs-lookup"><span data-stu-id="9bb37-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bb37-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9bb37-110">Remarks</span></span>

<span data-ttu-id="9bb37-111">Diese Methode löscht den Listen Knoten, jedoch nicht das Element, das der Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="9bb37-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bb37-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bb37-112">Requirements</span></span>



| <span data-ttu-id="9bb37-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bb37-113">Requirement</span></span> | <span data-ttu-id="9bb37-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9bb37-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bb37-115">Header</span><span class="sxs-lookup"><span data-stu-id="9bb37-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9bb37-116"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bb37-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9bb37-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9bb37-117">Library</span></span><br/> | <dl> <span data-ttu-id="9bb37-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9bb37-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bb37-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9bb37-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bb37-120">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9bb37-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




