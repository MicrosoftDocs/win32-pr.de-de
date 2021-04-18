---
description: Die prev-Methode ruft die vorherige Position in der Liste ab.
ms.assetid: 537c3019-373a-4974-a42e-72150da72767
title: Cbaselist. prev-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Prev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03c35a89754b27aa67a5bba33ee694433d74c0fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365462"
---
# <a name="cbaselistprev-method"></a><span data-ttu-id="1025d-103">Cbaselist. prev-Methode</span><span class="sxs-lookup"><span data-stu-id="1025d-103">CBaseList.Prev method</span></span>

<span data-ttu-id="1025d-104">Die- `Prev` Methode ruft die vorherige Position in der Liste ab.</span><span class="sxs-lookup"><span data-stu-id="1025d-104">The `Prev` method retrieves the previous position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1025d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1025d-105">Syntax</span></span>


```C++
POSITION Prev(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="1025d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1025d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1025d-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="1025d-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="1025d-108">Positionswert.</span><span class="sxs-lookup"><span data-stu-id="1025d-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1025d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1025d-109">Return value</span></span>

<span data-ttu-id="1025d-110">Gibt den Positionsindikator zurück, der vor der in *POS* angegebenen Position liegt.</span><span class="sxs-lookup"><span data-stu-id="1025d-110">Returns the position indicator that is previous to the position specified in *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="1025d-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1025d-111">Remarks</span></span>

<span data-ttu-id="1025d-112">Wenn *POS* die erste Position in der Liste ist, gibt die Methode **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="1025d-112">If *pos* is the first position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="1025d-113">Wenn *POS* **null** ist, gibt die Methode die letzte Position in der Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="1025d-113">If *pos* is **NULL**, the method returns the last position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="1025d-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1025d-114">Requirements</span></span>



| <span data-ttu-id="1025d-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1025d-115">Requirement</span></span> | <span data-ttu-id="1025d-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1025d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1025d-117">Header</span><span class="sxs-lookup"><span data-stu-id="1025d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1025d-118"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1025d-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1025d-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1025d-119">Library</span></span><br/> | <dl> <span data-ttu-id="1025d-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1025d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1025d-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1025d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1025d-122">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1025d-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




