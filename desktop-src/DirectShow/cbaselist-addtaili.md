---
description: Die addtaili-Methode fügt ein Element am Ende der Liste hinzu.
ms.assetid: 699408d1-fee2-43d7-b2c3-51637d063b2c
title: Cbaselist. addtaili-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c702256d75a2de6f914838f5c3412a4308a7241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361378"
---
# <a name="cbaselistaddtaili-method"></a><span data-ttu-id="7e260-103">Cbaselist. addtaili-Methode</span><span class="sxs-lookup"><span data-stu-id="7e260-103">CBaseList.AddTailI method</span></span>

<span data-ttu-id="7e260-104">Die- `AddTailI` Methode fügt ein Element am Ende der Liste hinzu.</span><span class="sxs-lookup"><span data-stu-id="7e260-104">The `AddTailI` method adds an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e260-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e260-105">Syntax</span></span>


```C++
POSITION AddTailI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="7e260-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e260-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e260-107">*pobj*</span><span class="sxs-lookup"><span data-stu-id="7e260-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="7e260-108">Zeiger auf das Element.</span><span class="sxs-lookup"><span data-stu-id="7e260-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e260-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e260-109">Return value</span></span>

<span data-ttu-id="7e260-110">Gibt einen Positionswert für die neue Endposition zurück.</span><span class="sxs-lookup"><span data-stu-id="7e260-110">Returns a POSITION value for the new tail position.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e260-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e260-111">Remarks</span></span>

<span data-ttu-id="7e260-112">Wenn die Methode fehlschlägt, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7e260-112">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e260-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e260-113">Requirements</span></span>



| <span data-ttu-id="7e260-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e260-114">Requirement</span></span> | <span data-ttu-id="7e260-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7e260-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e260-116">Header</span><span class="sxs-lookup"><span data-stu-id="7e260-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7e260-117"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e260-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7e260-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7e260-118">Library</span></span><br/> | <dl> <span data-ttu-id="7e260-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7e260-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e260-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e260-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e260-121">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7e260-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




