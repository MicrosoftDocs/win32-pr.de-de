---
description: Die AddAfter-Methode fügt eine Liste nach der angegebenen Position ein.
ms.assetid: c2a2e599-0a83-4eb0-aceb-c483f153ba7e
title: Cbaselist. AddAfter-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fdab54a124986b462e0ef592bba888e27c09b53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372087"
---
# <a name="cbaselistaddafter-method"></a><span data-ttu-id="1a0d0-103">Cbaselist. AddAfter-Methode</span><span class="sxs-lookup"><span data-stu-id="1a0d0-103">CBaseList.AddAfter method</span></span>

<span data-ttu-id="1a0d0-104">Die- `AddAfter` Methode fügt eine Liste nach der angegebenen Position ein.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a0d0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a0d0-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION  pos,
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="1a0d0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a0d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a0d0-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="1a0d0-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="1a0d0-108">Die Position, an der die Liste eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-108">Position after which to insert the list.</span></span>

</dd> <dt>

<span data-ttu-id="1a0d0-109">*pList*</span><span class="sxs-lookup"><span data-stu-id="1a0d0-109">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="1a0d0-110">Ein Zeiger auf die einzufügende Liste.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-110">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a0d0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a0d0-111">Return value</span></span>

<span data-ttu-id="1a0d0-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="1a0d0-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a0d0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a0d0-113">Remarks</span></span>

<span data-ttu-id="1a0d0-114">Vorhandene positionsindikatoren, einschließlich der im *POS* -Parameter angegebenen, bleiben gültig.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-114">Existing position indicators, including the one specified in the *pos* parameter, remain valid.</span></span> <span data-ttu-id="1a0d0-115">Wenn die Methode fehlschlägt, wurden möglicherweise einige der Elemente hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1a0d0-115">If the method fails, some of the items might have been added.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a0d0-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a0d0-116">Requirements</span></span>



| <span data-ttu-id="1a0d0-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a0d0-117">Requirement</span></span> | <span data-ttu-id="1a0d0-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1a0d0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a0d0-119">Header</span><span class="sxs-lookup"><span data-stu-id="1a0d0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1a0d0-120"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a0d0-120"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1a0d0-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a0d0-121">Library</span></span><br/> | <dl> <span data-ttu-id="1a0d0-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1a0d0-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a0d0-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a0d0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a0d0-124">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1a0d0-124">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




