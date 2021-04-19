---
description: Die addheadi-Methode fügt ein Element am Anfang der Liste hinzu.
ms.assetid: d83b3c5e-2c6d-4369-a74d-18bf19cfd34d
title: Cbaselist. addheadi-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6104b6acae0f22c028f3bad050567f4da34ff0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370117"
---
# <a name="cbaselistaddheadi-method"></a><span data-ttu-id="d2113-103">Cbaselist. addheadi-Methode</span><span class="sxs-lookup"><span data-stu-id="d2113-103">CBaseList.AddHeadI method</span></span>

<span data-ttu-id="d2113-104">Mit der- `AddHeadI` Methode wird ein Element am Anfang der Liste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d2113-104">The `AddHeadI` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2113-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2113-105">Syntax</span></span>


```C++
POSITION AddHeadI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="d2113-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2113-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2113-107">*pobj*</span><span class="sxs-lookup"><span data-stu-id="d2113-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="d2113-108">Zeiger auf das Element.</span><span class="sxs-lookup"><span data-stu-id="d2113-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2113-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2113-109">Return value</span></span>

<span data-ttu-id="d2113-110">Gibt einen Positionswert zurück, der die neue Head-Position angibt.</span><span class="sxs-lookup"><span data-stu-id="d2113-110">Returns a POSITION value indicating the new head position.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2113-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d2113-111">Remarks</span></span>

<span data-ttu-id="d2113-112">Wenn die Methode fehlschlägt, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="d2113-112">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2113-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2113-113">Requirements</span></span>



| <span data-ttu-id="d2113-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2113-114">Requirement</span></span> | <span data-ttu-id="d2113-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d2113-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2113-116">Header</span><span class="sxs-lookup"><span data-stu-id="d2113-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d2113-117"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2113-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d2113-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d2113-118">Library</span></span><br/> | <dl> <span data-ttu-id="d2113-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d2113-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2113-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2113-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2113-121">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d2113-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




