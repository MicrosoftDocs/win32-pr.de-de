---
description: Die AddHead-Methode fügt am Anfang dieser Liste eine andere Liste ein.
ms.assetid: 10999d93-2eb0-481f-8909-6f1184137786
title: Cbaselist. AddHead-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a262f2bcfb7c40671fd472ecd7d3f887b1db4224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373785"
---
# <a name="cbaselistaddhead-method"></a><span data-ttu-id="ce25c-103">Cbaselist. AddHead-Methode</span><span class="sxs-lookup"><span data-stu-id="ce25c-103">CBaseList.AddHead method</span></span>

<span data-ttu-id="ce25c-104">Die- `AddHead` Methode fügt am Anfang dieser Liste eine andere Liste ein.</span><span class="sxs-lookup"><span data-stu-id="ce25c-104">The `AddHead` method inserts another list at the front of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce25c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce25c-105">Syntax</span></span>


```C++
BOOL AddHead(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="ce25c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce25c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce25c-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="ce25c-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="ce25c-108">Ein Zeiger auf die Liste der hinzu zufügenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="ce25c-108">Pointer to the list of items to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce25c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce25c-109">Return value</span></span>

<span data-ttu-id="ce25c-110">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="ce25c-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce25c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce25c-111">Remarks</span></span>

<span data-ttu-id="ce25c-112">Wenn die Methode fehlschlägt, wurden möglicherweise einige Elemente zur Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ce25c-112">If the method fails, some items might have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce25c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce25c-113">Requirements</span></span>



| <span data-ttu-id="ce25c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce25c-114">Requirement</span></span> | <span data-ttu-id="ce25c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ce25c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce25c-116">Header</span><span class="sxs-lookup"><span data-stu-id="ce25c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ce25c-117"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce25c-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ce25c-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce25c-118">Library</span></span><br/> | <dl> <span data-ttu-id="ce25c-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ce25c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce25c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce25c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce25c-121">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ce25c-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




