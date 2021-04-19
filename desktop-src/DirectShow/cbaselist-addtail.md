---
description: Die AddTail-Methode fügt am Ende dieser Liste eine andere Liste an.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Cbaselist. AddTail-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356502"
---
# <a name="cbaselistaddtail-method"></a><span data-ttu-id="ef113-103">Cbaselist. AddTail-Methode</span><span class="sxs-lookup"><span data-stu-id="ef113-103">CBaseList.AddTail method</span></span>

<span data-ttu-id="ef113-104">Die- `AddTail` Methode fügt am Ende dieser Liste eine andere Liste an.</span><span class="sxs-lookup"><span data-stu-id="ef113-104">The `AddTail` method appends another list to the end of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef113-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef113-105">Syntax</span></span>


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="ef113-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef113-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef113-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="ef113-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="ef113-108">Ein Zeiger auf die anzufügende Liste.</span><span class="sxs-lookup"><span data-stu-id="ef113-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef113-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef113-109">Return value</span></span>

<span data-ttu-id="ef113-110">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ef113-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef113-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef113-111">Remarks</span></span>

<span data-ttu-id="ef113-112">Wenn die Methode fehlschlägt, wurden möglicherweise einige Elemente zur Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ef113-112">If the method fails, some items may have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef113-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef113-113">Requirements</span></span>



| <span data-ttu-id="ef113-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef113-114">Requirement</span></span> | <span data-ttu-id="ef113-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ef113-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef113-116">Header</span><span class="sxs-lookup"><span data-stu-id="ef113-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ef113-117"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef113-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ef113-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef113-118">Library</span></span><br/> | <dl> <span data-ttu-id="ef113-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ef113-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef113-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef113-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef113-121">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ef113-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




