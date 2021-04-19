---
description: Die getnexti-Methode ruft das Element an der angegebenen Position ab und erhöht die Position.
ms.assetid: 3ec217ec-b0f9-4ff4-bdb7-ac204df99010
title: Cbaselist. getnexti-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetNextI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f96be8d8cdf286a4017e56af7050970d45e8a56e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370116"
---
# <a name="cbaselistgetnexti-method"></a><span data-ttu-id="ab87b-103">Cbaselist. getnexti-Methode</span><span class="sxs-lookup"><span data-stu-id="ab87b-103">CBaseList.GetNextI method</span></span>

<span data-ttu-id="ab87b-104">Die `GetNextI` -Methode ruft das Element an der angegebenen Position ab und erhöht die Position.</span><span class="sxs-lookup"><span data-stu-id="ab87b-104">The `GetNextI` method retrieves the item at the specified position, and advances the position.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab87b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab87b-105">Syntax</span></span>


```C++
void* GetNextI(
  [ref] POSITION &rp
);
```



## <a name="parameters"></a><span data-ttu-id="ab87b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab87b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab87b-107">*RP* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="ab87b-107">*rp* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ab87b-108">Verweis auf einen Positionswert.</span><span class="sxs-lookup"><span data-stu-id="ab87b-108">Reference to a POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab87b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab87b-109">Return value</span></span>

<span data-ttu-id="ab87b-110">Gibt einen Zeiger auf das Element zurück.</span><span class="sxs-lookup"><span data-stu-id="ab87b-110">Returns a pointer to the item.</span></span> <span data-ttu-id="ab87b-111">Wenn *RP* **null** ist, gibt die Methode **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="ab87b-111">If *rp* is **NULL**, the method returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab87b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab87b-112">Remarks</span></span>

<span data-ttu-id="ab87b-113">Diese Methode verschiebt den Positionsindikator auf die nächste Position.</span><span class="sxs-lookup"><span data-stu-id="ab87b-113">This method advances the position indicator to the next position.</span></span> <span data-ttu-id="ab87b-114">Wenn sich der Positionsindikator hinter das Ende der Liste bewegt, legt die-Methode ihn auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="ab87b-114">If the position indicator moves past the end of the list, the method sets it to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab87b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab87b-115">Requirements</span></span>



| <span data-ttu-id="ab87b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab87b-116">Requirement</span></span> | <span data-ttu-id="ab87b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ab87b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab87b-118">Header</span><span class="sxs-lookup"><span data-stu-id="ab87b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ab87b-119"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab87b-119"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ab87b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ab87b-120">Library</span></span><br/> | <dl> <span data-ttu-id="ab87b-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ab87b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab87b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab87b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab87b-123">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ab87b-123">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




