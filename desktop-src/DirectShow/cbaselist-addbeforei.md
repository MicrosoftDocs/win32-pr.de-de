---
description: Die addbeforei-Methode fügt ein Element vor der angegebenen Position ein.
ms.assetid: d310e303-889a-43a6-bda5-2e7b805b25d1
title: Cbaselist. addbeforei-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddBeforeI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6996d2fd3ed0cad07a442530e3ae77470aaf6890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365463"
---
# <a name="cbaselistaddbeforei-method"></a><span data-ttu-id="d2162-103">Cbaselist. addbeforei-Methode</span><span class="sxs-lookup"><span data-stu-id="d2162-103">CBaseList.AddBeforeI method</span></span>

<span data-ttu-id="d2162-104">Die- `AddBeforeI` Methode fügt ein Element vor der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="d2162-104">The `AddBeforeI` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2162-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2162-105">Syntax</span></span>


```C++
POSITION AddBeforeI(
   POSITION pos,
   void     *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="d2162-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2162-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2162-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="d2162-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="d2162-108">Die Position, vor der das Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d2162-108">Position before which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="d2162-109">*pobj*</span><span class="sxs-lookup"><span data-stu-id="d2162-109">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="d2162-110">Zeiger auf das Element.</span><span class="sxs-lookup"><span data-stu-id="d2162-110">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2162-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2162-111">Return value</span></span>

<span data-ttu-id="d2162-112">Gibt den Positionsindikator für das eingefügte Element zurück.</span><span class="sxs-lookup"><span data-stu-id="d2162-112">Returns the position indicator for the inserted item.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2162-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2162-113">Remarks</span></span>

<span data-ttu-id="d2162-114">Wenn *POS* **null** ist, fügt diese Methode das Element am Ende der Liste hinzu (entspricht dem Aufruf der [**cbaselist:: addtaili**](cbaselist-addtaili.md) -Methode).</span><span class="sxs-lookup"><span data-stu-id="d2162-114">If *pos* is **NULL**, this method adds the item to the tail of the list (equivalent to calling the [**CBaseList::AddTailI**](cbaselist-addtaili.md) method).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2162-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2162-115">Requirements</span></span>



| <span data-ttu-id="d2162-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2162-116">Requirement</span></span> | <span data-ttu-id="d2162-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d2162-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2162-118">Header</span><span class="sxs-lookup"><span data-stu-id="d2162-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d2162-119"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2162-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d2162-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d2162-120">Library</span></span><br/> | <dl> <span data-ttu-id="d2162-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d2162-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2162-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2162-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2162-123">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d2162-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




