---
description: Die addaf Teri-Methode fügt ein Element nach der angegebenen Position ein.
ms.assetid: 6da6c1ed-5f22-4364-b636-64b5a0ce1560
title: Cbaselist. addafteri-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfterI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 760c0bea3a213d7126ea795e9575b3897117f7a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370118"
---
# <a name="cbaselistaddafteri-method"></a><span data-ttu-id="656dd-103">Cbaselist. addafteri-Methode</span><span class="sxs-lookup"><span data-stu-id="656dd-103">CBaseList.AddAfterI method</span></span>

<span data-ttu-id="656dd-104">Die- `AddAfterI` Methode fügt ein Element nach der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="656dd-104">The `AddAfterI` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="656dd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="656dd-105">Syntax</span></span>


```C++
POSITION AddAfterI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="656dd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="656dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656dd-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="656dd-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="656dd-108">Die Position, an der das Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="656dd-108">Position after which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="656dd-109">*pobj*</span><span class="sxs-lookup"><span data-stu-id="656dd-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="656dd-110">Zeiger auf das hinzu zufügende Element.</span><span class="sxs-lookup"><span data-stu-id="656dd-110">Pointer to the item to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656dd-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="656dd-111">Return value</span></span>

<span data-ttu-id="656dd-112">Gibt den Positionsindikator des eingefügten Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="656dd-112">Returns the position indicator of the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="656dd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="656dd-113">Remarks</span></span>

<span data-ttu-id="656dd-114">Wenn *POS* **null** ist, fügt diese Methode das Element am Anfang der Liste hinzu (entspricht dem Aufruf der [**cbaselist:: addheadi**](cbaselist-addheadi.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="656dd-114">If *pos* is **NULL**, this method adds the item to the head of the list (equivalent to calling the [**CBaseList::AddHeadI**](cbaselist-addheadi.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="656dd-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="656dd-115">Requirements</span></span>



| <span data-ttu-id="656dd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="656dd-116">Requirement</span></span> | <span data-ttu-id="656dd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="656dd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="656dd-118">Header</span><span class="sxs-lookup"><span data-stu-id="656dd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="656dd-119"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="656dd-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="656dd-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="656dd-120">Library</span></span><br/> | <dl> <span data-ttu-id="656dd-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="656dd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="656dd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="656dd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656dd-123">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="656dd-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




