---
description: Die findi-Methode ruft die erste Position ab, die das angegebene Element enthält.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: Cbaselist. findi-Methode (wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2366f8c4c117b8550d91c84bffafb03393801088
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351344"
---
# <a name="cbaselistfindi-method"></a><span data-ttu-id="edc0e-103">Cbaselist. findi-Methode</span><span class="sxs-lookup"><span data-stu-id="edc0e-103">CBaseList.FindI method</span></span>

<span data-ttu-id="edc0e-104">Die- `FindI` Methode ruft die erste Position ab, die das angegebene Element enthält.</span><span class="sxs-lookup"><span data-stu-id="edc0e-104">The `FindI` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="edc0e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="edc0e-105">Syntax</span></span>


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="edc0e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="edc0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edc0e-107">*pobj*</span><span class="sxs-lookup"><span data-stu-id="edc0e-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="edc0e-108">Zeiger auf das Element.</span><span class="sxs-lookup"><span data-stu-id="edc0e-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edc0e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="edc0e-109">Return value</span></span>

<span data-ttu-id="edc0e-110">Gibt einen Positionswert oder **null** zurück, wenn das Element nicht in der Liste enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="edc0e-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="edc0e-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edc0e-111">Requirements</span></span>



| <span data-ttu-id="edc0e-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="edc0e-112">Requirement</span></span> | <span data-ttu-id="edc0e-113">Wert</span><span class="sxs-lookup"><span data-stu-id="edc0e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edc0e-114">Header</span><span class="sxs-lookup"><span data-stu-id="edc0e-114">Header</span></span><br/>  | <dl> <span data-ttu-id="edc0e-115"><dt>Wxlist. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edc0e-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="edc0e-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="edc0e-116">Library</span></span><br/> | <dl> <span data-ttu-id="edc0e-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="edc0e-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edc0e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edc0e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edc0e-119">**Cbaselist-Klasse**</span><span class="sxs-lookup"><span data-stu-id="edc0e-119">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




