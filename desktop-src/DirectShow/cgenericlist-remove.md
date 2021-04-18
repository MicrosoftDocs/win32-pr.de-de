---
description: Die Remove-Methode entfernt das Element an der angegebenen Position.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Cgenericlist. Remove-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358624"
---
# <a name="cgenericlistremove-method"></a><span data-ttu-id="d8a26-103">Cgenericlist. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="d8a26-103">CGenericList.Remove method</span></span>

<span data-ttu-id="d8a26-104">Die- `Remove` Methode entfernt das Element an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="d8a26-104">The `Remove` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8a26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8a26-105">Syntax</span></span>


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="d8a26-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8a26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8a26-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="d8a26-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="d8a26-108">Positionswert, der das zu entfern gende Element angibt.</span><span class="sxs-lookup"><span data-stu-id="d8a26-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8a26-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8a26-109">Return value</span></span>

<span data-ttu-id="d8a26-110">Gibt einen Zeiger auf ein Objekt vom Typ " **Object** " (der Vorlagentyp) zurück.</span><span class="sxs-lookup"><span data-stu-id="d8a26-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="d8a26-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8a26-111">Remarks</span></span>

<span data-ttu-id="d8a26-112">Diese Methode löscht den Knoten aus der Liste, löscht jedoch nicht das Element, das in diesem Knoten enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d8a26-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="d8a26-113">Wenn *POS* **null** ist, gibt die Methode **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="d8a26-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8a26-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8a26-114">Requirements</span></span>



| <span data-ttu-id="d8a26-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8a26-115">Requirement</span></span> | <span data-ttu-id="d8a26-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d8a26-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8a26-117">Header</span><span class="sxs-lookup"><span data-stu-id="d8a26-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d8a26-118"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8a26-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d8a26-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d8a26-119">Library</span></span><br/> | <dl> <span data-ttu-id="d8a26-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d8a26-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8a26-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8a26-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8a26-122">**Cgenericlist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d8a26-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




