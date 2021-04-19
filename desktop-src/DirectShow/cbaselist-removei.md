---
description: Die removei-Methode entfernt das Element an der angegebenen Position.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Cbaselist. removei-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365701"
---
# <a name="cbaselistremovei-method"></a><span data-ttu-id="6c821-103">Cbaselist. removei-Methode</span><span class="sxs-lookup"><span data-stu-id="6c821-103">CBaseList.RemoveI method</span></span>

<span data-ttu-id="6c821-104">Die- `RemoveI` Methode entfernt das Element an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="6c821-104">The `RemoveI` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c821-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c821-105">Syntax</span></span>


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="6c821-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c821-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c821-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="6c821-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="6c821-108">Positionswert, der das zu entfern gende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="6c821-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c821-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c821-109">Return value</span></span>

<span data-ttu-id="6c821-110">Gibt einen Zeiger auf das Element zurück.</span><span class="sxs-lookup"><span data-stu-id="6c821-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c821-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c821-111">Remarks</span></span>

<span data-ttu-id="6c821-112">Diese Methode löscht den Knoten aus der Liste, löscht jedoch nicht das Element, das in diesem Knoten enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6c821-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="6c821-113">Wenn *POS* **null** ist, gibt die Methode **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="6c821-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c821-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c821-114">Requirements</span></span>



| <span data-ttu-id="6c821-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c821-115">Requirement</span></span> | <span data-ttu-id="6c821-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6c821-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c821-117">Header</span><span class="sxs-lookup"><span data-stu-id="6c821-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6c821-118"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c821-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6c821-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c821-119">Library</span></span><br/> | <dl> <span data-ttu-id="6c821-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6c821-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c821-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c821-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c821-122">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6c821-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




