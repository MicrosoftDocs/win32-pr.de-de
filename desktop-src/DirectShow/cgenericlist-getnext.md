---
description: Die GetNext-Methode ruft das Element an der angegebenen Position ab und erhöht die Position.
ms.assetid: d24d3388-1af9-4a62-bdb6-d3d3f5b0b97a
title: Cgenericlist. GetNext-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.GetNext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9491e58d817ce2c9dc4fb59fafa9bf96812a013a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366765"
---
# <a name="cgenericlistgetnext-method"></a><span data-ttu-id="a358c-103">Cgenericlist. GetNext-Methode</span><span class="sxs-lookup"><span data-stu-id="a358c-103">CGenericList.GetNext method</span></span>

<span data-ttu-id="a358c-104">Die `GetNext` -Methode ruft das Element an der angegebenen Position ab und erhöht die Position.</span><span class="sxs-lookup"><span data-stu-id="a358c-104">The `GetNext` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="a358c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a358c-105">Syntax</span></span>


```C++
OBJECT* GetNext(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="a358c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a358c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a358c-107">*RP* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="a358c-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a358c-108">Verweis auf einen Positionswert.</span><span class="sxs-lookup"><span data-stu-id="a358c-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a358c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a358c-109">Return value</span></span>

<span data-ttu-id="a358c-110">Gibt einen Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp) zurück.</span><span class="sxs-lookup"><span data-stu-id="a358c-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="a358c-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a358c-111">Remarks</span></span>

<span data-ttu-id="a358c-112">Diese Methode verschiebt den Positionsindikator auf die nächste Position.</span><span class="sxs-lookup"><span data-stu-id="a358c-112">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="a358c-113">Wenn sich der Positionsindikator hinter das Ende der Liste bewegt, legt die-Methode ihn auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="a358c-113">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

<span data-ttu-id="a358c-114">Wenn *RP* **null** ist, gibt die Methode **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="a358c-114">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a358c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a358c-115">Requirements</span></span>



| <span data-ttu-id="a358c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a358c-116">Requirement</span></span> | <span data-ttu-id="a358c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a358c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a358c-118">Header</span><span class="sxs-lookup"><span data-stu-id="a358c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a358c-119"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a358c-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a358c-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a358c-120">Library</span></span><br/> | <dl> <span data-ttu-id="a358c-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a358c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a358c-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a358c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a358c-123">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a358c-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




