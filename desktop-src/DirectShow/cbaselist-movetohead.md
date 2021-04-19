---
description: Die-Methode wird von der-Methode der-Methode geteilt, und der Teil Fragment wird an der Spitze einer anderen Liste eingefügt.
ms.assetid: 46e4f8fe-6707-44c6-9d49-0168b35d2364
title: Cbaselist. muvedehead-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.MoveToHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 80adec6c8e2f6d42b5cf2cabd3a83a4c3aededa3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361520"
---
# <a name="cbaselistmovetohead-method"></a><span data-ttu-id="04532-103">Cbaselist. muvedehead-Methode</span><span class="sxs-lookup"><span data-stu-id="04532-103">CBaseList.MoveToHead method</span></span>

<span data-ttu-id="04532-104">Die `MoveToHead` -Methode teilt die Liste auf und fügt den Teil Fragment an der Spitze einer anderen Liste ein.</span><span class="sxs-lookup"><span data-stu-id="04532-104">The `MoveToHead` method splits the list and inserts the tail portion at the head of another list.</span></span>

## <a name="syntax"></a><span data-ttu-id="04532-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="04532-105">Syntax</span></span>


```C++
BOOL MoveToHead(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="04532-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="04532-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04532-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="04532-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="04532-108">Positionsindikator, mit dem die Aufteilung in der Liste markiert wird.</span><span class="sxs-lookup"><span data-stu-id="04532-108">Position indicator that marks the split in the list.</span></span>

</dd> <dt>

<span data-ttu-id="04532-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="04532-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="04532-110">Zeiger auf eine andere Liste.</span><span class="sxs-lookup"><span data-stu-id="04532-110">Pointer to another list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04532-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04532-111">Return value</span></span>

<span data-ttu-id="04532-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="04532-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="04532-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04532-113">Remarks</span></span>

<span data-ttu-id="04532-114">Diese Methode teilt die Liste vor der durch den *POS* -Parameter angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="04532-114">This method splits the list before the position specified by the *pos* parameter.</span></span> <span data-ttu-id="04532-115">Der Kopfteil verbleibt in der Liste.</span><span class="sxs-lookup"><span data-stu-id="04532-115">The head portion remains in the list.</span></span> <span data-ttu-id="04532-116">Der Teil Teil wird an der Spitze der anderen Liste eingefügt.</span><span class="sxs-lookup"><span data-stu-id="04532-116">The tail portion is inserted at the head of the other list.</span></span>

## <a name="requirements"></a><span data-ttu-id="04532-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04532-117">Requirements</span></span>



| <span data-ttu-id="04532-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04532-118">Requirement</span></span> | <span data-ttu-id="04532-119">Wert</span><span class="sxs-lookup"><span data-stu-id="04532-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04532-120">Header</span><span class="sxs-lookup"><span data-stu-id="04532-120">Header</span></span><br/>  | <dl> <span data-ttu-id="04532-121"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04532-121"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="04532-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="04532-122">Library</span></span><br/> | <dl> <span data-ttu-id="04532-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="04532-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04532-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="04532-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04532-125">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="04532-125">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




