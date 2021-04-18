---
description: Die GetI-Methode ruft das Element an der angegebenen Position ab.
ms.assetid: fc775230-491a-49b6-b631-e7d5b8c82d8c
title: Cbaselist. GetI-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.GetI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2473401aeaee201456b4eede39ffb492f40ee2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358110"
---
# <a name="cbaselistgeti-method"></a><span data-ttu-id="6a69f-103">Cbaselist. GetI-Methode</span><span class="sxs-lookup"><span data-stu-id="6a69f-103">CBaseList.GetI method</span></span>

<span data-ttu-id="6a69f-104">Die- `GetI` Methode ruft das Element an der angegebenen Position ab.</span><span class="sxs-lookup"><span data-stu-id="6a69f-104">The `GetI` method retrieves the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a69f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a69f-105">Syntax</span></span>


```C++
void* GetI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="6a69f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a69f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a69f-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="6a69f-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="6a69f-108">Positionsindikator für das Element, das abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a69f-108">Position indicator for the item to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a69f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a69f-109">Return value</span></span>

<span data-ttu-id="6a69f-110">Gibt einen Zeiger auf das Element zurück.</span><span class="sxs-lookup"><span data-stu-id="6a69f-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a69f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a69f-111">Remarks</span></span>

<span data-ttu-id="6a69f-112">Wenn *POS* **null** ist, gibt die Methode **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="6a69f-112">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a69f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a69f-113">Requirements</span></span>



| <span data-ttu-id="6a69f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a69f-114">Requirement</span></span> | <span data-ttu-id="6a69f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6a69f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a69f-116">Header</span><span class="sxs-lookup"><span data-stu-id="6a69f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6a69f-117"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a69f-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6a69f-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6a69f-118">Library</span></span><br/> | <dl> <span data-ttu-id="6a69f-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6a69f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a69f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a69f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a69f-121">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6a69f-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




